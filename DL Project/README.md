# Credit Card Fraud Detection

## Overview

The dataset contains transactions made by credit cards in September 2013 by European cardholders.This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

## Objective

The objective is use a Deep Learning (Artificial Neural Network) algorithm to detect whether the transaction is fraud or not and also handling imbalance dataset.So that customers are not charged for items that they did not purchase. 
  
## Data Exploration

### Data
Due to confidentiality issues, we don't have the original features and more background information about the data.

* There are 30 features out of which 28 features (V1, V2, ... V28) are numerical input variables resulting from a PCA transformation. The other two features, 'Amount' and 'Time,' are not PCA transformed.

* Feature 'Time' holds the seconds elapsed between each transaction and the first transaction in the dataset.

* Feature 'Class' is the target variable that takes value 1 in fraudulent transactions and 0 otherwise.

Dataset can be downloaded from ( https://www.kaggle.com/mlg-ulb/creditcardfraud )

### Data Imbalance

It is evident from the below plot that data is highly imbalanced. The dataset has only 492 fraudulent transactions out of a total of 284,807 transactions, which is a mere 0.17%.

![imbalance](https://user-images.githubusercontent.com/73767113/145210985-66ee4bb3-790d-457b-9f5c-7366c2cab1e5.jpg)

## Problem with imbalance data

Feeding imbalanced data to your classifier can make it biased in favor of the majority class, simply because it did not have enough data to learn about the minority.

## SAMPLING Techniques to handle imbalance data:
Sampling is a process used in statistical analysis in which a predetermined number of observations are taken from a larger population.In Sampling ,i have implemented following three techniques to handle imbalance dataset:

1.UNDER SAMPLING:

In undersampling, we balance uneven dataset by keeping minority class as it is and decreasing the size of majority class to minority class.

![undersampling](https://user-images.githubusercontent.com/73767113/145209185-2619d991-0725-46e3-abda-1642e7f30087.jpg)

2.OVER SAMPLING:

In oversampling, we balance uneven dataset by creating duplicate data in minority class to equalize to size of majority class.

![Oversampling](https://user-images.githubusercontent.com/73767113/145209227-c687e536-453a-4d99-a792-7053e4ca81aa.jpg)

3.SMOTE(Synthetic Minority Over-sampling Technique):

In SMOTE, we balance uneven dataset by creating new synthetic data in minority class to equalize to size of majority class.

![Smote](https://user-images.githubusercontent.com/73767113/145209254-84b81a38-3991-4f59-86a6-68d05d2055b7.jpg)

## Results

1.UNDER SAMPLING

![undersampling_result](https://user-images.githubusercontent.com/73767113/145209328-1fee8c40-4af5-43e9-a4d5-7d148fc366d5.jpg)

2.OVER SAMPLING

![oversampling_result](https://user-images.githubusercontent.com/73767113/145209370-62d972b5-5cde-4634-846f-d9108c8cc8c4.jpg)

3.SMOTE

![smote_result](https://user-images.githubusercontent.com/73767113/145209483-76116387-b885-4623-9931-ecd6f8ef6b2f.jpg)

## Conclusion
One might argue that the reduced accuracy is an indicator of lower model performance. However, this is not true.

Error in prediction can be made in two ways:


1.   Classifying not fraud as fraud

2.   Classifying fraud as not fraud


It should not be hard to understand that the second error is costlier than the first.

The objective of each classification problem is different. So make sure to evaluate each model with respect to its own objective instead of merely judging it on its accuracy.
