# Enhancing Particulate Matter Risk Assessment with Novel Machine Learning-Driven Toxicity Threshold Prediction - PM-ToxML

This repository contains the implementation of the **machine learning-based PM toxicity threshold prediction approach** proposed in the paper:

> Enhancing particulate matter risk assessment with novel machine learning-driven toxicity threshold prediction  
> DOI: https://doi.org/10.1016/j.engappai.2024.109531

The objective of this work is to develop a **data-driven predictive model** that classifies tested concentrations of airborne particulate matter (PM) as **toxic or non-toxic**, leveraging physico-chemical and exposure characteristics, with model interpretability provided through eXplainable AI (XAI) techniques.

---

## Main Features

- Data collection, structuring, and preprocessing from multi-source literature
- Exploratory data analysis (EDA) and feature engineering
- Binary classification using five machine learning algorithms
- Handling of imbalanced classification via class weighting
- Hyperparameter optimization using Grid Search Cross-Validation
- Model evaluation with accuracy, precision, recall, F1-score, ROC-AUC, and k-fold cross-validation
- SHAP (SHapley Additive exPlanations) analysis for model interpretability

---

## Machine Learning Models

The following algorithms are implemented and compared:

- Logistic Regression
- Support Vector Classifier (SVC)
- Decision Tree Classifier
- Random Forest Classifier
- XGBoost Classifier

---

## Dataset

The dataset was **manually constructed** from an extensive review of over **40 scientific studies** on particulate matter toxicity, comprising more than **1000 PM samples** and **30+ physico-chemical and exposure characteristics**.

### Physico-chemical characteristics include:
- Aerodynamic diameter class (PM0.1, PM1, PM2.5, PM10)
- Chemical composition (ETM, CARBON, HAP, O-HAP, IONS, WSE, OTHERS)
- Surface chemistry, zeta potential, oxidative potential

### Exposure characteristics include:
- In vitro / In vivo conditions
- Cell type and cell viability test
- Exposure duration and mode (unique or chronic)
- Markers of oxidative stress or inflammation
- Tested concentrations (μg/mL or μg/cm²)

### Target variable:
- **Effect** — Toxic (class 1) or Non-toxic (class 0)

> ⚠️ The dataset is not publicly available by default. It will be made available on request, as stated in the original publication.

---

## Output

The models produce:
- **Binary classification predictions** (toxic / non-toxic) for PM concentrations
- **SHAP beeswarm plots** quantifying the contribution of each feature to model predictions
- **Confusion matrices** and **ROC-AUC curves** for performance comparison across models

Key features consistently identified as most influential: **Composition ETM**, **Composition HAP**, **Concentration**, and **Composition IONS**.

---

## Reference

If you use this code, please cite the original paper:
  doi={10.1016/j.engappai.2024.109531}
}
```
