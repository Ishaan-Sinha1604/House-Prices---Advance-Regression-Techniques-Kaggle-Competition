# House-Prices---Advance-Regression-Techniques-Kaggle-Competition
This competition challenges you to predict the final price of each home based on its features such as size, location, the material used, etc.

---
## Overview
The objective of this project was to develop a robust regression model to predict house prices based on 79 explanatory variables such as location, condition, quality, and size. The dataset was sourced from Kaggle's [House Prices: Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques).

---
## Repository Structure
```
├── Data_clean_test_new_code.txt                # Contains code for running the model on test dataset
├── Data_clean_train_new_code.txt               # Contains code for building the model
└── MMA867_TeamAssignment_Consolidated.pdf      # Project Report
└── README.md                                   # Summary of the Project
└── data_description.txt                        # Contains descriptions of all the features in the dataset
└── test.csv                                    # Testing dataset
└── train.csv                                   # Training dataset
```
---
## Tech Stack
- **Language**: R
- **Libraries**: tidyverse(Data manipulation and visualization), car(Diagnostic tools for regression models), fastDummies(encoding for categorical variables), corrplot(Correlation matrix visualizations), psych(Descriptive statistics), lares(Feature importance and model interpretation), caTools(Data splitting and performance metrics), glmnet(LASSO and Ridge Regression)\
- **Data Source**: Kaggle

---
## Features and Approach
### Data Preprocessing
- **Feature engineering**: Derived variables such as `Age`, `GarageAge`, `AgeRemodAdd`, `AgeSold`.
- **Variable transformation**: Applied log, square root, and interaction terms to improve linear fit.
- **Encoding**: Used `fastDummies` to convert categorical features.

### Modeling
- **Models Built**: Multiple Linear Regression, **LASSO Regression** using `glmnet` (α = 1), **Ridge Regression** using `glmnet` (α = 0)
- **Model selection**: Used cross-validation to choose optimal lambda values.

---
## Results
- Models were evaluated using **Mean Squared Error (MSE)** on the test set. Final RMSE = 0.13
- LASSO and Ridge both produced strong generalization, with LASSO providing better feature selection.

---
## Key Learnings
- Regularization helps in reducing overfitting and improves generalization.
- LASSO tends to perform better when there are small number of significant features and the remaining features have coefficients close to 0.

---
