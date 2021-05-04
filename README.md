# Credit Risk Analysis

Machine learning analysis of credit card loan reports

## Overview

The project involves machine learning analysis of a large credit card dataset from LendingClub, a peer-to=peer lending services company. Six different machine learning models were run on the dataset:

* Oversampling
* SMOTE
* Undersampling
* Cambination
* Balanced Random Forest Classifier
* Easy Ensemble AdaBoost Classifier

The performance for predicting credit card risk was then compared and evaluated between the different models to assess suitability.

### Purpose

Credit risk is an unbalanced classification problem and we can expect good loans to outnumber riskier loans. We need to determine which models are most suitable for accurately predicting loan risk as providing risky loans is likely to loose the company money. Both Balanced Random Forest and Easy Ensemble classifiers are designed to reduce bias and it will be interesting to see how they compare to the various other models in terms of performance. 

## Resources

Tools and software: Python 3.7.9, Jupyter Notebook 6.1.4, imbalanced-learn and scikit-learn libraries, Visual Studio Code 1.54.3

Dataset: ["LoanStats_2019Q1.csv"]()

## Comparison of Machine Learning Model Results

The .csv data file was read and basic cleaning of the data performed. The data was then split into training and testing datasets prior to analyses being performed.

**Oversampling**

![]()

Figure. 1 - Results
* Accuracy  0.65
* Precision 0.99
* Recall    0.70

**SMOTE Oversampling**

![]()

Figure. 2 - Results
* Accuracy  0.64
* Precision 0.99
* Recall    0.64

**Undersampling**

![]()

Figure. 3 - Results
* Accuracy  0.52
* Precision 0.99
* Recall    0.45

**Combination (Over and Under) Sampling**

![]()

Figure. 4 - Results
* Accuracy  0.63
* Precision 0.99
* Recall    0.57

**Balanced Random Forest Classifier**

![]()

Figure. 5 - Results
* Accuracy  0.78
* Precision 0.99
* Recall    0.87

**Easy Ensemble AdaBoost Classifier**

![]()

Figure. 6 - Results
* Accuracy  0.78
* Precision 0.99
* Recall    0.87

