📊 Xente Credit Scoring – Loan Default Prediction
📌 Project Overview

This project builds a machine learning classification pipeline to predict whether a customer will default on a loan using their historical e-commerce transaction data.

The dataset comes from the Zindi – Standard Bank Tech Impact Challenge (Xente Credit Scoring Challenge).

The goal is to help fintech companies make smarter lending decisions by identifying high-risk customers before issuing loans.

🎯 Problem Statement

Xente provides short-term “Pay Later” loans to customers in Uganda.

The objective is:

Predict whether a customer will default on a loan based on their transaction behavior.

Target Variable

IsDefaulted

1 → Customer defaulted (failed to repay on time)

0 → Customer repaid successfully

This is a binary classification problem.

📂 Dataset Description

The dataset contains:

Customer transaction history

Loan details

Payment history

Loan repayment outcomes

Key features include:

CustomerId

TransactionStartTime

Amount

ProductCategory

ChannelId

AmountLoan

IsDefaulted (Target)

The data is chronologically split into:

Train set

Test set

🔄 Project Pipeline
1️⃣ Problem Definition

Define classification objective

Identify classes

Determine cost of false positives vs false negatives

2️⃣ Data Cleaning

Handle missing values

Remove duplicates

Fix inconsistent formats

Convert date columns

Detect outliers

3️⃣ Exploratory Data Analysis (EDA)

Class imbalance check

Feature distributions

Correlation analysis

Identify anomalies

4️⃣ Feature Engineering

Aggregate customer behavior

Encode categorical variables

Scale numeric features

Remove leakage features

5️⃣ Data Splitting

Train

Validation

Test

6️⃣ Modeling
Baseline Model

Logistic Regression

Advanced Models

Decision Tree

Random Forest

AdaBoost

Ensemble Methods

Voting Classifier (Hard & Soft Voting)

Stacking Classifier

Class imbalance handled using:

class_weight = "balanced"

📈 Model Evaluation

Models were evaluated using:

Confusion Matrix

Accuracy

Precision

Recall

F1-score

ROC-AUC

Since this is a credit scoring problem, Recall and ROC-AUC are more important than Accuracy.

⚖️ Error Consideration

In this business problem:

False Negative (predict non-default but customer defaults)
→ Financial loss (more costly)

Therefore, minimizing False Negatives is important.

🛠️ Technologies Used

Python

Pandas

NumPy

Scikit-learn

Matplotlib / Seaborn

🚀 Future Improvements

Hyperparameter tuning with GridSearchCV

XGBoost / LightGBM implementation

Feature importance analysis

Model calibration

Deployment pipeline

📌 Conclusion

This project demonstrates a complete end-to-end classification pipeline for credit risk modeling, including:

Data preprocessing

Feature engineering

Handling imbalanced data

Ensemble modeling

Model evaluation

The final model aims to support smarter, data-driven lending decisions.
