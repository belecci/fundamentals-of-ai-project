# fundamentals-of-ai-project
# 🤖 AI-Driven Network Intrusion Detection & Traffic Classification

## 📋 Project Overview
This project applies fundamental principles of Artificial Intelligence and Data Science following the CRISP-DM framework to analyze a cybersecurity dataset of 6,000 network sessions. The objective was to build and evaluate predictive models capable of distinguishing between legitimate (Benign) and malicious (Brute Force) network activity, alongside predicting average packet sizes via regression models.

---

## 🔍 Data Understanding & Preprocessing
* **Dataset Structure:** 6,000 records across 19 numerical and categorical features representing day-to-day network telemetry.
* **Class Imbalance:** Identified a moderate class imbalance in the target variable (`attack_category`), where Benign traffic accounts for ~70% (4,161 samples) and Brute Force accounts for ~30% (1,839 samples).
* **Data Cleaning:** Handled missing values, standardized string casings, applied `LabelEncoder` for categorical variables, and `StandardScaler` for normalization.

---

## 🛠️ Feature Engineering
1. **`failed_login_ratio`**: `failed_logins / (login_attempts + 1)` — represents the proportion of failed login attempts relative to total attempts.
2. **`anomaly_per_packet`**: `anomaly_score / (packet_rate + 1)` — normalizes anomaly indicators against overall packet volume.

---

## 🤖 Machine Learning Models & Evaluation
* **Classification Models:** Evaluated Decision Tree (Baseline), Default Random Forest, Tuned Random Forest (GridSearchCV), and Naive Bayes models. Highlighted the critical impact of **Class Imbalance** on Brute Force recall.
* **Regression Models:** Evaluated Linear and Ridge Regression models to predict `avg_packet_size`, achieving an optimal cross-validation score with Tuned Ridge Regression ($\alpha = 10.0$).

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
* **Methodology:** CRISP-DM Framework, Exploratory Data Analysis (EDA), Hyperparameter Tuning
