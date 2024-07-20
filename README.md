# Supervised Machine Learning Loan Risk Evaluation

## Overview of the Analysis

In this assignment, a model was developed to predict loan risk. The financial information used in the model included loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. With this data, the model aimed to predict whether a loan would be healthy or high-risk. The dataset showed a class imbalance, with 75,036 healthy loans compared to 2,500 high-risk loans.

To create the machine learning algorithm, the data was first separated into features (input values) and labels (output values). The dataset was then split into training and testing sets using a random state of 1. A LogisticRegression module was instantiated into a classifier object. The model was trained on the training data, and predictions were made on the testing data. To evaluate the model's performance, a confusion matrix and a classification report were generated.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model Evaluation:
    * Confusion Matrix:
        * 18679 (~96.37%) True Positives
        * 558 (~2.87%) True Negatives
        * 67 (~0.34%) False Negatives
        * 80 (~0.41%) False Positives
    * Classification Report
        * Precision
          * Healthly Loan precision: 1.0
          * High-Risk Loan precision: 0.87
          * The difference in precision values indicate that the model perfectly predicted positive healthy loans while produced some false positive                  values for high-risk loans. 
        * Recall
          * Healthy Loan recall: 1.0
          * High-Risk Loan recall: 0.89
          * The difference in recall values indicates the the model perfectly classified all healthy loans while produces some false negative values              for high-risk loans. 
        * F1 Score
          * When comparing the F1 scores between the two classes there is a decline in values between the healthy loans and high risk loans. This                 corresponds to the precision and recall values for each class.
        * Support
          * There is a large difference in the support values between the healthy loan and high-risk loan classes, indicating class imbalance.
        * Accuracy
          * The overall accuracy value for the model is nearly perfect (0.99), but due to the class imbalance other values should be used to evaluate the model's performance.
        * Macro Average & Wieghted Average
          * The macro average value for this model is 0.94, which better represents the model's performance as it does not account for class imbalance. On the other hand, the weighted average value is 0.99. This weighted average can be misleading, as it tends to favor the majority class.

## Summary

Overall, I believe the model does a fairly good job of predicting healthy loans versus high-risk loans. While the number of false positives and negatives was not zero, both were low, and the precision and recall values for each class were high. In terms of loan risk prediction, this model performs well.

In my opinion, for a bank to stay on the safer side, having more false positive high-risk loans is less of an issue than having false negatives. The greatest flaw in the model is its false negative predictions of high-risk loans. To improve this, the dataset should include more high-risk loan information to address the class imbalance and provide the model with more high-risk loan data to train on.

