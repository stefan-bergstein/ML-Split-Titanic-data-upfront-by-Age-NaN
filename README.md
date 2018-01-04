# Split Titanic data upfront - A simple attempt for separate predictions


---

The Age-feature in the Titanic data is not defined for many passengers. Several good Kaggle notebooks do feature engineering to come up with replacements of the missing age data (e.g. [Titanic Data Science Solutions](https://www.kaggle.com/startupsci/titanic-data-science-solutions/notebook)).

I was wondering if it would be possible to just .... 
1. ** separate the training and test data ** into two buckets (Age defined vs. Age NaN), 
2. do **predictions separately**, and 
3. finally, ** concatenate the results**.


Additionally, the notebook includes basic hyperparameter tuning for RandomForest and AdaBoost.

## Overview:

- Import modules, read data and display some data
- Prepare subset of training and test data without any NaN in Age
- Predict 'Survived' for passengers data with Age
 - Grid search and fit with Random Forest Classifier
 - Grid search and fit with AdaBoost Classifier
 - Predict based on better algorithm and score
- Predict 'Survived' with Random Forest Classifier for passengers data without Age
- Concatenate predictions
- Summary
