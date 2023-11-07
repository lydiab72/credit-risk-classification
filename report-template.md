# Module 12 Report Template

## Overview of the Analysis

Credit risk poses a problem for any financial institute. This could be for a number of reasons, but in this analysis it is the result of there being an uneven, or imbalanced, count of healthy loans (low-risk) outnumbering non-healthy loans (high-risk). Two techinques were used to train and evaluate imblananed loans. The dataset used is of historical lending activity from a peer reviewed lending service company to help build a model that can identify the credit score of those trying to seek a loan.

This exercises uses a logistic regression model to compare two versions of the dataset. The first verison is the orginial dataset and the second is a resample of the data by using the RandomOverSampler module.

Both models will be gathering the count of target classes, train a logistic regression model, calcuate the balance accuracy score, generate a confusion matrix, and generate a classification report.

## Results

Below will analyze both models.

* Machine Learning Model 1:
  * The Logistic Regression model fitted with the Imbalanced DataSet predicted healthy loans 100% of the time and predicted non-healthy loans 85% of the time.
 
  * The model fitted with imbalanced data has a higher possibility of making the following mistakes:
   * a low-risk loan is classified as a high-risk loan.
   * a high-risk loan is classified as a low-risk loan.
     
According to the models recall scores, the model made 1% of mistakes when predicting healthy loans and made 9% of mistakes when predicted non-healthy loans.

![image](https://github.com/lydiab72/credit-risk-classification/assets/132516418/e79e1218-ac8a-4f68-aa58-2c5a0eac0151)

The model generated an accuracy score of 95% but could be improved due to the dataset being imbalanced.

![image](https://github.com/lydiab72/credit-risk-classification/assets/132516418/0adf9ae2-6613-4783-b197-d37cd5bfc6bf)


* Machine Learning Model 2:
  * The Logistic Regression model fitted with the OverSampled DataSet predicted healthy loans 100% of the time and predicted non-healthy loans 84% of the time.
 
  * The model fitted with balanced (oversampled) data has a much lower possibility of making these mistakes:
   * a low-risk loan is classified as a high-risk loan.
   * a high-risk loan is classified as a low-risk loan.

According to the models recall scores, the model made 1% of mistakes when predicting healthy loans and made 1% of mistakes when predicted non-healthy loans.

![image](https://github.com/lydiab72/credit-risk-classification/assets/132516418/159aff27-60f1-4185-84c2-a277760a7798)

The model generated an accuracy score of 99% due to the dataset being balanced.

![image](https://github.com/lydiab72/credit-risk-classification/assets/132516418/21526800-9b09-40ff-85bf-a7b3383da6a1)


## Summary

A lending company may want a model that requires classifying a low-risk and high-rsik loans correctly a majority of the time.

For example, a low-risk loan being identified as a high-risk loan may be more costly for a lending company since it could cause a loss of customers. Alternatively, a high-risk loan can also be costly, if identified as a low-risk loan, due to the loss of funds being provided by the lending company. It gives the perception to the company that this customer is trustworthy and will pay back the loan.

Overall, the logistic regressional model with the OverSampled data performed much better than the fitted model with the imbalanced data due to the data being more balanced and generating a higher accuracy score, higher recall. This indicates the model will make fewer mistakes when identifying high-risk loans. The lending company would likely make far less false-positives due to the greater possibility of a lender losing provided funds when falsely identifying high-risk loans as low-risk. 

Model fitted with Imbalanced Data:

 * 56 (FALSE POSITIVES) --> The actual value is healthy and the predicted value is non-healthy

 * 102 (FALSE NEGATIVES) --> The actual value is non-healthy and the predicted value is healthy


Model fitted with Balanced Data:

 * 4 (FALSE POSITIVES) --> The actual value is healthy and the predicted value is non-healthy

 * 116 (FALSE NEGATIVES) --> The actual value is non-healthy and the predicted value is healthy

This matrix shows the number of false-positive results decreased, indicating the model was able to classify each risk type of a loan correctly. In conclusion, model 2 is the recommend model for identifying low or high risk loans.
