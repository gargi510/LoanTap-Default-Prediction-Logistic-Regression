# LoanTap Default Prediction: Logistic Regression Model

This project builds a logistic regression-based classification model to predict the probability of personal loan default using LoanTap’s historical lending data. The approach is designed to assist fintech lenders in minimizing risk and improving underwriting decisions.

## 📌 Problem Statement
LoanTap, a digital lending platform, seeks to predict loan default risks to reduce NPAs and make more informed credit decisions.

## 🔍 Key Highlights
- **EDA & Preprocessing**: Addressed class imbalance, cleaned high-cardinality fields, and engineered meaningful features.
- **Feature Engineering**:
  - Risk grouping of job titles
  - Credit age calculation
  - Binary flags for credit indicators
- **Outlier Treatment**: IQR capping + log transformation
- **Modeling Techniques**:
  - Logistic Regression with and without SMOTE/class_weight
  - ROC-AUC, Precision, Recall, F1-score evaluations
- **Best Model**: Logistic Regression with `class_weight='balanced'` – achieved strong recall with robust AUC (0.71), optimal for real-world credit risk use.

## 📊 Metrics
| Model Type                  | Recall (Defaulters) | ROC AUC |
|----------------------------|---------------------|---------|
| Baseline (No Balancing)    | 7%                  | 0.71    |
| SMOTE Only                 | 54%                 | 0.69    |
| Class Weight Only (✔️ Best) | 66%                 | 0.71    |
| SMOTE + Class Weight       | 54%                 | 0.69    |

## 🛠 Tech Stack
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Jupyter / Colab

## 📈 Business Impact
Improves early detection of high-risk applicants with interpretable, regulator-friendly modeling techniques. Supports more confident and data-driven loan approvals and pricing strategies.

---

⭐ If you find this project useful, feel free to star or fork!
