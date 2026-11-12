# Day 6 - Logistic Regression Baseline

## Objective
Train and evaluate a Logistic Regression baseline model
for the Hospital Patient Readmission Prediction project.

## Dataset
- Dataset: Diabetes 130-US Hospitals
- Evaluation split: Validation
- Validation records: 16,467
- Target: readmitted within 30 days (binary classification)
- Classification threshold: 0.5

## Models
1. Logistic Regression
2. Dummy Classifier (most frequent strategy)

## Logistic Regression Configuration
- C: 1.0
- Penalty: L2
- Solver: liblinear
- Class weight: balanced
- Maximum iterations: 1000
- Random state: 42

## Validation Results

| Metric | Logistic Regression | Dummy Classifier |
|---|---:|---:|
| Accuracy | 0.6541 | 0.8860 |
| Precision | 0.1765 | 0.0000 |
| Recall | 0.5551 | 0.0000 |
| F1-score | 0.2679 | 0.0000 |
| Balanced Accuracy | 0.6110 | 0.5000 |
| ROC-AUC | 0.6596 | 0.5000 |
| Average Precision | 0.2235 | 0.1140 |

## Confusion Matrix

| | Predicted Not Readmitted | Predicted Readmitted |
|---|---:|---:|
| Actual Not Readmitted | 9729 (TN) | 4861 (FP) |
| Actual Readmitted | 835 (FN) | 1042 (TP) |

## Interpretation
The Logistic Regression model detects 55.51% of actual
readmissions at the default threshold of 0.5.

However, precision is 17.65%, indicating a high number of
false-positive predictions.

The Dummy Classifier achieves higher accuracy because of
class imbalance, but it fails to identify any positive cases.

Therefore, accuracy alone is not sufficient to evaluate
this imbalanced classification problem.

## Limitations
- This is a baseline academic model, not a clinically validated system.
- Results are based on the validation dataset.
- Further model comparison and threshold analysis are required.
- The test dataset has not been used for this experiment.

## Output Files
- results/day6_logistic_regression_metrics.json
- results/day6_validation_predictions.csv

## Next Step
Compare the baseline with a Decision Tree classifier.
