# Cirrhosis-Survival-Prediction-Explainable-Machine-Learning-Pipeline
End-to-end machine learning pipeline for cirrhosis survival prediction from data preprocessing to model explainability with SHAP and LIME.


# Cirrhosis Survival Prediction Pipeline

This project builds a complete **machine learning pipeline** to predict survival outcomes in cirrhosis patients.  
It covers the full process — from **data cleaning and transformation** to **modeling, explainability, and validation** — using advanced tools like **SHAP** and **LIME** for transparency and trust.

---

## Overview
Liver cirrhosis is a severe condition that causes progressive liver failure.  
The goal of this project is to create interpretable ML models that classify patients as **Censored (Survived)** or **Death (Event)** using clinical and biochemical data.

---

## Pipeline Structure

| Stage | Notebook | Description |
|--------|-----------|-------------|
| **01** | `01_Data_Import_and_Overview.ipynb` | Loads and cleans the dataset, performs structural overview and sanity checks. |
| **02** | `02_EDA_Log_Transformation.ipynb` | Conducts exploratory data analysis, visualizes outliers, and applies log transformation to skewed features. |
| **03** | `03_Missing_Value_Analysis_and_Imputation.ipynb` | Handles missingness through Mean and MICE (Iterative) imputation, with visual analysis of MCAR and MNAR patterns. |
| **04** | `04_Data_Encoding_and_Visualization.ipynb` | Encodes categorical variables and visualizes correlations and distributions. |
| **05** | `05_SMOTE_Class_Balancing.ipynb` | Applies SMOTE to fix class imbalance between censored and death outcomes. |
| **06** | `06_Baseline_Model_Development.ipynb` | Trains baseline models: Logistic Regression (PCA, LASSO) and Decision Tree. |
| **07** | `07_Random_Forest_and_SHAP_Explainability.ipynb` | Builds a Random Forest classifier and explains predictions using SHAP and LIME. |
| **08** | `08_XGBoost_Advanced_Model_and_Explainability.ipynb` | Develops an advanced XGBoost model with SHAP explainability and calibration analysis. |
| **09** | `09_Cross_Validation_and_Model_Comparison.ipynb` | Performs 5-fold cross-validation, compares models, and visualizes accuracy results. |

---

## Key Features
- **Comprehensive preprocessing:** cleaning, transformation, and missing-value handling.  
- **SMOTE balancing:** resolves class imbalance for fairer learning.  
- **Modeling:** Logistic Regression, Decision Tree, Random Forest, and XGBoost.  
- **Evaluation:** Accuracy, Precision, Recall, F1, and ROC-AUC.  
- **Explainability:** SHAP & LIME visualizations for global and local model interpretation.  
- **Cross-Validation:** Stratified 5-fold testing for robust performance estimation.

---

## Explainable AI Highlights
- **SHAP Summary Plots** show the most influential predictors globally.  
- **SHAP Force Plots** and **LIME Explanations** reveal how individual features affect each prediction.  
- Provides interpretability crucial for **clinical decision support** and ethical AI.

---

## Folder Structure
Classification_Project/
│
├── data/
│ ├── 01_cleaned_cirrhosis.csv
│ ├── 02_log_transformed_cirrhosis.csv
│ ├── 03_cirrhosis_imputed.csv
│ └── cirrhosis_balanced.csv
│
├── results/
│ ├── 02_log_transform_comparison.png
│ ├── 03_after_MICE_imputation.png
│ ├── 07_RF_SHAP_summary.png
│ ├── 08_XGB_SHAP_summary.png
│ └── 09_CV_Model_Comparison.png
│
└── notebooks/
├── 01_Data_Import_and_Overview.ipynb
├── 02_EDA_Log_Transformation.ipynb
├── ...
└── 09_Cross_Validation_and_Model_Comparison.ipynb
