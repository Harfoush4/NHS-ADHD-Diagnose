# ADHD & Sex Prediction Support Tool

This project was developed to support the NHS in building an assistive system for predicting ADHD and biological sex in children and adolescents based on socio-demographic, behavioral, parenting, and fMRI-derived data. The system is designed to address diagnostic biases, especially underdiagnosis of females with ADHD, and complies with GDPR through explainable AI techniques.

## Project Objectives

- Predict ADHD diagnosis from complex multimodal data.
- Predict participant sex, highlighting gender-specific differences.
- Ensure fairness and avoid diagnostic bias, particularly in female subjects.
- Provide model transparency using SHAP explainability.

---

## Dataset Overview

The dataset includes:

- **SDQ scores** (e.g., Hyperactivity, Internalizing/Externalizing)
- **Parenting factors** (e.g., APQ, Barratt scores)
- **Socio-demographic data**

---

## Tools & Libraries

- Python, scikit-learn, XGBoost
- SHAP & LIME for explainability
- Matplotlib, Seaborn for visualization
- Pandas, NumPy for data processing

---

## Models Evaluated

- Random Forest  
- Gradient Boosting  
- Support Vector Machine (SVM)  
- Logistic Regression  
- Neural Network  
- XGBoost

Macro F1-scores were used to evaluate model performance, especially to account for class imbalance.

### Best Models:
- **Sex Prediction:** Logistic Regression (~0.65 macro F1)
- **ADHD Prediction:** XGBoost (~0.75 macro F1)


## Results Summary

- **High ADHD detection accuracy** for both males and females (≥75%)
- **Significant sex prediction bias**: accuracy for female classification dropped below 25%
- SHAP analysis revealed behavioral SDQ scores and parenting data were highly influential features.
- Threshold tuning and class weighting were explored to address fairness concerns.

---

## Explainability (SHAP)

- SHAP summary and decision plots were used to:
  - Understand model feature importance
  - Visualize prediction logic on an individual level
  - Ensure GDPR-compliant transparency for clinical settings

---

## How to use
- using the function created at the end of the notebook (preprocess_and_predict):
    - giving it all the data with or without labels
    - preprocessing is going to happen automaticly and then preditcting the gender and the likelyhood of having ADHD  