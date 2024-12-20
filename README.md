# breastCancer-predictions-analysis
## Overview
This project consists of the analysis of Breast Cancer dataset and exploration of different machine learning models for predictions of diagnosis of tumors based on tumor cells characteristics. The problem in hand is a Classification task, identifying a tumor as Malign (1) or Benign (0).

The dataset used for this project is a copy of UCI ML Breast Cancer Wisconsin (Diagnostic) dataset which is publicly available through sklearn datasets ([Sklearn Breast Cancer Dataset](https://scikit-learn.org/1.5/modules/generated/sklearn.datasets.load_breast_cancer.html)).

The models explored in this project include Random Forest, Logistic Regression, Neural Networks and Support Vector Machine classifiers.

This project structure is inspired in the CRISP-DM Framework.

## Report Sections
- Data Understanding -> this section presents an exploratory analysis on the given business data.
- Data Preparation -> this section includes data cleaning steps, as well as dataset split into train, validate and test subsets.
- Modelling -> this section includes the application of different modelling techniques and comparison across models with the purpose to find the most suitable model for the given task.
- Evaluation -> this section shows final results of chosen model into test data and reflections.

## Results
The Logistic Regression model with hyperparameter configuration as {'C': 206.913808111479, 'penalty': 'l1', 'solver': 'liblinear'} achieved 95.9% *Accuracy* in the test dataset, with *Recall* at 96% and *Precision* at 95%.

For cancer diagnosis, False Positives result in doctors further testing patients who don't have a malign tumor, while False Negatives can result in doctors dismissing a patient who has a malign tumor and needs further testing and treatment. Both risks should be controlled and keep to a minimum, however the occurence of False Positives is more acceptable in this scenario than the occurence of False Negatives. Based on this evaluation, the model's False Negative Rate (probability of a true positive being missed by the test) has been monitored during this project, with the selected model achieving *False Negative Rate* of 3.7%.
