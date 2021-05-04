# Credit Risk Analysis

Machine learning analysis of credit loan reports

## Overview

The project involves machine learning analysis of a large credit card dataset from LendingClub, a peer-to-peer lending services company. Six different machine learning models were run on the dataset:

* Oversampling
* SMOTE
* Undersampling
* Cambination
* Balanced Random Forest Classifier
* Easy Ensemble AdaBoost Classifier

The performance for predicting credit risk was then compared and evaluated between the different models to assess suitability.

### Purpose

Credit risk is an unbalanced classification problem and we can expect good loans to outnumber riskier loans. We need to determine which models are most suitable for accurately predicting loan risk as providing risky loans is likely to loose the company money. Both Balanced Random Forest and Easy Ensemble classifiers are designed to reduce bias and it will be interesting to see how they compare to the various other models in terms of performance. 

## Resources

Tools and software: Python 3.7.9, Jupyter Notebook 6.1.4, imbalanced-learn and scikit-learn libraries, Visual Studio Code 1.54.3

Dataset: ["LoanStats_2019Q1.csv"](https://github.com/jkenning/Credit_Risk_Analysis/blob/main/Resources/LoanStats_2019Q1.csv)

## Comparison of Machine Learning Model Results

The .csv data file was read and basic cleaning of the data performed. The data was then split into training and testing datasets prior to analyses being performed.

**Oversampling**

![](https://github.com/jkenning/Credit_Risk_Analysis/blob/main/Images/oversampling_class_report.png)

Figure. 1 - Results
* Accuracy  0.65
* Precision 0.99
* Recall    0.70

**SMOTE Oversampling**

![](https://github.com/jkenning/Credit_Risk_Analysis/blob/main/Images/SMOTE_class_report.png)

Figure. 2 - Results
* Accuracy  0.64
* Precision 0.99
* Recall    0.64

**Undersampling**

![](https://github.com/jkenning/Credit_Risk_Analysis/blob/main/Images/undersampling_class_report.png)

Figure. 3 - Results
* Accuracy  0.52
* Precision 0.99
* Recall    0.45

**Combination (Over and Under) Sampling**

![](https://github.com/jkenning/Credit_Risk_Analysis/blob/main/Images/combination_class_report.png)

Figure. 4 - Results
* Accuracy  0.63
* Precision 0.99
* Recall    0.57

**Balanced Random Forest Classifier**

![](https://github.com/jkenning/Credit_Risk_Analysis/blob/main/Images/randomforest_class_report.png)

Figure. 5 - Results
* Accuracy  0.78
* Precision 0.99
* Recall    0.87

**Easy Ensemble AdaBoost Classifier**

![](https://github.com/jkenning/Credit_Risk_Analysis/blob/main/Images/easyensemble_class_report.png)

Figure. 6 - Results
* Accuracy  0.78
* Precision 0.99
* Recall    0.87

## Summary

* The best performing models were the Balanced Random Forest and Easy Ensemble AdaBoost Classifiers, both sharing accuracy and recall values of 0.78 and 0.87 respectively. This suggests that, in general, using models that are designed the elimiate bias may be more suitable for highly unbalanced classifications such as credit card risk.

* There is realtviely little difference in performance between the Oversampling, SMOTE oversampling, and Combination models suggesting these are poor to moderate in their predictions (only about 60-70% accuracy/recall). In the case of credit risk, having a higher number of false positives for risky loans is preferable as these can always be re-checked, however missing risky loans does more damage so this matters a little more as ideally we want that percentage to be low. 30-40% is a lot in this regard for recall. 

* The worst performing is the undersampling model. This may be partially due to the fact that there is already a very low proportion of risky loans compared to good loans, and reduces these occurences in the model data further.

* All the models display high precision rates (0.99) suggesting that they are likely all overfitting the data. Even though the ensemble models were better performing overall they still may not be suitable for predicting credit loan risk.