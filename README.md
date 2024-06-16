# House Price Prediction

## Overview

This project aims to predict house prices using various machine learning models. The dataset includes several features such as the number of bedrooms, whether the house is under construction, and the square footage. We will explore and compare the performance of three different models: Linear Regression, Decision Tree Regressor, and Random Forest Regressor.

## Dataset Description

The dataset contains the following features:

- **POSTED_BY**: The entity that posted the listing (Owner, Agent, Builder)
- **UNDER_CONSTRUCTION**: Whether the property is under construction (Yes/No)
- **RERA**: RERA compliance (Yes/No)
- **BHK_NO.**: Number of bedrooms
- **BHK_OR_RK**: BHK (Bedroom, Hall, Kitchen) or RK (Room, Kitchen)
- **SQUARE_FT**: Area in square feet
- **READY_TO_MOVE**: Whether the property is ready to move (Yes/No)
- **RESALE**: Whether the property is a resale (Yes/No)
- **ADDRESS**: The address of the property
- **LONGITUDE**: Longitude of the property
- **LATITUDE**: Latitude of the property
- **TARGET (PRICE_IN_LACS)**: The target variable, price in lakhs

## Models Used

### 1. Linear Regression

**Linear Regression** is a basic and widely used type of predictive analysis. It assumes a linear relationship between the input variables (X) and the single output variable (Y). In this project, Linear Regression was used as a baseline model.

**Advantages**:
- Simple to implement and understand
- Computationally efficient

**Disadvantages**:
- Assumes a linear relationship between features and target
- Sensitive to outliers

### 2. Decision Tree Regressor

**Decision Tree Regressor** is a non-linear model that splits the data into subsets based on the value of input features. It builds a tree-like model of decisions and their possible consequences.

**Advantages**:
- Captures non-linear relationships
- Easy to visualize and interpret
- Handles both numerical and categorical data

**Disadvantages**:
- Prone to overfitting
- Sensitive to small variations in data

### 3. Random Forest Regressor

**Random Forest Regressor** is an ensemble method that uses multiple decision trees to improve the accuracy and robustness of the model. It reduces overfitting by averaging the results of multiple trees.

**Advantages**:
- Reduces overfitting
- Handles non-linear relationships
- More accurate and stable than individual decision trees

**Disadvantages**:
- More complex and computationally intensive
- Less interpretable than a single decision tree

## Results

| Model                 | RMSE           | R-squared      |
|-----------------------|----------------|----------------|
| Linear Regression     | 600.84         | 0.1633         |
| Decision Tree Regressor| 8.72           | 0.9998         |
| Random Forest Regressor| 8.72           | 0.9998         |

## Conclusion

- **Linear Regression**: The model performed poorly with a high RMSE of 600.84 and a low R-squared value of 0.1633, indicating that it does not fit the data well.
- **Decision Tree Regressor**: This model showed excellent performance with an RMSE of 8.72 and an R-squared value of 0.9998. However, it is prone to overfitting.
- **Random Forest Regressor**: The Random Forest model achieved the same performance metrics as the Decision Tree Regressor, with an RMSE of 8.72 and an R-squared value of 0.9998. It provides better generalization and robustness compared to a single decision tree.

In summary, while both Decision Tree and Random Forest Regressors performed exceptionally well, the Random Forest Regressor is preferred due to its ability to generalize better and reduce the risk of overfitting.

## Usage

To run the models and predict house prices, follow these steps:

1. Load the dataset.
2. Preprocess the data (handle missing values, encode categorical variables, etc.).
3. Split the dataset into training and testing sets.
4. Train the models using the training set.
5. Evaluate the models using the testing set.
6. Compare the performance of the models and choose the best one.
