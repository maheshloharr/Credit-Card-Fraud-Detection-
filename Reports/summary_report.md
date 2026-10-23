# Summary Report — Credit Card Fraud Detection

## Business Problem

Credit-card fraud detection is an extreme imbalanced classification problem. In the supplied dataset, fraudulent transactions represent only about 0.17% of all transactions. Because legitimate transactions dominate, accuracy is not a reliable measure of fraud-detection quality. A model predicting every transaction as legitimate can achieve approximately 99.83% accuracy while detecting no fraud. For this reason, this project uses Precision, Recall, F1-score and especially PR-AUC to evaluate the minority fraud class.

## Imbalance Handling

A stratified 50,000-row sample was created for local execution, preserving the fraud ratio. The training set was split into three versions: original imbalanced data, SMOTE with a 0.1 sampling strategy, and Random Undersampling with a 0.1 sampling strategy. The untouched test set was never resampled. Logistic Regression performed best among its three variants with SMOTE, reaching PR-AUC 0.8133 and recall 1.0000 at the default threshold.

## Model Selection and Threshold

Random Forest achieved PR-AUC 0.8748. The baseline XGBoost model achieved PR-AUC 0.8996. After the required 15-iteration, 3-fold RandomizedSearchCV, tuned XGBoost achieved the strongest PR-AUC of 0.9133 on the test set. Its best parameters were 300 estimators, depth 3, learning rate 0.1, subsample 0.6 and column subsampling 0.8. At the default 0.5 threshold, tuned XGBoost had precision 0.9286, recall 0.7647 and F1 0.8387. The F1-optimal threshold was 0.3930, producing precision 0.8824, recall 0.8824 and F1 0.8824. A much lower threshold of 0.0148 achieved recall 0.9412 with precision 0.5926, showing the operational tradeoff clearly.

## Cost-Benefit Result

Using the exam assumptions of ₹4,500 average fraud value and ₹150 investigation cost per flagged transaction, the highest net benefit on the 10,000-row test set was ₹64,950. At the F1-optimal threshold, 15 fraud transactions were caught, 2 legitimate transactions were falsely flagged, and 2 fraud transactions were missed. The business result demonstrates why the final threshold should be chosen with the risk team rather than from a model metric alone.

## Production Improvements

A production system should perform real-time scoring, maintain monitoring for data and model drift, and continuously collect confirmed fraud/legitimate outcomes for a feedback loop. Thresholds should be reviewed as fraud patterns, investigation capacity and transaction values change. Additional production controls would include model versioning, alert monitoring, latency monitoring, calibration checks and periodic retraining.
