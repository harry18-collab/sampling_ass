Sampling Techniques for Imbalanced Datasets


-> Project Objective

The objective of this project is to understand the importance of sampling techniques in handling imbalanced datasets and to analyze how different sampling strategies impact the performance of various machine learning models.

In real-world applications such as Credit Card Fraud Detection, datasets are highly imbalanced (e.g., ~99% legitimate transactions vs. ~1% fraudulent transactions). This project focuses on balancing such data and evaluating multiple sampling strategies across different machine learning models to identify the most effective combinations for improved performance.

-> Dataset

Source: Creditcard_data.csv
Description:
The dataset consists of credit card transaction records. The target variable Class indicates whether a transaction is:

0 → Legitimate transaction

1 → Fraudulent transaction

The dataset is highly imbalanced, making it suitable for studying sampling techniques.

-> Methodology
1️) Data Balancing

Since the original dataset is heavily skewed, the data is first balanced to ensure fair and effective model training.

Technique Used: Random Over Sampling (RandomOverSampler from imbalanced-learn)

Outcome: Both classes (0 and 1) are balanced with equal representation in the training data.

2️) Sample Size Calculation

The sample size is determined using Cochran’s Formula with the following parameters:

Confidence Level: 95%

Margin of Error: 5%

Proportion (p): 0.5

This ensures statistically meaningful sampling.

3️) Sampling Techniques Applied

Five distinct samples are created from the balanced dataset using different sampling strategies:

Sampling 1: Simple Random Sampling

Sampling 2: Systematic Sampling

Sampling 3: Stratified Sampling

Sampling 4: Cluster Sampling

Sampling 5: Bootstrap Sampling (with replacement)

4️) Machine Learning Models

Each sampled dataset is evaluated using the following machine learning models:

M1: Logistic Regression

M2: Decision Tree Classifier

M3: Random Forest Classifier

M4: Support Vector Machine (SVM)

M5: Naive Bayes (GaussianNB)

The performance of each model is compared across different sampling techniques to identify the optimal sampling–model combination.
