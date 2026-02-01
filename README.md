# 📊 Sampling Techniques on Imbalanced Credit Card Dataset

## 📌 Assignment Overview
This assignment analyzes the impact of different sampling techniques on machine learning model performance when dealing with a highly imbalanced credit card fraud dataset. The dataset is balanced using multiple sampling strategies, and the resulting performance of various machine learning models is compared using accuracy.

---

## 🎯 Objective
- Handle class imbalance in a real-world credit card fraud dataset  
- Apply five different sampling techniques  
- Train five different machine learning models  
- Compare model performance using accuracy  
- Identify the best sampling technique for each model  

---

## 📂 Dataset
- **Dataset Name:** Creditcard_data.csv  
- **Target Column:** Class  
  - `0` → Normal transaction  
  - `1` → Fraudulent transaction  
- The dataset is highly imbalanced, which necessitates the use of sampling techniques.

---

## ⚙️ Sampling Techniques Used

| Sampling Method | Description |
|-----------------|------------|
| Random Under Sampling (RUS) | Reduces majority class samples |
| Random Over Sampling (ROS) | Duplicates minority class samples |
| SMOTE | Generates synthetic minority class samples |
| NearMiss | Selects majority samples closest to minority samples |
| SMOTETomek | Combination of SMOTE and Tomek Links |

---

## 🤖 Machine Learning Models Used

| Model | Description |
|------|------------|
| Logistic Regression | Linear classification model |
| Decision Tree | Rule-based non-linear classifier |
| Random Forest | Ensemble learning model |
| K-Nearest Neighbors (KNN) | Distance-based classifier |
| Naive Bayes | Probabilistic classifier |

---

## 📊 Accuracy Comparison Results

| Model ↓ / Sampling → | RUS | ROS | SMOTE | NearMiss | SMOTETomek |
|----------------------|-----|-----|-------|----------|------------|
| Logistic Regression  | 69.40 | 92.24 | **93.97** | 42.67 | **93.97** |
| Decision Tree        | 58.19 | **98.71** | 98.28 | 28.88 | 96.98 |
| Random Forest        | 78.88 | **99.14** | 98.71 | 30.17 | 98.71 |
| KNN                  | 89.66 | 96.98 | 94.83 | **98.28** | 94.83 |
| Naive Bayes          | 62.07 | **95.26** | **95.26** | 2.59 | **95.26** |

---

## 🏆 Best Sampling Technique per Model

| Model | Best Sampling Technique | Accuracy |
|------|-------------------------|----------|
| Logistic Regression | SMOTE / SMOTETomek | 93.97% |
| Decision Tree | Random Over Sampling | 98.71% |
| Random Forest | Random Over Sampling | 99.14% |
| KNN | NearMiss | 98.28% |
| Naive Bayes | ROS / SMOTE / SMOTETomek | 95.26% |

---

## 🔍 Observations
- Over-sampling techniques generally outperform under-sampling techniques.
- Random Forest achieves the highest accuracy due to ensemble learning.
- NearMiss performs well for KNN but poorly for Naive Bayes.
- Random Under Sampling leads to loss of important information.
- No single sampling technique works best for all models.

---

## 🧠 Conclusion
The results demonstrate that sampling techniques play a crucial role in improving model performance on imbalanced datasets. Over-sampling methods such as SMOTE and Random Over Sampling consistently provide better accuracy. The optimal sampling strategy depends on the machine learning algorithm used.

---

## 🛠️ Technologies Used
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Imbalanced-learn  
- Jupyter Notebook  

---

## 📁 Project Structure

Sampling_Assignment/
│
├── Creditcard_data.csv
├── sampling_assignment.ipynb
├── requirements.txt
└── README.md
