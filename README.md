# Mental Health Depression Prediction — Machine Learning Assignment

## Overview

This project implements a complete machine learning pipeline for **binary classification of depression** using a mental health survey dataset.

The analysis follows a rigorous experimental workflow covering:

* Exploratory Data Analysis (EDA)
* Data cleaning and missing-value analysis
* Feature engineering and preprocessing
* Cross-validation and hyperparameter tuning
* Multiple classification models
* Class-imbalance analysis
* Model comparison and evaluation
* Model interpretation
* Limitations and reproducibility

The target variable is **`Depression`**, formulated as a binary classification problem.

> **Note:** This project is an academic machine learning analysis. The resulting model is not a clinical diagnostic tool, and predictive associations should not be interpreted as causal relationships.

---

## Repository Contents

| File                   | Description                                                                                             |
| ---------------------- | ------------------------------------------------------------------------------------------------------- |
| `ML-Assignment2.ipynb` | Complete Jupyter Notebook containing the analysis, code, visualizations, model training, and evaluation |
| `train.csv`            | Dataset used for the analysis                                                                           |
| `Assignment-2.pdf`     | Technical report containing the detailed methodology, results, interpretation, and discussion           |

---

## Dataset

The dataset contains information about individuals':

* Demographic characteristics
* Academic and professional status
* Lifestyle habits
* Academic/work pressure
* Satisfaction levels
* CGPA
* Mental-health-related background
* Depression status

The analysis considers both numerical and categorical variables and examines their relationship with the target variable.

---

## Project Workflow

### Phase I — Exploratory Data Analysis

The EDA investigates:

* Dataset size and structure
* Data types
* Descriptive statistics
* Missing values and missingness patterns
* Distribution of the `Depression` target
* Class imbalance
* Numerical-variable distributions
* Outliers and anomalies
* Relationships between numerical variables
* Depression rates across categorical variables
* Rare categorical levels
* Differences between depressed and non-depressed groups

Visualizations are accompanied by analytical interpretations rather than being presented without context.

---

### Phase II — Data Preprocessing

The preprocessing pipeline includes:

* Removing non-informative variables such as `id` and `Name`
* Handling missing values
* Accounting for conditional missingness
* Encoding categorical variables
* Scaling numerical variables where required
* Preserving potentially informative missingness patterns

Because students and working professionals may have different available variables, subgroup-aware imputation and/or missingness indicators are considered where appropriate.

All preprocessing steps are designed to avoid data leakage.

---

### Phase III — Predictive Modeling

The task is formulated as a binary classification problem with:

**Target:** `Depression`

A baseline classifier is included using a majority-class strategy to establish a minimum performance reference.

Multiple supervised learning approaches are compared, including models from at least three different families, such as:

* Logistic Regression
* Linear/Quadratic Discriminant Analysis
* Decision Tree
* Random Forest
* Boosting models
* Linear SVM
* Kernel SVM

Model selection and hyperparameter tuning are performed using cross-validation.

Preprocessing operations such as imputation, encoding, and scaling are performed within the cross-validation pipeline to prevent information leakage.

---

## Evaluation

Model performance is evaluated using multiple metrics rather than accuracy alone:

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC
* Confusion Matrix
* Training Time

Special attention is given to **recall for the Depression class**, since false negatives may be particularly important in this type of prediction problem.

The analysis also discusses:

* Class imbalance
* Precision–recall trade-offs
* Threshold selection
* False positives and false negatives
* Computational cost

---

## Model Comparison

All selected models are compared using a common evaluation framework.

The comparison considers:

| Metric        | Purpose                                   |
| ------------- | ----------------------------------------- |
| Accuracy      | Overall proportion of correct predictions |
| Precision     | Reliability of positive predictions       |
| Recall        | Ability to identify positive cases        |
| F1-score      | Balance between precision and recall      |
| ROC-AUC       | Ranking/discrimination performance        |
| Training Time | Computational cost                        |

Model selection is based on the overall empirical evidence rather than a single metric.

---

## Model Interpretation

The final model is interpreted to identify important predictors of depression.

Depending on the selected models, interpretation includes comparisons such as:

* Logistic Regression coefficients
* Tree-based feature importance
* Differences between linear and nonlinear models

Linear models primarily capture additive relationships, while tree-based models can capture nonlinear relationships and interactions. Differences in feature importance between model families are therefore discussed.

---

## Reproducibility

The notebook is structured as a reproducible scientific workflow:

1. Data loading
2. Data inspection
3. Exploratory Data Analysis
4. Data cleaning
5. Feature engineering
6. Train/test split
7. Preprocessing pipeline
8. Cross-validation
9. Hyperparameter tuning
10. Model training
11. Model evaluation
12. Model comparison
13. Final model interpretation

A fixed random seed is used where appropriate to improve reproducibility.

---

## Limitations

Several limitations should be considered when interpreting the results:

* Missing values may introduce uncertainty.
* Survey data can contain noisy or subjective responses.
* Class imbalance can affect model performance.
* Categorical variables may contain rare or inconsistent categories.
* Survey-based datasets may contain sampling or response bias.
* Predictive association does not imply causation.
* Model performance depends on the available dataset and may not generalize to other populations.
* The model should **not** be interpreted as a clinical diagnostic system.

---

## Report

The detailed technical report is available here:

**[📄 Read the Full Technical Report](Tamrin-2-ML.pdf)**

---

## Notebook

The complete implementation, outputs, visualizations, and analysis are available in:

**[📓 Open the Jupyter Notebook](ML-Assignment2.ipynb)**

---

## Academic Context

**Course:** Machine Learning
**Assignment:** Practical Assignment — Exploring Mental Health Data
**Task:** Binary Classification of Depression
