# Adult Income Classification with Over-Sampling Techniques

## Project Overview

This project aims to predict whether an individual's income exceeds \$50K/year using the Adult Income dataset. The focus is on handling class imbalance using various over-sampling techniques and evaluating different machine learning models to achieve optimal performance.



## Data Preprocessing

- Handled missing values by replacing "?" with the most frequent value in each column.
- Encoded categorical variables using one-hot encoding.
- Scaled numerical features using StandardScaler for better model performance.

## Handling Imbalanced Data

The dataset is imbalanced, with fewer instances of high-income individuals. To address this, the following over-sampling techniques were explored:

- **Random Over-Sampling:** Duplicates random samples from the minority class.
- **SMOTE (Synthetic Minority Over-sampling Technique):** Generates synthetic samples for the minority class.
- **ADASYN:** Similar to SMOTE but focuses more on difficult-to-learn examples.

**Why Over-Sampling?**  
Over-sampling helps balance the class distribution, allowing models to learn patterns from both classes more effectively and improving recall for the minority class.

## Model Selection

The following models were evaluated:

- **Logistic Regression:** Simple, interpretable baseline.
- **Random Forest:** Handles non-linearities and feature interactions well.
- **XGBoost:** Powerful gradient boosting algorithm, often yields top performance.
- **Support Vector Machine (SVM):** Effective for high-dimensional spaces.

**Model Choice Rationale:**  
After comparing models, XGBoost was chosen for its superior performance on the validation set, especially after applying SMOTE. It provided the best balance between precision and recall, and handled the imbalanced data effectively.


## Conclusion

- Over-sampling techniques like SMOTE significantly improved recall for the minority class.
- XGBoost with SMOTE provided the best overall performance.
- Proper handling of class imbalance is crucial for fair and accurate predictions in real-world datasets.



