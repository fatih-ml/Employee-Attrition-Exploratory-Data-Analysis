# Deciphering Employee Attrition: An Exploratory Data Analysis on HR Dataset

## Overview
This repository contains an in-depth exploratory data analysis (EDA) of a fictional Human Resources dataset. The primary goal of this analysis is to gain valuable insights into employee attrition and related factors. The dataset, provided by IBM and presented in a Kaggle competition, consists of 2795 observations and 35 features, encompassing various aspects of employees' professional and personal lives.

## Dataset
The dataset is divided almost equally into test and train datasets, forming a binary classification type dataset. The target variable is 'Attrition', which indicates whether an employee stays or leaves the company.

## Key Findings
**No Missing Values:** The dataset was clean with no missing values.

**Outlier Handling:** Outliers were identified and appropriately addressed in the 'DailyRate', 'Education', and 'JobLevel' features.

**High/Low Cardinality Issues:** Columns like 'Over18', 'EmployeeCount', and 'StandardHours' were removed due to either having only one value or lacking diversity. The 'id' column was also dropped.

**Feature Importance:** Stock option level, age, job involvement, monthly income, and total working years were identified as the top features impacting attrition.

## Attrition Classes Analysis:
**Travel Frequency:** Employees who frequently travel have a significantly higher attrition rate compared to non-travelers.
**Marital Status:** Singles show a higher attrition rate compared to married and divorced employees.
**Gender:** Male employees exhibit a higher attrition rate compared to females.
**Work-Life Balance:** Employees with very low work-life balance tend to have higher attrition rates.
**Numerical Variables Analysis:** Employees who leave the company tend to have spent significantly fewer years in their current role, with their current manager, and in the company overall.
**Encoding and Collinearity:** Categorical variables were appropriately encoded. Multicollinearity was checked using Variance Inflation Factor (VIF) and correlations, leading to feature selection.

## Feature Selection
Based on the analysis, remaining features were selected for the model after dropping these:

* 'PercentSalaryHike' over 'PerformanceRating'
* 'TotalWorkingYears' over 'YearsAtCompany', 'YearsInCurrentRole', 'YearsSinceLastPromotion', 'YearsWithCurrManager'
* 'MonthlyIncome' over 'JobLevel'
* 'JobRole' over 'Department Features'
* Retained encoded features.

## Model Building
Classifiers like Decision Trees, Random Forest, XGBoost, and Gradient Boosting will be employed for the predictive model, utilizing the selected features.

## Dependencies
Python 3.6+
Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

## Usage
Clone the repository.
Install the necessary dependencies.
Run the Jupyter notebook.
