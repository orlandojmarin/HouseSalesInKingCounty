# House Sales in King County, USA: Housing Price Prediction

## Overview
This project applies machine learning techniques to predict housing prices in King County, Washington, using historical sales data from 2014–2015.  
The goal is to identify key factors that impact home values and create accurate models to assist in real estate decision-making.

## Goals
- Predict housing prices based on property features and location.
- Identify the most important features influencing house prices.
- Compare the performance of linear and non-linear machine learning models.

## Technologies
Python for data analysis, feature engineering, and modeling.

Key libraries:
- pandas: Data cleaning and manipulation
- numpy: Numerical computations
- matplotlib and seaborn: Data visualization
- scikit-learn: Machine learning (Lasso Regression, KNN Regressor)
- folium: Interactive mapping (property locations)

## Dataset
- **Source**: [House Sales in King County, USA (Kaggle)](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction)
- **Original Size**: 21,613 rows, 21 columns
- **Post-Cleaning Size**: 18,229 rows, 18 columns

Feature Engineering:
- Converted `date` to datetime format.
- Dropped `id`, `zip_code`, `sqft_above`, and `sqft_basement`.
- Removed outliers in `price`, `sqft_lot`, and `bedrooms`.
- Created `has_basement` binary feature.

## Machine Learning Models

### Lasso Regression
- **Purpose**: Linear regression with regularization to prevent overfitting.
- **Results**:
  - R² Score: 0.7011
  - Root Mean Squared Error (RMSE): \$112,313
- **Feature Insights**:
  - Top predictors included `grade`, `sqft_living`, and `latitude`.

### K-Nearest Neighbors (KNN) Regression
- **Purpose**: Non-linear regression to capture more complex patterns.
- **Results**:
  - R² Score: 0.7721
  - Root Mean Squared Error (RMSE): \$98,078
- **Performance**:
  - Outperformed Lasso by better explaining variance and reducing prediction error.

## Results
- **Best Model**: KNN Regression
- **Key Observations**:
  - Homes with better `view`, higher `grade`, and waterfront access are priced higher.
  - Square footage (`sqft_living`) has a strong positive relationship with price.
  - Latitude is more predictive of housing price than longitude, reflecting proximity to Seattle and Bellevue.

## Visualizations
Explore the code for detailed visualizations:
- Histograms of price distributions
- Seasonal trends in home sales
- Folium maps of the most and least expensive homes
- Scatter plots and bar charts for feature relationships
- Residual plots for model evaluation

## Conclusion
This project highlights the role of machine learning in real estate analytics.  
By applying both linear and non-linear models, we gained valuable insights into the factors driving home prices and demonstrated how different modeling techniques capture complex patterns in the data.

---
