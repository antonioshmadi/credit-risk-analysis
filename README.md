# Credit Risk Analysis with Python and SQL

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

- Data loading and initial inspection
- Missing-value analysis
- Target distribution analysis
- Numerical feature exploration
- Bad credit rate analysis across categorical variables
- Baseline logistic regression
- Class-weighted logistic regression
- Model comparison using accuracy, ROC-AUC, classification reports, and confusion matrices

## Main Findings

The target variable is moderately imbalanced, with 70% good credit outcomes and 30% bad credit outcomes.

Bad credit risk borrowers tend to have longer loan durations and higher average credit amounts. Categorical variables such as checking account status, credit history, savings status, employment status, and housing status show substantial differences in observed bad credit rates.

The baseline logistic regression model achieves an accuracy of 0.78 and a ROC-AUC of approximately 0.804. However, its recall for the bad credit risk class is 0.53.

The class-weighted logistic regression model achieves an accuracy of 0.75 and a ROC-AUC of approximately 0.806, while improving recall for the bad credit risk class to 0.80.

## Interpretation

The balanced model is better at detecting bad credit risk borrowers, while the baseline model has slightly higher overall accuracy. This illustrates a common credit risk tradeoff: maximizing accuracy may not be sufficient when the minority class is the class of greatest business interest.

## Next Steps

- Add SQL-based segmentation analysis
- Add model calibration
- Compare with tree-based models
- Add cost-sensitive evaluation
- Refactor notebook code into reusable Python scripts

## Model Results

| Model | Accuracy | ROC-AUC | Recall for Bad Credit |
|---|---:|---:|---:|
| Baseline Logistic Regression | 0.78 | 0.804 | 0.53 |
| Class-Weighted Logistic Regression | 0.75 | 0.806 | 0.80 |

The class-weighted model sacrifices some overall accuracy but substantially improves recall for the bad credit class. In credit risk settings, this tradeoff can be preferable when missing high-risk borrowers is more costly than incorrectly flagging low-risk borrowers.
