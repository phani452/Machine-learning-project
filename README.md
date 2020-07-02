# Machine-learning-project
Predicting House Prices using Regression Techniques

 

Chapter 1-Introduction
Problem Statement:
Problems Faced during buying a house:
1.Buying house is stressful thing
2.Buyers are not generally aware of the factors that influence the house price
3.Many problems are faced during buying a house
4.Hence real estate agents trusted with communication between seller and buyer as well as laying down a legal contract. This just creates another person in between and increases the cost
Problem Objective:
1.Our project is a machine learning model based on certain specifications of your home it will try to guess the most accurate price.
2.Information such as location, number of bedrooms etc
3. To predict the sale price of each houses
Reference link: https://www.ijitee.org/wpcontent/uploads/papers/v8i9/I7849078919.pdf
You can access code here: https://github.com/phani452/Machine-learning-project
Motivation
In order to predict the home prices, I chose the housing price dataset that was sourced from Kaggle. This dataset contains house sale prices for King County, which includes Seattle. It includes homes sold between May 2014 and May 2015. It has many characteristics of learning, and the dataset can be downloaded from here.
Chapter – 2
Exploratory Data Analysis & Anomaly detection
We divided our data into three sets train, validation and test 
Train data Info:
Our training data contains 9761 rows and 21 unique columns

Validation data Info:
Our validation data contains 9635 rows and 21 unique columns
Test data Info:
Our test data contains 2217 rows and 21 unique columns
Data Dictionary:
id - Unique ID for each home sold
date - Date of the home sale
price - Price of each home sold
bedrooms - Number of bedrooms
bathrooms - Number of bathrooms, where .5 accounts for a room with a toilet but no shower
sqft_living - Square footage of the apartments interior living space
sqft_lot - Square footage of the land space
floors - Number of floors
waterfront - A dummy variable for whether the apartment was overlooking the waterfront or not
view - An index from 0 to 4 of how good the view of the property was
condition - An index from 1 to 5 on the condition of the apartment
grade - An index from 1 to 13, where 1-3 falls short of building construction and design, 7 has an average level of construction and design, and 11-13 have a high-quality level of construction and design.
sqft_above - The square footage of the interior housing space that is above ground level
sqft_basement - The square footage of the interior housing space that is below ground level
yr_built - The year the house was initially built
yr_renovated - The year of the house’s last renovation
zip code - What zip code area the house is in
lat - Latitude
long - Longitude
sqft_living15 - The square footage of interior housing living space for the nearest 15 neighbours
sqft_lot15 - The square footage of the land lots of the nearest 15 neighbours
Variable Datatypes:
id – Nominal scale with numerical value
date – nominal scale in date format
price – numerical continuous variable
bedrooms – numerical discrete variable
bathrooms - numerical discrete variable
sqft_living - numerical continuous variable
sqft_lot - numerical continuous variable
floors - numerical discrete variable
waterfront - numerical discrete variable
view - Ordinal variable
condition - Ordinal variable
grade - Ordinal discrete variable
sqft_above - numerical continuous variable
sqft_basement - numerical continuous variable
yr_built – discrete variable
yr_renovated – discrete variable
zip code – nominal variable
lat - nominal variable
long - nominal variable
sqft_living15 - numerical continuous variable
sqft_lot15 - numerical continuous variable
Null values:
There are no null values in our Data.
Chapter 3:
Modelling:
Since our target variable price is a continuous variable, we apply different regression techniques on train and validation data and apply the best one on test data. 
Model 1:
From the correlation matrix we selected the columns which are highly correlated with the target column
and used them to predict the price.
Model-Multiple Linear Regression
Predictors:
Bedrooms,bathrooms,sqft_living,view,grade,sqft_above,sqft_basement,sqft_living15
We use metrics such as Root mean Squared Error(rmse) and r2_score to check our model.
We achieved an RMSE of 230245, We achieved an r2 score of 0.58
Model2:
Feature Engineering:
We created a new feature age from the yr_built feature by calculating the age of the house
 
We transformed yr_renovated column into binary
 
Model-Multiple Linear Regression
Predictors-each and every feature including newly created features
We use metrics such as Root mean Squared Error(rmse) and r2_score to check our model.
We achieved an RMSE of 194975
We achieved an r2 score of 0.70
Model 3:
From EDA we came to know that the location of the house plays an important role so we converted zipcode  
Variable using get dummies method as it is a categorical variable.
 
Model -Multiple Linear Regression
We use metrics such as Root mean Squared Error(rmse) and r2_score to check our model.
We achieved an RMSE of 15728, We achieved an r2 score of 0.80
Model 4:
In model 4 we transformed the total, total1, total2
variables using the log transformation and we removed the lat and long features as we are using zipcode.
trained our model
 
Model: Multiple Linear Regression
We use metrics such as Root mean Squared Error(rmse) and r2_score to check our model.
We achieved an RMSE of 120816
We achieved an r2 score of 0.88
Which is an improvement compared to all other models
Metrics of different models:
Model	RMSE	R2 score
Model-1	230245	0.58
Model-2	194975	0.70
Model-3	157284	0.80
Model-4	120816	0.88

Chapter 4:
Conclusion
Among the all models model 4 given the lowest rmse value and high r2 score. Hence, we used model 4 to predict the test data and we achieved an RMSE of
                                  RMSE=126847
Hence model4 can be used for deployment
Github link: 
https://github.com/phani452/Machine-learning-project
Reference link: https://www.ijitee.org/wpcontent/uploads/papers/v8i9/I7849078919.pdf

