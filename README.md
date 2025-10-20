# 🏠 Predicting House Prices using Square Footage
## Principles of ML Lifecycle: Data Cleaning, Feature Engineering to Train Linear Regression Model
El Brewster

---

## Dataset Description

This project uses a housing dataset containing property sale information for King County, Washington. The dataset includes numerical and categorical features such as living area (`sqft_living`), lot size, number of bedrooms and bathrooms, year built, and sale price.
The target variable in this analysis is `price_per_sqft`, representing the sale price divided by the home’s living area. This metric normalizes prices across different home sizes, making it easier to compare properties.

---

## Data Cleaning and Feature Engineering

- Removed duplicate and missing records to ensure data integrity.
- Converted relevant features to numeric types and handled outliers where appropriate.
- Created new features such as `price_per_sqft` for normalized price comparisons.
- Applied logarithmic transformations to highly skewed variables to improve linearity where relevant.
- Split the data into training (80%) and testing (20%) subsets for model evaluation.

---

## Model and Evaluation

A simple linear regression model was trained using one predictor variable to estimate `price_per_sqft`.
The model’s performance on the test set was:
- R²: 0.995
- RMSE: 29,468.09
These results indicate an excellent model fit, with the regression line explaining approximately 99.5% of the variation in price per square foot and an average prediction error of about $29,500.




