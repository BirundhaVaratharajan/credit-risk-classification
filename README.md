# credit-risk-classification

##Purpose of the analysis
In this Challenge, supervised machine learning technique such as logistic regression is used to  train and evaluate a model based on loan risk(helathy risk and high-risk loan).

##financial information and the prediction.
lending_data.csv is used as the dataset , which has the information of historical lending activity from a peer-to-peer lending services company  such as loan_size	interest_rate	borrower_income	debt_to_income	num_of_accounts	derogatory_marks	total_debt.
And using a model  will predict the creditworthiness of borrowers

using  Loan_status as the target variable that we will predict value_counts, accuracy score, the precision score, and recall score

##machine learning process

1.Split the Data into Training and Testing Sets 
2.Create a Logistic Regression Model with original data and resampled data
3.Make a prediction using the testing data
4.generated balanced_accuracy score, confusion matrix and classification report

##Methods
In model 1 logistic regression is used with original data. 
But the the "healthy loans" and "high risk loans" count is  highly imbalanced (75,036, 2,500). 
I split this model into Training and Test sets and generated a Logistic Regression model. I then generated Confusion matrix and  accuracy, precision and recall for both the training and test sets.

For model 2,  resampled data is used and an equal number of 'healthy loans' and 'high risk loans' with which to train my model has been obtained as 56,271 of each type .  split this model into Training and Test sets and generated a Logistic Regression model. I then generated Confusion matrix and  accuracy, precision and recall for both the training and test sets.




##Results
Machine Learning Model 1: 

value counts of Y(Loan_status)
0    75036
1     2500

Balanced accuracy:  0.9520479254722232

Confusion matrix :
 [[18663   102]
 [   56   563]]

Classification report for logistic regression model
               precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
   
weighted avg       0.99      0.99      0.99     19384



* Machine Learning Model 2:
Value count of Loan status
0    56271
1    56271

Balanced accuracy score for resampled data
0.9936781215845847

Confusion matrix for resampled data
 18649   116
 4      615

Classification report for resampled datal
               precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.99      0.91       619

    accuracy                           0.99     19384
   macro avg       0.92      0.99      0.95     19384
   
weighted avg       0.99      0.99      0.99     19384


Summary:
From the result, the second model woul be better ,since it is detecting 'high risk loans' accurately. As high risk loan applicant would fail to repay and it costs more money for loan provider where as loosing a customer is  the minimal cost of misidentifying a 'healthy loan' applicant. The first model is slightly better at identifying 'healthy loan' applicants, but this is less important than correctly identifying 'high risk loan' applicants, which is accomplished better with the second model.


