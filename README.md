# credit-risk-classification
Module 20 Challenge

## Purpose of the Analysis:
The analysis aims to develop and assess machine learning models for loan risk assessment. Using a dataset from a peer-to-peer lending services company, the goal is to create models that can accurately determine the creditworthiness of borrowers and classify the risk associated with loans.

## Financial Information in the Data:
The dataset includes various financial information, with the primary focus on predicting loan status. Features used for prediction include loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt.

# Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
The first set of variables, with a value of '0' (value count of 75,036), indicates healthy loans. The second set, with a value of '1' (value count of 2,500), suggests loans at a higher risk of default.

# Describe the stages of the machine learning process you went through as part of this analysis.
•	Split the Data into Training and Testing Sets

•	Read the `lending_data.csv` data from the `Resources` folder into a Pandas DataFrame.

•	Create the labels set (`y`)  from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns.

•	Split the data into training and testing datasets by using `train_test_split`.

•	Create a Logistic Regression Model with the Original Data

•	Fit a logistic regression model by using the training data (`X_train` and `y_train`).

•	Step 2: Save the predictions on the testing data labels by using the testing feature data (`X_test`) and the fitted model.

•	Evaluate the model's performance by calculating accuracy scores, confusion matrix, and classification report.

# Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithm).
The methods used are:
•	Logistic Regression model on the original fitted data. 
•	Confusion matrix
•	Classification report

## Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

•	This model performs well in predicting both healthy and high-risk loans, as evidenced by its high accuracy score of 99% and balanced accuracy score of 95%. However, it's important to note that the data is imbalanced, with 96% of the target values (75,036 out of 77,536) representing healthy loans.

•	The model achieves a precision score of 100% for healthy loans and 85% for high-risk loans. This discrepancy can be attributed to the data imbalance. The precision scores indicate that healthy loans were correctly classified as positive 100% of the time, while high-risk loans were correctly classified only 85% of the time.

•	Furthermore, the model achieves a recall score of 99% for healthy loans and 91% for high-risk loans. These scores indicate that 99% of instances where loans were actually healthy were classified correctly, while 91% of instances where loans were actually high-risk were classified correctly.

## Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.

I highly recommend using this model for predicting borrower creditworthiness. With an accuracy rate of over 95% in forecasting the outcome of loan repayments, it can be effectively integrated into a business risk profile. This ensures sufficient capital flow for lenders to remain profitable and sustain their operations.
