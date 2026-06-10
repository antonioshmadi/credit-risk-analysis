# Credit Risk Analysis with Python

## Objective

This project analyzes the German Credit dataset as a binary credit risk classification problem. The goal is to explore borrower-level characteristics, identify patterns associated with bad credit risk, and build interpretable baseline classification models.

## Dataset

The dataset contains 1,000 borrower-level observations, 20 predictor variables, and one binary target variable indicating whether a borrower is classified as a good or bad credit risk.

## Tools

- Python
- pandas
- NumPy
- matplotlib
- scikit-learn
- Jupyter Notebook

## Analysis

The project includes:

* Data loading and initial inspection
* Missing-value analysis
* Target distribution analysis
* Numerical feature exploration
* Bad credit rate analysis across categorical variables
* Baseline logistic regression
* Class-weighted logistic regression
* Model comparison using accuracy, ROC-AUC, precision, recall, F1-score and confusion matrices
* 5-fold stratified cross-validation
* Threshold tuning for the classification decision rule
* Coefficient-based interpretation of the logistic regression model

## Main Findings

The target variable is moderately imbalanced, with 70% good credit outcomes and 30% bad credit outcomes.

Bad credit risk borrowers tend to have longer loan durations and higher average credit amounts. Categorical variables such as checking account status, credit history, savings status, employment status, and housing status show substantial differences in observed bad credit rates.

The baseline logistic regression model achieves an accuracy of 0.78 and a ROC-AUC of approximately 0.804. However, its recall for the bad credit risk class is 0.53.

The class-weighted logistic regression model achieves an accuracy of 0.75 and a ROC-AUC of approximately 0.806, while improving recall for the bad credit risk class to 0.80.

Cross-validation supports the same qualitative tradeoff: the baseline model has stronger overall accuracy, while the class-weighted model improves detection of bad credit risk borrowers.

Threshold tuning shows that the default 0.5 classification threshold is not necessarily optimal in a credit risk setting. Lowering the threshold can improve recall for bad credit risk borrowers, at the cost of more false positives.

## Business Interpretation

The balanced model is better at detecting bad credit risk borrowers, while the baseline model has slightly higher overall accuracy. This illustrates a common credit risk tradeoff: maximizing accuracy may not be sufficient when the minority class is the class of greatest business interest.

In a credit risk context, false negatives and false positives have different business costs. A false negative may expose the lender to credit losses, while a false positive may reject or flag a potentially profitable borrower. For this reason, recall, precision, threshold selection and confusion matrices are more informative than accuracy alone.

## Limitations

* The dataset is relatively small, with 1,000 observations.
* The analysis is observational and does not establish causality.
* The model is intended as an interpretable baseline, not a production credit scoring system.
* A real credit risk system would require calibration, cost-sensitive evaluation, external validation and fairness analysis.

## Next Steps

Future work could include:

* SQL-based segmentation analysis
* Model calibration
* Tree-based models
* Cost-sensitive evaluation
* Fairness and bias analysis
* Conversion of the notebook workflow into reusable Python scripts