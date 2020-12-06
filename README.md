# ML_Homework

For this homework activity we used supervised ML algorithms to classify transactions as either being a loan risk (0) or NOT being a loan risk (1)

# Credit Risk Resampling #

First steps were to read in the CSV and preprocess the data (binary encode certain columns/make sure only numerical values). I tried using StandardScaler() to scale key values, but I assumed you couldn't do that after looking at where it put my binary values for loan risk (they were decimals and not 0 or 1). After that split data into features (X) from the dependent variable (y)

After that tried classifying the data using a Simple Logistic Regression --> didn't produce the best results. That was to be expected since it was working with imbalanced data and didn't resample the features. Next, used various Oversampling and UnderSampling techniques. This means they resampled either the minority or majority class so that majority == minority. The best results came from the two Oversampling technique --> Naive OverSampling and SMOTE. Makes sense b/c with Undersampling the algo's reduce the majority class to == minority and this results in less training data overall. 

Best balanced accuracy score --> SMOTE oversampling
Best recall score --> tied b/w two oversampling techniques (random and SMOTE) and combination algo (SMOTEENN)
Best geo mean score --> again, same as above

# Credit Risk Ensemble #

For this portion of homework used to ensemble algorithms to see which one classified more accurately (same data as previous notebook)

Used Balanced Random Forest Classifier & Easy Ensemble Classifier

Both algo's produced high balanced accuracy scores w/ the EasyEnsember beating out the BRF by a small margin (.9945 v. .9937)

Best balanced accuracy score --> EasyEnsemble
Best recall score --> identical
Best geo mean score --> identical
Top three features --> interest rate, borrower income, debt to income




