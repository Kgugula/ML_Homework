# ML_Homework

For this homework activity we used supervised machine learning algorithms to classify transactions as either being a high loan risk (target=0) or a low loan risk (target=1)

# Credit Risk Resampling #

First steps were to read in the CSV and preprocess the data (binary encode certain columns/make sure only numerical values), the preprocessed data was then saved to a csv and can be viewed under the 'Resources' folder. I tried using StandardScaler() to scale key values, but I assumed you couldn't do that after looking at where it put my binary values for loan risk (they were decimals and not 0 or 1). After that split data into features (X) from the dependent variable (y). 

Next, I tried classifying the data using a Simple Logistic Regression --> it did not produce superior results. That was to be expected since it was working with imbalanced data and didn't resample the classes. I then used various Oversampling and UnderSampling techniques. This means they resampled either the minority or majority class so that majority class == minorityclass. The best results came from the two Oversampling technique --> Naive OverSampling and SMOTE. This Makes sense b/c with Undersampling the algorithms reduce the majority class to == minority and this results in less training data overall. 

Best balanced accuracy score --> SMOTE oversampling
Best recall score --> tied b/w two oversampling techniques (random and SMOTE) and combination algorithm (SMOTEENN)
Best geometric mean score --> again, same as above

# Credit Risk Ensemble #

For this portion of the homework assignment I used ensemble algorithms to see which one classified more accurately (same data as previous notebook). 

Used Balanced Random Forest Classifier & Easy Ensemble Classifier

Both algorithm's produced high balanced accuracy scores w/ the EasyEnsember beating out the BRF by a small margin (.9945 v. .9937)

Best balanced accuracy score --> EasyEnsemble
Best recall score --> identical
Best geometric mean score --> identical
Top three features --> interest rate, borrower income, debt to income




