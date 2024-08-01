# Credit Card Fraud Detection

## Dependencies

Libraries used are likely standard.\
xgboost: https://xgboost.readthedocs.io/en/stable/install.html#conda \
imbalanced-learn (for oversampling): https://imbalanced-learn.org/stable/install.html
Dataset: https://www.kaggle.com/datasets/dhanushnarayananr/credit-card-fraud/data


## Introduction

In today's digital economy, credit card fraud poses a significant threat to consumers, financial institutions, and the global financial system. As e-commerce continues to grow exponentially, so does the sophistication and frequency of fraudulent activities. A lot of money is lost due to credit card fraud. This calls for the urgent need for robust predictive models that can effectively identify and mitigate fraudulent transactions in real time. 

Being able to deploy an automatic machine to determine the validity of a transaction is beneficial for any organization that deals with online transactions. Sophisticated models such as XGBoost can discover obscure features that indicate fraud that humans have no chance of doing manually. 

Effective fraud detection safeguards consumers' financial assets and helps maintain trust in digital payment systems. This is crucial for the growth of e-commerce and online banking, which are integral to modern economies.



## Data Preprocessing

- There were no null values, so no imputation required.
- The `fraud` class is unbalanced, (only 8.7% are fraudulent). Therefore, I will use a metric that emphasizes recall (likely F2 score) to minimize false negatives.
- Some features have extreme outliers (skewed right), so I will normalize with MinMaxScaler (removing outliers not an option). The other columns are binary, so they are unaffected.
- I will stratify split based on the fraud class to keep the same distribution of fraud in my training and test set.

## Training first model

- I picked RandomForestClassifer with a moderate 25 trees. The metrics were abnormally high, both for the training and testing set.
- I will consider some other models to compare to random forest.



