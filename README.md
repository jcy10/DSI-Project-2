## DSI Project 2: Ames Housing Prediction Challenge
By: Yeo Jia Chi

## Problem Statement
Housing prices are dependent upon many factors, the question therefore is to determine which features play a bigger impact on increasing or decreasing the overall housing sale price. Using the Ames housing data, the goal of this project is to create a regression model that is able to accurately predict the sale price of each house in Ames, IA. 

The evaluation of this project will be done through a Kaggle submission, with leaderboard standings determined by the root mean squared error (RMSE) of your predicted house sale price vs. the actual house sale price.

## Executive Summary
Contents:
  - Importing the Libraries
  - Importing Training dataset
  - Manual Inspection of Dataset
  - Data Cleaning
  - Experimental Data Analysis (EDA)
  - Feature Engineering and Modelling
  - Pre-processing and prediction of actual test data
  - Final test scores

## Data Dictionary
As this is part of a Kaggle competition, the data dictionary may be found at below:
- https://www.kaggle.com/c/dsi-us-6-project-2-regression-challenge/data

## Key Findings
The most optimal features were used to model the target "SalePrice":
- Continuous:
  - PolynomialFeatures (degree=2) for:
    - "Mas Vnr Area"
    - "BsmtFin SF 1"
    - "Total Bsmt SF"
    - "Gr Liv Area"
    - "Garage Area"
- Categorical:
  - get_dummies for:
    - "Neighborhood"
    - "Overall Qual"
    - "Exter Qual"
    - "Bsmt Qual"
    - "Kitchen Qual"
    - "Garage Cars"

A total of 73 features were used for Linear Regression and Lasso Regression.

## Model Evaluation

Using linear regression, the model's RMSE score was:
- Kaggle private score: 30262.80
- Kaggle public score: 28869.88

Using lasso regularization, my model's RMSE score was:
- Kaggle private score: 31505.63
- Kaggle public score: 30562.34

Overall, both models were able to predict housing saleprices with an approximate r2-score of 0.8.

## Conclusions

- Through the exercise, it is interesting to observe that the features which best predict the house sale price were "general" in nature. By this, I found that people largely based their sale price on features such as number of square-feet (area), housing build quality, and the neighborhood it is located in (i.e. common features which every house should have). 

- This discovery also gives me confidence that our model is sufficiently generalized to be applied across future instances within the city of Ames, IA for sale price predictions, or as a guide for property evaluators.

- Overall, this exercise has provided the exposure towards data cleaning, engineering and modelling real-life data problems. Subsequently, as more advanced machine learning technique would be taught, this project may be revisited to find ways to better improve the Kaggle test scores.

