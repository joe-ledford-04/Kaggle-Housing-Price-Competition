# Kaggle-Housing-Price-Competition

This repository includes all of my Kaggle Housing Price competition submissions. The dataset for this competiton includes 1459 observations of residential homes in Ames, Iowa. It includes 79 feature variables and is evaluated based on Root Mean Squared Error (RMSE).


## Submission One

My first ever Kaggle submission which follows the template given by the competiton.

## Submission Two

Ranked 877 globally with an RMSE score of 0.12381, my second submission greatly expands on my first submission. This version properly deals with missing values depending on a particular feature; imputing a constant for categorical features that already had a value designated for NA, while categorical features without a valid NA value were imputed using the column's mode. For numerical features, they were imputed using KNN imputation. After that, I transitioned to feature transformation. Numerical features were log transformed to deal with skewness, and a cosine transformation was done for the Month Sold (MoSold) to deal with its cyclical nature. The target variable, sale price, was also log transformed so that it matched the rest of the training set. Once I transformed the data, categorical features were encoded, and the standard sklearn scalar was applied to the dataset. I then split the data back into its original form before comparing models using Pycaret. Its initial output recommended a CatBoost Regressor, which I used for this submission. 

## Submission Three

Ranked 768 globally with an RMSE score of 0.12308, my third submission added ensembling. I removed the baseline model that only uses a Catboosted regressor and included a combination of four other models that both performed well and added variation to the approach of the problem. The final prediction on the test set is a combination of all five models' predictions equally weighted by 20%. This lowered my RMSE score by .00073 and improved my global ranking by 109. 


## Future Submissions

My fourth submission will build upon the third by adding feature engineering 
