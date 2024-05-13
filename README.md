# Credit Card Fraud Detection Machine Learning Read Me

# Project Overview:

This project focuses on developing a machine learning model for detecting credit card fraud using the PaySim dataset. PaySim is a synthetic dataset simulating mobile money transactions based on real transaction logs from a mobile money service in an African country. The goal is to identify fraudulent transactions within the dataset.

# Dataset Description:

The dataset consists of financial transaction records simulated over a 30-day period, with each step representing one hour of real-world time. Key columns include:

step: A unit of time in hours.

type: Type of transaction (e.g., CASH-IN, CASH-OUT, DEBIT, PAYMENT, TRANSFER).

amount: Amount of the transaction in local currency.

nameOrig: Customer initiating the transaction.

oldbalanceOrg: Initial balance before the transaction for the originating customer.

newbalanceOrig: New balance after the transaction for the originating customer.

nameDest: Recipient of the transaction.

oldbalanceDest: Initial balance before the transaction for the recipient (excluding merchant accounts).

newbalanceDest: New balance after the transaction for the recipient (excluding merchant accounts).

isFraud: Binary indicator of whether the transaction is fraudulent.

isFlaggedFraud: Binary indicator of illegal attempts to transfer more than 200,000 in a single transaction.

# Machine Learning Process:


## Data Preprocessing:

Load the PaySim dataset.

Handle missing values if any.

Encode categorical features (e.g., type) using one-hot encoding.

Cleaning data to prepare for model fitting

Drop irrelevant columns (oldbalanceOrg, newbalanceOrig, oldbalanceDest, newbalanceDest) for fraud detection.

Split the dataset into training and testing sets.


## Exploratory Data Analysis (EDA):

Explore the distribution of the target variable (isFraud) to understand class imbalance.

Visualize the distribution of transaction types.

Investigate the relationship between transaction amount and fraud.

Analyze the correlation between features and the target variable.

Explore any other relevant patterns or anomalies in the data.


## Feature Engineering:

Explore feature correlations and distributions.

Create additional features if necessary (e.g., time-based features).

Scale numerical features if required.

## Model Selection:

Choose appropriate machine learning algorithms for fraud detection (e.g., Logistic Regression, Random Forest, Gradient Boosting).

Train multiple models and compare their performance using cross-validation.

## Model Training:

Train the selected models on the training dataset.

Optimize hyperparameters using techniques like grid search or random search.

## Model Evaluation:

Evaluate the trained models on the testing dataset using metrics such as accuracy, precision, recall, and F1-score.

Analyze the confusion matrix to understand model performance in detecting fraud cases.

## Model Deployment:

Choose the best-performing model based on evaluation metrics.

Serialize the trained model for deployment in production environments.

Integrate the model into a web application or API for real-time fraud detection.
