# 🎗️ Breast Cancer Survival Prediction

A Machine Learning project to predict breast cancer patient survival status (Alive / Dead) using clinical features from real medical data.

---

## 📌 Problem Statement

Breast cancer is a leading cause of death among women worldwide.  
Existing ML models fail on imbalanced medical datasets — they are biased toward predicting **Alive**, causing them to miss high-risk **Dead** patients.  
Missing a Dead patient in clinical screening is **life-threatening**.

---

## 🎯 Objective

- Predict breast cancer patient survival status — **Alive / Dead**
- Build and compare **3 ML models** — Logistic Regression, Random Forest, XGBoost
- Handle class imbalance using **SMOTE**
- Maximize **Recall** — ensuring maximum Dead patients are correctly identified

---

## 📊 Dataset

- **File:** `breast-cancer-dataset.csv`
- **Size:** 387 KB
- **Features:** Age, Race, Marital Status, T Stage, N Stage, 6th Stage, Grade, Tumor Size, Estrogen Status, Progesterone Status, Regional Node Examined, Regional Node Positive
- **Target:** `Status` — Alive / Dead

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| ML Models | Scikit-learn, XGBoost |
| Imbalance Handling | imbalanced-learn (SMOTE) |
| Notebook | Jupyter Notebook |

---

## 📈 Model Results

| Model | Accuracy | Recall | ROC-AUC |
|---|---|---|---|
| Logistic Regression | 0.901 | 0.425 | 0.902 |
| Random Forest | 0.906 | 0.508 | 0.897 |
| XGBoost | 0.886 | 0.608 | 0.850 |
| Random Forest + SMOTE | 0.902 | 0.617 | 0.884 |
| XGBoost + SMOTE | 0.893 | 0.550 | 0.870 |
| **XGBoost + SMOTE + Threshold 0.3** ⭐ | **0.873** | **0.642** | **0.870** |

---

## 🏆 Best Model

> **XGBoost + SMOTE + Threshold 0.3**  
> Recall = **0.642** — Detects 64% of Dead patients correctly  
> Acceptable trade-off: false alarms are safer than missed diagnoses

---

## 💡 Why Recall is the Key Metric

| Error Type | Prediction | Reality | Impact |
|---|---|---|---|
| False Negative ❌ | Alive | Dead | Patient gets no treatment → **Life-threatening** |
| False Positive ⚠️ | Dead | Alive | Patient gets extra screening → **Manageable** |

That's why we prioritized **Recall over Accuracy**.

---

## 🚀 How to Run

Open `breast-cancer-survival-prediction.ipynb` in Jupyter Notebook or Google Colab and run all cells.

---

## 📁 Project Structure
```
breast-cancer-survival-prediction/
├── breast-cancer-survival-prediction.ipynb   # Main ML notebook
├── breast-cancer-dataset.csv                 # Dataset
├── breast-cancer-survival-prediction.pptx    # Project presentation
└── README.md                                 # Project documentation
```

---

## 🔍 Key Findings

- Logistic Regression had the highest ROC-AUC (0.902) but the lowest Recall (0.425) — missed 57% of Dead patients
- SMOTE significantly improved minority class detection by balancing training data from **5:1 to 1:1**
- Threshold tuning from 0.5 → 0.3 further boosted Recall without major accuracy loss
- XGBoost + SMOTE + Threshold 0.3 is the **best model for real-world medical use**

---

## 🌍 Real World Impact

- Helps doctors identify **high-risk patients early** — enabling timely treatment
- Reduces bias in medical AI — ensuring Dead patients are not overlooked
- Can be integrated into **hospital screening pipelines**

---

## 👤 Author

**Dhanushree N**  
Capstone Project | Machine Learning  
