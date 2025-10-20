# 🏠 Simple Linear Regression: Predicting Housing Prices from Living Area
Principles of ML Lifecycle: Data Cleaning and Feature Engineering to Train Linear Regression Model
El Brewster

## Dataset Description
This project utilizes a housing dataset containing property sale records from King County, Washington. The dataset includes a range of structural and physical attributes such as living area (`sqft_living`), lot size, number of bedrooms and bathrooms, and final sale price.
The target variable for this analysis is `price`, representing each property's sale price in U.S. dollars.

---

## Data Cleaning and Feature Engineering

To prepare the dataset for modeling, the following preprocessing steps were performed:
  - Removed missing and duplicate records to ensure data integrity.
  - Converted relevant attributes to numeric types and addressed potential outliers.
  - Engineered new features to explore possible predictive relationships, including:
    - `living_to_lot_ratio` = `sqft_living` / `sqft_lot`
    - `bath_per_bed` = `bathrooms` / `bedrooms`
    - `log_sqft_living` = natural logarithm of `sqft_living`, applied to reduce right skewness and improve linearity.
  - The data was subsequently divided into training (80%) and testing (20%) subsets using a fixed random state for reproducibility.

---

## Model Description and Evaluation

A *simple linear regression model* was developed to predict housing prices using `log_sqft_living` as the sole independent variable.
The estimated regression equation is expressed as:

  price^=533,099.06×log⁡(sqft_living)+intercept

Model performance on the test set was evaluated using standard regression metrics:
  - R²: 0.374
  - RMSE: $285,482.72

---

## Interpretation

The model explains approximately *37.4% of the variance* in sale prices based solely on the logarithm of living area. While this represents a *moderate linear relationship*, the relatively high *RMSE* indicates that additional predictors—such as property grade, neighborhood location, or view—would be necessary to improve predictive accuracy.

Overall, this analysis demonstrates that *living area* is a significant, though incomplete, determinant of housing price variation within King County.






