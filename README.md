# Credit_Risk_Analysis
## Overview

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. This project is intended to build and evaluate models using resampling to predict credit risk.

In this way, credit risk is very tough to predict. In this project we want to take a look at how all the factors in our loan_stats csv help predict whether someone is low or high risk status. One method that data scientists use for this type of issue is creating a model and then evaluate and train the models that they create. In this specific project it is used imbalanced-learn and scikit-learn libraries to build models and evalute them using a resampling method. In the first couple of models it is oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models it is used a combination approach to over and undersample the data using smoteenn. Finally, it is compared two machine learning models that minimize bias, balancedrandomforestclassifier and easyensembleclassifier.

This project leverages the following libraries:

imbalanced-learn
scikit-learn
Six models were used:

Random Oversampling
SMOTE Oversampling
ClusterCentroids Resampler
SMOTEENN Combination Sampling
Balanced Random Forest Classifier
Easy Ensemble Classifier


## Summary

In the first four models it was deployed an undersampled, oversampled and a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next two models it was resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In the first four models the accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in the models it is desired want a good balance of recall and precision which is why it is recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.

Here is a summary of the results:



## Recomendations

After reviewing the above summary table, the following observations can be derived:

The Accuracy of the (4) sampling methods is subpar to that of the (2) classification methods.
Precision is consistent with identifying Low Risk but is not great at High Risk across all (6) models.
Out of all of the models, Easy Ensemble Classifier performed the best Recall for identifying the High Risk borrowers.
Considering the observations, the Easy Ensemble Classifier method is the best performing. Additional tuning with this model could address the low precision rate for high risk borrowers.

