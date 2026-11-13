
# Day 7 – Model Comparison

## Validation Results

| Metric | Logistic Regression | Decision Tree |
|---|---:|---:|
| Accuracy | 0.6541 | 0.6590 |
| Precision | 0.1765 | 0.1752 |
| Recall | 0.5551 | 0.5370 |
| F1 Score | 0.2679 | 0.2642 |
| Balanced Accuracy | 0.6110 | 0.6058 |
| ROC-AUC | 0.6596 | 0.6455 |
| Average Precision | 0.2235 | 0.2074 |

## Interpretation

Decision Tree achieved slightly higher accuracy.

Logistic Regression performed better in precision,
recall, F1 score, balanced accuracy, ROC-AUC and
average precision.

Therefore, Logistic Regression currently has stronger
validation performance for identifying the minority
readmission class.

Accuracy alone is insufficient for evaluating this
imbalanced classification problem.

## Evaluation Notes

- Dataset: Diabetes 130-US Hospitals
- Task: 30-day readmission prediction
- Evaluation split: Validation
- Decision Tree: Gini criterion, max_depth=10,
  min_samples_split=100, min_samples_leaf=50,
  class_weight=balanced, random_state=42.

These are validation results, not final test results.
