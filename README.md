# Heart Disease Prediction Using Optimized Ensemble Learning and Explainable AI

## Overview

This project presents a machine learning-based approach for heart disease prediction using optimized ensemble learning and Explainable Artificial Intelligence (XAI).

The project reproduces and evaluates an ensemble-learning methodology based on Random Forest, AdaBoost, and XGBoost classifiers. Bayesian hyperparameter optimization and five-fold stratified cross-validation are used to improve model selection and evaluation.

SHAP (SHapley Additive exPlanations) is incorporated to explain model predictions at both global and individual levels.

An interactive Streamlit dashboard is also included for model performance analysis, patient-level prediction, dataset information, and explainability.

## Objectives

- Develop machine learning models for heart disease prediction.
- Compare ensemble learning algorithms.
- Optimize model hyperparameters using Bayesian optimization.
- Evaluate models using appropriate classification metrics.
- Select an appropriate decision threshold.
- Explain predictions using SHAP.
- Provide an interactive Streamlit prediction dashboard.

## Models Used

The project evaluates the following ensemble classifiers:

- Random Forest
- AdaBoost
- XGBoost

XGBoost is selected as the best-performing model based on cross-validation performance.

## Datasets

The project supports two datasets:

### Cleveland Heart Disease Dataset

The Cleveland dataset is used for heart disease classification using clinical and demographic features.

### Framingham Heart Study Dataset

The Framingham dataset is additionally used for model evaluation and analysis.

The notebook automatically creates separate project directories for datasets, trained artifacts, results, plots, and SHAP outputs.

## Methodology

The overall workflow is:

```text
Dataset
   ↓
Data Preprocessing
   ↓
Train/Test Split
   ↓
Five-Fold Stratified Cross-Validation
   ↓
Ensemble Model Training
   ↓
Bayesian Hyperparameter Optimization
   ↓
Model Evaluation
   ↓
Decision Threshold Selection
   ↓
SHAP Explainable AI
   ↓
Streamlit Dashboard
```

The notebook uses an 80/20 stratified train-test split and five-fold stratified cross-validation. A fixed random seed is used to improve reproducibility.

## Hyperparameter Optimization

Bayesian optimization is used to search for suitable model hyperparameters.

The notebook uses configurable optimization settings, including:

- Five-fold cross-validation
- Multiple optimization trials
- ROC-AUC-based model selection
- Reproducible random seed

This allows the ensemble models to be evaluated using a consistent experimental procedure.

## Model Evaluation

The project evaluates model performance using multiple classification and probability-quality metrics, including:

- Accuracy
- Sensitivity
- Specificity
- Balanced Accuracy
- ROC-AUC
- Brier Score
- Log Loss

The held-out test set is reserved for final evaluation rather than being used during model optimization.

## Explainable AI

SHAP is used to understand the behaviour of the trained model.

The project provides:

-
