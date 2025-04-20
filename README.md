
# Credit Card Fraud Detection

## Description
This project focuses on detecting fraudulent credit card transactions using supervised machine learning techniques. The dataset used is highly imbalanced, and we explore methods such as SMOTE and hyperparameter tuning to improve model accuracy. Our goal is to effectively classify fraudulent transactions while minimizing false positives and negatives.

---

## 📊 Data Source
The dataset used in this project is publicly available on Kaggle:
- [Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

It contains anonymized features (V1 to V28), the transaction amount, and a target label `Class` indicating fraud (`1`) or not (`0`).

---

## 🔍 Methodology

### 1. Exploratory Data Analysis (EDA)
- Checked for duplicates and missing values.
- Visualized the amount distribution for fraud vs non-fraud.
- Grouped by class and transaction amount to identify patterns.
- Identified that fraud often occurs for amounts below $100, and most features V1-V17 are correlated.

### 2. Feature Engineering
- Identified useful features from grouped analysis.
- Applied SMOTE to balance the dataset.

### 3. Model Building
- **Logistic Regression**
  - Tuned hyperparameters to achieve ~98% accuracy (ROC-AUC).
- **Decision Tree**
  - Set minimum samples per leaf to 30 to avoid overfitting.
  - Achieved ~95% accuracy.
- **Random Forest**
  - Max depth set to 30, min samples per leaf = 30.
  - Achieved ~99% accuracy, best performance overall.

---

## 📈 Results
| Model              | ROC-AUC Score |
|-------------------|---------------|
| Logistic Regression | 98%         |
| Decision Tree       | 95%         |
| Random Forest       | 99%         |

- Fraudulent transactions are generally small (< $2500).
- Time of day analysis suggests fraud peaks during early morning (bimodal distribution).

---

## ✅ Conclusion
1. **Random Forest** is the best-performing model with 99% ROC-AUC.
2. Fraudulent transactions are low in amount and often occur during off-peak hours.
3. SMOTE helped significantly in dealing with data imbalance.
4. Hyperparameter tuning greatly improved model performances.
5. EDA played a crucial role in understanding data characteristics and guiding feature selection.

---
