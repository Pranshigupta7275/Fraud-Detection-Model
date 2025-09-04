# Financial Fraud Detection Model

A machine learning model to detect fraudulent financial transactions using Python, Pandas, and XGBoost. This project was completed as part of a case study to demonstrate skills in data analysis, feature engineering, and predictive modeling.

## Business Context
The goal of this project is to build a model for a financial company to proactively detect fraudulent transactions, aiming to reduce financial losses while minimizing disruption to legitimate customers.

## Dataset
The dataset used for this project is a synthetic financial dataset from Kaggle, simulating mobile money transactions. It contains over 6 million records and 10 features, including transaction type, amount, and account balances.

## Key Results
The final XGBoost model demonstrated excellent performance on the test set:
* **Recall:** 99.5% (Successfully identified 1,635 out of 1,643 fraudulent transactions)
* **Precision:** 97% (Maintained a very low rate of false alarms)

## Technologies Used
* Python
* Pandas
* Scikit-learn
* XGBoost

* Seaborn & Matplotlib
* ## Visualizations

This section visually summarizes the key data characteristics and the final model's performance.

### Data Exploration

**Target Variable Imbalance**

The dataset is highly imbalanced, with fraudulent transactions making up only ~0.12% of the total data. This presented the primary challenge for the model, as it could easily achieve high accuracy by simply guessing "not fraud". This is why metrics like Recall were critical for evaluation.

![Target Variable Imbalance](images/class_imbalance.png)

**Transaction Amount Distribution**

The transaction `amount` was heavily skewed to the right due to a large number of high-value outliers. Applying a log transformation revealed a more structured, bimodal distribution that is more suitable for analysis and modeling.

![Transaction Amount Distribution](images/amount_distribution.png)

### Model Performance

**Confusion Matrix**

The final model's performance on the unseen test data was excellent. The confusion matrix below shows that the model successfully identified **99.5%** of all fraudulent transactions (1,635 out of 1,643), demonstrating a very high recall rate while keeping false alarms low.

![Confusion Matrix](images/confusion_matrix.png)
