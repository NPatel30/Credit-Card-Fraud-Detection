# Credit-Card-Fraud-Detection
Uploading one of my old college projects of classic class-imbalance problem.

Imagine a world where every credit card transaction is seamlessly and securely processed. This would mean no more stolen identities, no more fraudulent charges, and no more financial distress for innocent consumers. This story delves into the development of a predictive model that aims to make this vision a reality.


## Understanding the problem 
Credit Card Fraud Detection is a classic class-imbalance problem where the number of fraud transactions is much lesser than the number of legitimate transaction for any bank. Most of the approaches involve building model on such imbalanced data, and thus fails to produce results on real-time new data because of overfitting on training data and a bias towards the majoritarian class of legitimate transactions. Thus, we can see this as an anomaly detection problem.

• What time does the Credit Card Frauds usually take place?

• What are the general trends of amounts for Credit Card Fraud Transactions?

• How do we balance the data to not let the model overfit on legitimate transactions?


## Data Understanding
The Dataset we use is the Kaggle Credit Card Fraud Detection Dataset enlisted in the following link: Link

• The Data has 32 features from V1-V28 which are unknown for confidentiality, TIme, Amount and Class

• The input features are V1-V28, Time and Amount

• The target variable is Class

• The Data does not have any missing values as evident from the below mentioned code, thus need not be handled

• The Data consists of all numerical features, and only the Target Variable Class is a categorical feature.

• Class 0: Legitimate Transaction

• Class 1: Fraud Transaction


## Data Preparation
• The Data does not have any missing values and hence, need not be handled.

• The Data has only Target Variable Class as the categorical variable.

• Remaining Features are numerical and need to be only standardized for comparison after balancing the dataset

• The mean of the amount of money in transactions is 88.34

• The standard deviation of amount of money in transactions is 250.12

• The time is distributed throughout the data equitably and hence, serves as an independent feature

• It is best to not remove or drop any data or features in this case and try to tune the model assuming them as independent features initially


## Conclusion

• The K-Nearest Neighbors Classifier tuned with Grid Search with the best parameter being the Euclidean Distance (p=2) outperforms its counterparts to give a test accuracy of nearly 99.8% and a perfect F1-Score with minimal overfitting

• SMOTE overcomes overfitting by synthetically oversampling minority class labels and is successful to a great degree


## Summary

• All Fraud Transactions occur for an amount below 2500. Thus, the bank can infer clearly that the fraud committers try to commit frauds of smaller amounts to avoid suspicion.

• The fraud transactions are equitable distributed throughout time and there is no clear relationship of time with commiting of fraud.

• The number of fraud transactions are very few comparted to legitimate transactions and it has to be balanced in order for a fair comparison to prevent the model from overfitting.
