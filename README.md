# Myocardial Infarction Complications

![MI](MI_fig.png)

## Overview

Myocardial infarction (MI) is a major cause of early in-hospital death, often due to complications within 72 hours of admission. 
This project uses a stacked ensemble machine learning approach to predict fatal MI complications by combining multiple algorithms through a meta-learner, 
improving accuracy and robustness over standalone models.


## Dataset

The dataset includes clinical records from 1,700 MI patients treated in Russia between 1992 and 1995, and is publicly available via the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Myocardial+Infarction+Complications). 
The primary outcome is a binary indicator of lethal complications within 72 hours. This dataset is in the Data Folder.


## Methods

The workflow involves cleaning and imputing data, followed by exploratory analysis and feature selection using LASSO and Recursive Feature Elimination. 
Class imbalance is addressed with SMOTE. Six base models are trained with repeated cross-validation and hyper parameter tuning. 
A stacked ensemble is then built using meta-learners to combine base model predictions. 
Parallel processing and fixed random seeds are used to ensure efficiency and reproducibility.


## Key Insights


- Stacked ensemble models, particularly Stacked Random Forest, achieved the highest predictive performance, with strong accuracy (87.7%) and sensitivity (97.4%) on the test set. 
- While individual models like XGBoost and Random Forest performed well in training, they showed lower sensitivity on test data, highlighting potential overfitting. 
- Overall, ensemble stacking significantly improved generalization for detecting early lethal outcomes.
