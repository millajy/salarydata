# Salary Prediction with Regression Models

This project explores how age, education level, work experience, and job type affect salary, and how accurately salary can be predicted from these variables. Three regression models are compared: Linear Regression, Ridge, and Lasso.

## Dataset

[Salary_Data](https://www.kaggle.com/datasets/mohithsairamreddy/salary-data) from Kaggle — 6704 observations, 6 variables (age, gender, education level, job title, years of experience, salary).

Download the CSV and place it in the repo root (or update the path in the notebook) before running.

## Project Structure

```
├── salary_prediction.ipynb   # Main notebook
├── Salary_Data.csv           # Dataset (download from Kaggle)
└── README.md
```

## Methods

- **Data cleaning**: median/mode imputation for missing values, duplicate removal, education level standardization
- **Linear Regression**: baseline model
- **Ridge Regression**: L2 regularization, alpha tuned with cross-validation
- **Lasso Regression**: L1 regularization with feature selection, alpha tuned with cross-validation
- **Evaluation**: MSE and R² on train/test split (75/25)

## Key Findings

Years of experience was the strongest predictor of salary, followed by education level and job category. All three models generalized well (train R² ≈ 0.86, test R² ≈ 0.84), with Ridge and Lasso offering marginal improvements over linear regression. Lasso eliminated some low-impact features entirely.
