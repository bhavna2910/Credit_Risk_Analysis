# Credit_Risk_Analysis
## Overview of Loan Prediction Risk Analysis
 Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. In this project, we want to take a look at how all the factors in our loan_stats csv help predict whether someone is low or high risk status. In this specific project we are using imbalanced-learn and scikit-learn libraries to build models and evalute them using a resampling method. In the first couple of models I oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models I used a combination approach to over and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize bias, balancedrandomforestclassifier and easyensembleclassifier.
 
 ## Results
 1. **Naive Random Oversampling results**:
* Balanced Accuracy: 0.6612700484668286
* Precision: The precision is low for High-risk loans and is high for Low-risk loans.
* Recall: High/Low risk = .66/.67

 2. **SMOTE oversampling results**: 
* Balanced Accuracy: 0.6303296388959394
* Precision: The precision is low for High-risk loans and is high for Low-risk loans.
* Recall: High/Low risk = .62/.64

 3. **Undersampling results**: 
* Balanced Accuracy: 0.6303296388959394
* Precision: The precision is low for High-risk loans and is high for Low-risk loans.
* Recall: High/Low risk = .62/.64

 4. **Combination(over and undersampling) results**:
* Balanced Accuracy: 0.5173713090878325
* Precision: The precision is low for High-risk loans and is high for Low-risk loans.
* Recall: High/Low risk = .70/.57

 5. **Balanced Random Forest Classifier results:** 
* Balanced Accuracy: 0.7877672625306695
* Precision: The precision is low for High-risk loans and is high for Low-risk loans.
* Recall: High/Low risk = .67/.91

 6. **Easy Ensemble AdaBoost Classifier results:** 
* Balanced Accuracy: 0.925427358175101
* Precision: The precision is low for High-risk loans and is high for Low-risk loans.
* Recall: High/Low risk = .91/.94
 
 ## Summary
In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.
