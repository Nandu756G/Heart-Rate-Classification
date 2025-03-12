# Heart Rate Abnormality Classification

## Overview
This project aims to classify heart rate data into **normal (0)** and **abnormal (1)** categories using **Random Forest Classifier**. The dataset undergoes preprocessing to handle missing values, remove outliers, and scale features before training the model.

## Dataset Preprocessing
1. **Handling Missing Values:**
   - Missing heart rate values are replaced with the **mean** of the column.
   - Missing labels are filled with the **median** value.

2. **Outlier Removal (IQR Method):**
   - The **Interquartile Range (IQR)** method is used to detect and remove extreme outliers in heart rate values.

3. **Feature Scaling:**
   - **StandardScaler** is applied to normalize heart rate values for better model performance.

## Model Selection: Why Random Forest?
Random Forest was chosen over other models due to:
- **High Accuracy & Robustness:** Reduces overfitting by combining multiple decision trees.
- **Handling Outliers & Missing Data:** Works well with real-world noisy medical data.
- **Minimal Feature Engineering:** Performs well even with a single feature (heart rate).
- **Better Performance than Logistic Regression & SVM:** Logistic regression assumes a linear relationship, while SVM can be computationally expensive.

## Model Training & Evaluation
- **Training:** The cleaned dataset is split into **80% training** and **20% testing**.
- **Classifier Used:** `RandomForestClassifier(n_estimators=100, random_state=42)`
- **Evaluation Metrics:**
   - **Accuracy:** Measures overall correctness.
   - **Classification Report:** Includes precision, recall, and F1-score.

## Results
- The trained model achieved a classification accuracy of **~50%**, indicating a need for further optimization, additional features, or more data.

## Visualization
A histogram plot is generated to visualize the distribution of **normal vs. abnormal** heart rate values.

## Deliverables
- **Cleaned Dataset:** `cleaned_heart_rate_data.csv`

---
This README provides an overview of the classification process and model implementation.
