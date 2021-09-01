# NYC-Taxi-Trip-Time-Prediction

Colab Notebook Link - https://colab.research.google.com/drive/1X0A7JTOoEcJpTZtB2XZsBekaTg3wph84?usp=sharing

## Problem Statement
Your task is to build a model that predicts the total ride duration of taxi trips in New York City. Your primary dataset is one released by the NYC Taxi and Limousine Commission, which includes pickup time, geo-coordinates, number of passengers, and several other variables

## Data Description
The dataset is based on the 2016 NYC Yellow Cab trip record data made available in Big Query on Google Cloud Platform. The data was originally published by the NYC Taxi and Limousine Commission (TLC). The data was sampled and cleaned for the purposes of this project. Based on individual trip attributes, you should predict the duration of each trip in the test set.

## Objective
To Explore various attributes and build a Predictive model that predicts the total trip duration of taxi trips in New York City.

## Architecture
Data Preparation and Exploratory Data Analysis > Build Predictive Model using Multiple Techniques/Algorithms > Optimal Model identified through Testing and Evaluation

## Short Summary
Approach is that to build a model that predicts the total ride duration of taxi trips in New York City and the Target variable is Trip Duration. And I get to know after doing this analysis that Trip Duration varies a lot ranging from few seconds to more than 20 hours also some are going from 528 Hours to 972 Hours and there is two taxi service provider(Vendor) where 2nd vendor is most frequently use. Trip duration takes longer whose flag was not stored before sending to vendors. Few trips found with Zero Passenger and 3 trips with 7 and 1 trip each with 8 & 9 Passengers may be some vendor is using big taxi’s and also few trips have covered Zero Km. distance this may be due to trip cancellation or target completion. Trip duration is the maximum around 3 PM (Rush hours) and the lowest around 6 AM (Streets are free in the morning) and is the longest on Thursdays closely followed by Fridays and Saturday maybe due to weekend. January having the lowest trips count may be due to snowfall and From February, we can see trip duration rising every month also there was a significant drop in the Taxi trip count as a month-end approach.

Also, we are talking about applying a machine learning algorithm first will Normalizing the Dataset using Standard Scaling Technique then we had passed our Scaled Dataframe in the PCA model to reduce dimension so that we can apply it to the ML regression algorithm. Then after applying it to models, we get to know that when we compare to linear regression, decision tree, and random Forest we are getting the best model result with Random Forest.

And without applying PCA we are getting good results for random Forest and also when we apply GridsearchCV in the decision tree we got the best result as compared to others. We can say that without Hyperparameter tuning Random Forest model will be less prone to overfitting than the Decision tree, and gives a more generalized solution, and also is more robust and accurate than decision tree.

But if we use any outlier remover techniques (Z-Score, IQR, etc.) then Hyperparameter tuning will perform best on our models.
