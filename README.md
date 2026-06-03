# Breast Cancer Diagnosis Prediction using Machine Learning

This repository contains a Jupyter Notebook that explores the Wisconsin Diagnostic Breast Cancer dataset and prepares the data for a machine learning classification pipeline.

## Project Overview

- **Goal:** Build a prediction framework for breast cancer diagnosis using 30 cell nucleus features.
- **Dataset:** Wisconsin Diagnostic Breast Cancer (WDBC) from the UCI Machine Learning Repository.
- **Outcome:** Load and inspect the dataset, perform exploratory data analysis, apply dimensionality reduction, and prepare data for model training.

## Notebook

- `20260602_Breast_Cancer_Prediction_ML_Emel_Alpay_v1.ipynb`

## What the notebook covers

1. Data download and loading from the UCI repository
2. Data validation and label encoding
3. Exploratory data analysis with plots
4. Correlation analysis and PCA visualization
5. Train/test splitting with stratification
6. Feature scaling with `StandardScaler`

## Installation

This notebook requires the following Python packages:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `ucimlrepo`

If you are using Anaconda, most of these packages are already installed. To install the missing dataset helper package, run:

```bash
pip install ucimlrepo
```

## Dataset

The notebook downloads the dataset directly from the UCI repository using `ucimlrepo`.

- UCI dataset page: https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic
- Original dataset: Wisconsin Diagnostic Breast Cancer (WDBC)

## Key findings from the notebook

- The dataset contains **569 patients** and **30 numeric features** plus diagnosis labels.
- There are **357 benign** and **212 malignant** cases, which is a slightly imbalanced binary classification task.
- The notebook converts the diagnosis labels to a binary target: `M` → `1` (malignant) and `B` → `0` (benign).
- Exploratory plots show that malignant tumors tend to have larger size-related measurements and more irregular shapes.
- The correlation heatmap reveals strong multicollinearity among size-related features like `radius_mean`, `perimeter_mean`, and `area_mean`.
- PCA shows that the two classes are largely separable in 2 dimensions, suggesting a simple model may perform well.
- The data is split into an **80/20 stratified train/test split** and scaled using `StandardScaler`.

## Next steps

The notebook prepares the dataset and features for supervised learning, but it does not yet train or evaluate classification models. The natural next steps are:

- Train classifiers such as Logistic Regression, K-Nearest Neighbors, SVM, or Random Forest
- Tune hyperparameters and evaluate with cross-validation
- Report metrics like accuracy, precision, recall, and F1-score
- Analyze feature importance and decision boundaries

## References

- Wolberg, W., Mangasarian, O., Street, N., & Street, W. (1993). *Breast Cancer Wisconsin (Diagnostic)* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5DW2B
- UCI Machine Learning Repository — Breast Cancer Wisconsin (Diagnostic) dataset page: https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic
