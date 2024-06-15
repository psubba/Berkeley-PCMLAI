# Practical Application Assignment 17.1 - Comparing Classifiers

## Overview:

In this third practical application assignment, your goal is to compare the performance of the classifiers (k-nearest neighbors, logistic regression, decision trees, and support vector machines) you encountered in this section of the program. You will use a dataset related to the marketing of bank products over the telephone.

The dataset bank-full.csv contains the following columns:

- age - Age of the client.
- job - Type of job.
- marital - Marital status.
- education - Education level.
- default - Has credit in default? (binary: "yes","no")
- balance - Average yearly balance, in euros.
- housing - Has a housing loan? (binary: "yes","no")
- loan - Has a personal loan? (binary: "yes","no")
- contact - Contact communication type.
- day - Last contact day of the month.
- month - Last contact month of the year.
- duration - Last contact duration, in seconds.
- campaign - Number of contacts performed during this campaign and for this client.
- pdays - Number of days that passed by after the client was last contacted from a previous campaign.
- previous - Number of contacts performed before this campaign and for this client.
- poutcome - Outcome of the previous marketing campaign.
- y - Has the client subscribed to a term deposit? (binary: "yes","no")

The data was successfully preprocessed and split into training and testing sets. The shapes of these sets are as follows:

- Training features (X_train_scaled): 36,168 samples, 16 features
- Testing features (X_test_scaled): 9,043 samples, 16 features
- Training labels (y_train): 36,168 samples
- Testing labels (y_test): 9,043 samples

Next, we will build and evaluate the performance of the following classifiers:

- k-Nearest Neighbors (k-NN)
- Logistic Regression
- Decision Trees
- Support Vector Machines (SVM)

We will use accuracy as the primary evaluation metric. Let's start by training and evaluating each classifier.


## Conclusion
All classifiers were successfully trained and evaluated without encountering any errors. The results, including the accuracy and classification reports, are compiled in the provided table.

Here is a summary of the accuracy for each model:

- k-Nearest Neighbors (k-NN): 89.12%
- Logistic Regression: 88.80%
- Decision Tree: 87.37%
- Support Vector Machine (SVM): 89.64%

k-Nearest Neighbors and Logistic Regression both perform well, with accuracies around 89%. However, k-NN has a slightly better recall for the positive class (y=1), indicating it is slightly better at identifying clients who subscribe to a term deposit.

Decision Tree has a slightly lower accuracy at 87.26% but maintains a balance between precision and recall.

Overall, k-NN and Logistic Regression are recommended for this problem due to their higher accuracy and balanced performance.


