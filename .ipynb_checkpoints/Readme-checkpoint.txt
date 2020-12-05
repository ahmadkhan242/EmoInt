Winter Internship 2021 coding assignment to predict intensity of emotion.

Problem website - https://www.google.com/url?sa=D&q=https://saifmohammad.com/WebPages/EmotionIntensity-SharedTask.html&ust=1607168520000000&usg=AOvVaw36bG8H9EL2CIUJy3tqvBva&hl=en&source=gmail
For this we have to use Anger and Joy classes.
All dataset can be downloaded from the above website.

-----------------------------------Approachs------------------------------------------ 
For this Assignment I had use Two approachs.
1.) Based on dataset.
    a.) First used Raw data.
    b.) Pre-processed all dataset.(Explained Below)

2.) Based on Vocabulary
    a.) Used simple Stopword to create TfidfVectorizer.
    b.) Used cutome Vocabulary created using unigrams and bigrams from tweet data.
    c.) Used Twitter Glove Embedding.
    
-----------------------------------Models-------------------------------------------- 
I had used Three model 
1.) Random Forest Regressor.
2.) SVM.
3.) Simple MLP using keras(run for 100 epochs).


All code implemention is given in Jupyter notebook with relevent comments.

-----------------------------------Results-------------------------------------------
Following are the best result obtain in test set for each approach.
####################################  For Anger  ####################################
1.) Without Pre-processing.
    a.) simple Stopword.
        Best result - Random Forest
                metrics     Value
        0          Pearsonr  0.247100
        1         Spearmanr  0.222550
        2   Pearsonr >= 0.5  0.136760
        3  Spearmanr >= 0.5  0.109948
        
    b.) cutome Vocabulary.
        Best result - Random Forest
                 metrics     Value
        0          Pearsonr  0.536161
        1         Spearmanr  0.504543
        2   Pearsonr >= 0.5  0.400112
        3  Spearmanr >= 0.5  0.363594
    
    c.) Twitter Glove Embedding.
        Best result - SVM
              metrics     Value
        0          Pearsonr  0.586624
        1         Spearmanr  0.580586
        2   Pearsonr >= 0.5  0.429999
        3  Spearmanr >= 0.5  0.424292
        
2.) With Pre-processing
    a.) simple Stopword.
        Best result - Random Forest
                       metrics     Value
        0          Pearsonr  0.243917
        1         Spearmanr  0.217084
        2   Pearsonr >= 0.5  0.128100
        3  Spearmanr >= 0.5  0.110319
        
    b.) cutome Vocabulary.
        Best result - Random Forest
                    metrics     Value
        0          Pearsonr  0.535899
        1         Spearmanr  0.504324
        2   Pearsonr >= 0.5  0.399039
        3  Spearmanr >= 0.5  0.360943
    
    c.) Twitter Glove Embedding.
        Best result - SVM
                    metrics     Value
        0          Pearsonr  0.587715
        1         Spearmanr  0.581532
        2   Pearsonr >= 0.5  0.432472
        3  Spearmanr >= 0.5  0.426328
        
####################################  For Joy  ######################################
1.) Without Pre-processing.
    a.) simple Stopword.
        Best result - Random Forest
                    metrics     Value
        0          Pearsonr  0.312417
        1         Spearmanr  0.309787
        2   Pearsonr >= 0.5  0.154492
        3  Spearmanr >= 0.5  0.160097
        
    b.) cutome Vocabulary.
        Best result - SVM
                    metrics     Value
        0          Pearsonr  0.474524
        1         Spearmanr  0.494809
        2   Pearsonr >= 0.5  0.308389
        3  Spearmanr >= 0.5  0.307756
        
    c.) Twitter Glove Embedding.
        Best result - SVM
                metrics     Value
        0          Pearsonr  0.606882
        1         Spearmanr  0.604149
        2   Pearsonr >= 0.5  0.449256
        3  Spearmanr >= 0.5  0.442449
    
2.) With Pre-processing
    a.) simple Stopword.
        Best result - Random Forest
            metrics     Value
        0          Pearsonr  0.257611
        1         Spearmanr  0.256136
        2   Pearsonr >= 0.5  0.157086
        3  Spearmanr >= 0.5  0.154409
        
    b.) cutome Vocabulary.
        Best result - SVM
                    metrics     Value
        0          Pearsonr  0.482738
        1         Spearmanr  0.499942
        2   Pearsonr >= 0.5  0.310332
        3  Spearmanr >= 0.5  0.323588
        
    c.) Twitter Glove Embedding.
        Best result - SVM
                 metrics     Value
        0          Pearsonr  0.579386
        1         Spearmanr  0.576765
        2   Pearsonr >= 0.5  0.382190
        3  Spearmanr >= 0.5  0.382472
        
        
Results for all Approaches are present in Jupyter notebook of each class.