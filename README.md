# Machine-Learning
This project addresses the problem of bank account fraud detection using a synthetic dataset published at NeurIPS 2022. The dataset includes transaction, account, and device-related features. The goal is to predict fraudulent transactions in a highly imbalanced dataset.

## Data Preprocessing

- Converting binary and boolean features to numeric types.

- Standardizing numerical features for consistent scaling.

- Identifying and addressing class imbalance.

## Handling Class Imbalance

Fraud instances represent only ~1% of the data. Several techniques were applied to balance the training set:

- Oversampling: Duplicates minority class examples.

- Undersampling: Reduces majority class examples.

- SMOTE: Generates synthetic examples of the minority class.

These techniques improved model recall, a crucial metric in fraud detection.

## Classification

A Random Forest classifier was trained on the original and balanced datasets. Key insights:

- Oversampling improved recall and F1-score without significantly reducing precision.

- Undersampling increased recall but caused many false positives.

- SMOTE improved generalization while slightly decreasing precision.

## Clustering Analysis

K-means clustering was applied to explore transaction patterns. Features were scaled, and the optimal number of clusters was determined via the elbow method. Clusters were of roughly equal size, revealing segmentation patterns that may help understand fraudulent behavior.

## Conclusions

- Class imbalance is a major challenge in fraud prediction; resampling strategies are essential.

- Oversampling and SMOTE provide the best balance between recall and precision.

- Combining supervised classification with unsupervised clustering offers insights and predictive capability.

- This project demonstrates practical machine learning techniques applied to a real-world fraud detection problem.
