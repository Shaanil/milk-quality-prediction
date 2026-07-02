# Milk Quality Prediction Pipeline

This project aims to develop a predictive system that determines the quality of milk based on its physicochemical and sensory properties. By analyzing parameters such as pH, temperature, taste, odor, fat content, turbidity, and color, the study seeks to identify patterns that distinguish between high-quality and low-quality milk samples.

---

## Preprocessing and Exploratory Data Analysis

### Missing Data Check
A heatmap validation was performed to confirm data completeness before training. The dataset contained no missing records.

![Missing Data Heatmap](images/missing_data.png)

### Outlier Removal
Extreme outliers in the pH distribution were identified and resolved using the Interquartile Range method to protect model stability.

![pH Boxplots Before and After](images/outliers.png)

### Class Balancing (SMOTE)
The target variable initially showed an unequal distribution of classes. Synthetic Minority Over-sampling Technique (SMOTE) was applied to ensure equal class representation.

![Class Balance Before and After](images/distribution.png)

### Feature Selection
A correlation matrix was computed to observe the linear relationships between the engineered physicochemical parameters and the final encoded milk grade.

![Correlation Heatmap](images/correlation.png)

---

## Performance Matrix

Six machine learning frameworks were evaluated using an 80/20 train-test split configuration. The hyperparameter-tuned Random Forest ensemble delivered the most stable generalization metrics on unseen data.

| Supervised Framework | Test Accuracy | Weighted F1-Score | ROC-AUC |
| :--- | :---: | :---: | :---: |
| Random Forest | 0.9719 | 0.9715 | 1.0000 |
| Support Vector Machine | 0.9943 | 0.9900 | 1.0000 |
| K-Nearest Neighbors | 0.9944 | 0.9900 | — |
| Decision Tree | 0.9719 | 0.9700 | — |
| Naive Bayes | 0.9607 | 0.9730 | 0.9843 |
| Logistic Regression | 0.7135 | 0.7901 | 0.7952 |

---

## Project Contributors

* J.G.H. Jayalath
* B.M.B.S. Alahakoon
* P.A.S. Dinod
* M.G.M. Sanvidu
* S.A.W. Fernando
* N. Thahani

