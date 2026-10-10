# Customer-churn-analysis-and-prediction-using-R

## Project Overview

This project uses the IBM Telco Customer Churn dataset to investigate factors associated with customer churn and build a predictive classification model using R.

The project combines statistical hypothesis testing with logistic regression modelling and model evaluation.

## R Script

Main script:

`week3_churn_analysis.R`

The script performs:

- Data loading and cleaning
- Missing-value handling
- Exploratory statistics
- Welch two-sample t-tests
- Chi-square testing
- Train-test splitting
- Logistic regression modelling
- Churn probability prediction
- Confusion matrix analysis
- Performance metric calculation
- ROC curve analysis
- AUC calculation
- Classification threshold optimization

## Dataset Source

IBM Telco Customer Churn dataset.

Important variables include:

- tenure
- Contract
- InternetService
- PaymentMethod
- MonthlyCharges
- TotalCharges
- Churn

The original dataset contains 7,043 customers.

After removing 11 records with missing TotalCharges values, 7,032 customer records are used for analysis.

## Usage

Place:

`WA_Fn-UseC_-Telco-Customer-Churn.csv`

inside the project folder.

Install and load the required packages, then run:

source("week3_churn_analysis.R")

## Required R Packages

install.packages("ggplot2")
install.packages("pROC")

Required libraries:

library(ggplot2)
library(pROC)

The modelling and statistical testing primarily use Base R functions.

## Important Output Charts

- Monthly Charges by Churn Status boxplot
- Churn Proportion by Contract Type
- Customer Tenure by Churn Status boxplot
- ROC Curve for Logistic Regression

Important model outputs also include:

- Confusion matrix
- Accuracy
- Precision
- Recall
- Specificity
- F1 Score
- ROC-AUC

## Expected Results

Hypothesis testing should show that:

- Churned customers have higher monthly charges.
- Contract type is significantly associated with churn.
- Churned customers have shorter tenure.

The logistic regression model should produce approximately:

Default 0.50 threshold:

- Accuracy: 81.1%
- Precision: 67.5%
- Recall: 51.9%
- Specificity: 91.3%
- F1 Score: 58.7%

Optimized 0.40 threshold:

- Accuracy: 80.0%
- Precision: 60.5%
- Recall: 64.8%
- Specificity: 85.2%
- F1 Score: 62.6%

ROC-AUC:

0.8477

The 0.40 classification threshold is preferred because it detects more customers who are actually likely to churn.

## Author

Suhas D
