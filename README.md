# football_hackathon
A data science hackathon hosted by "ANALYTICAL VIDHYA". Includes football data analysis and prediction. POSTION: TOP 5% @ number 20\500+ in private and public leaderboards.

Data Exploration:
The dataset had numerous null values.
First, we checked for columns present in the train dataset and absent in the test dataset:
We got the ‘rating_num’. Columns present in test dataset but absent in train dataset: this gave us none.

Then, we combined the train and test datasets, we did this so we could have more information to work with during preposing. Concatenating them on top of each other.
Some features were embedded as numeric but actually should be categorical, such features should be set to string so we can treat them properly in the coming stages


Approach
We tried different models like: XGBRegressor, LGBMRegressor, ExtraTreesRegressor,lightgbm,CATboost after feature selection, 
Using “Scipy”, we checked if certain models will perform better if the data was normally distributed, be checked for the skewness of the data, then checked for the numeric features, which will be corrected for skewness. Determining our absolute skewness to be greater than 0.5, then applying the transformation.
After transformation, we checked the skewness again, our target transformation looked negatively skewed, we got zero, then we used log 1p.


Feature Engineering:
The feature engineering was done by clustering similar columns,

Final Model and Submission:
We split into 2 separate datasets- the test and trained data, this became our final train and test sets, the data was split the same dimension as the original train and test sets.
We trained on train set and evaluated on test sets. Using XGBRegressor, Catboost, BayesianRidge

