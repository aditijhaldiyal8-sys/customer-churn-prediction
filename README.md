# Customer Churn Prediction & Analysis

A machine learning project that analyzes customer data to identify patterns associated with bank customer churn and predicts whether a customer is likely to leave.

## Project Overview

Customer churn is an important business problem for banks because retaining existing customers can be more valuable than acquiring new ones.

In this project, customer data is explored to understand factors associated with churn. Exploratory Data Analysis (EDA) is performed to identify patterns across customer age, geography, membership activity, and other features.

Two classification models are then trained:

- Logistic Regression
- Random Forest

The models are evaluated using accuracy, precision, recall, F1-score, and confusion matrices.

## Dataset

The dataset contains 10,000 customer records and includes information such as:

- Credit Score
- Geography
- Gender
- Age
- Tenure
- Balance
- Number of Products
- Credit Card ownership
- Active Membership
- Estimated Salary

### Target Variable

`Exited`

- `0` → Customer stayed
- `1` → Customer churned

## Project Workflow

### 1. Data Cleaning

- Loaded the dataset using Pandas
- Checked dataset dimensions and data types
- Checked for missing values
- Checked for duplicate records
- Removed irrelevant columns such as `RowNumber`, `CustomerId`, and `Surname`

### 2. Exploratory Data Analysis

The project analyzes:

- Overall customer churn distribution
- Churn rate by geography
- Relationship between age and churn
- Relationship between active membership and churn

### 3. Data Preprocessing

- Separated features and target variable
- Applied one-hot encoding to categorical variables
- Split the data into training and testing sets
- Applied feature scaling for Logistic Regression

### 4. Machine Learning Models

#### Logistic Regression

Used as a baseline classification model.

#### Random Forest

Used to capture potentially non-linear relationships between customer characteristics and churn.

### 5. Model Evaluation

Models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

### 6. Feature Importance

Random Forest feature importance is used to identify the features that the model relied on most when making predictions.

## Key Findings

- The dataset contains 10,000 customer records.
- Approximately 20% of customers in the dataset churned.
- Germany had the highest observed churn rate among the three countries.
- Churned customers were generally older than customers who stayed.
- Active members showed a lower observed churn rate than inactive members.
- Random Forest achieved higher test-set performance than Logistic Regression.
- Age had the highest feature importance in the Random Forest model.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Repository Structure

```text
customer-churn-prediction/
│
├── Customer_Churn_Analysis.ipynb
├── Churn_Modelling.csv
├── README.md
├── requirements.txt
└── .gitignore