# 🎗️ Breast Cancer Survival Prediction

A Machine Learning project to predict breast cancer patient survival status 
(Alive / Dead) using clinical features.

## 📌 Problem Statement
Existing ML models fail on imbalanced medical datasets — biased toward 
predicting "Alive", causing them to miss high-risk Dead patients. 
Missing a Dead patient in clinical screening is life-threatening.

## 🎯 Objective
- Predict survival status using clinical features
- Compare 3 ML models: Logistic Regression, Random Forest, XGBoost
- Handle class imbalance using **SMOTE**
- Maximize **Recall** to detect high-risk patients

## 📊 Dataset
- Source: Breast Cancer clinical dataset
- Features: Age, Race, Tumor Size, Stage, Estrogen Status, etc.
- Target: Survival Status (Alive / Dead)

## 🛠️ Tech Stack
- Python, Pandas, NumPy, Scikit-learn
- XGBoost, imbalanced-learn (SMOTE)
- Matplotlib, Seaborn
- Jupyter Notebook

## 📈 Model Results

| Model | Accuracy | Recall | ROC-AUC |
|---|---|---|---|
| Logistic Regression | 0.901 | 0.425 | 0.902 |
| Random Forest | 0.906 | 0.508 | 0.897 |
| XGBoost | 0.886 | 0.608 | 0.850 |
| RF + SMOTE | 0.902 | 0.617 | 0.884 |
| **XGB + SMOTE + Threshold 0.3** ⭐ | **0.873** | **0.642** | **0.870** |

## 🏆 Best Model
**XGBoost + SMOTE + Threshold 0.3** — Highest Recall (0.642)  
Detects 64% of Dead patients correctly — best for medical use.

## 🚀 How to Run
1. Clone the repository:
```bash
   git clone(https://github.com/dhanushreen2004-collab/Breast-cancer-survival-prediction)
```
2. Install dependencies:
```bash
   pip install pandas numpy scikit-learn xgboost imbalanced-learn matplotlib seaborn
```
3. Open the notebook:
```bash
   jupyter notebook breast-cancer_survival_prdiction.ipynb
```

## 📁 Project Structure
```
├── breast-cancer_survival_prdiction.ipynb   # Main ML notebook
├── Breast_Cancer.csv              # Dataset
├── Breast_Cancer_Survival_prediction_ppt.pptx  # Presentation
└── README.md
```

## 👤 Author
**Dhanushree N**  
Capstone Project | Machine Learning
