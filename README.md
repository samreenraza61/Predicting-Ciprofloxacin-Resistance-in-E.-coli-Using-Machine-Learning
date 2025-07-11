# Predicting-Ciprofloxacin-Resistance-in-E.-coli-Using-Machine-Learning
This project explores how machine learning can be applied to biological data to predict whether an *Escherichia coli* clinical isolate is **resistant or susceptible** to the antibiotic **ciprofloxacin**, based on antimicrobial susceptibility testing data.

# 🧬 Predicting Ciprofloxacin Resistance in *E. coli* Using Machine Learning

**Author:** Samreen Raza  
**Date:** July 2025  
**Status:** 🚧 *This project is for learning purposes only — not intended for publication.*  

---

## 📂 Dataset Source

**Dataset Title:** E. coli Resistance Dataset  
**Link:** [Kaggle - E. coli Resistance Dataset](https://www.kaggle.com/datasets/valeriamaciel/e-coli-resistance-dataset)  
**Original Source:** [Bacterial and Viral Bioinformatics Resource Center (BV-BRC)](https://www.bv-brc.org/)  
**License:** CC BY-NC-SA 4.0  

### Dataset Includes:
- Genome ID and strain name  
- Antibiotic tested  
- Measurement values (e.g., MIC)  
- Resistance phenotype (Resistant / Susceptible / Intermediate)  
- Testing method and standard (CLSI / EUCAST)  
- PubMed reference (if available)  

---

## 🎯 Project Goal

To build supervised machine learning models that predict if an *E. coli* isolate is **resistant or susceptible to ciprofloxacin** using MIC values, measurement signs, and testing standards.

---

## 🛠️ Tools & Libraries Used

- Python  
- Google Colab  
- pandas, seaborn, matplotlib  
- scikit-learn (RandomForest, LogisticRegression, SVM)

---

## 🧹 Data Preprocessing Steps

1. Loaded the raw dataset in Google Colab.
2. Filtered only rows where `Resistant Phenotype` was **"Resistant"** or **"Susceptible"**.
3. Kept only data related to **ciprofloxacin**.
4. Removed rows with missing values in key columns:  
   - `Measurement Value`  
   - `Measurement Sign`  
   - `Testing Standard`
5. Converted target labels to binary:  
   - `Resistant` → 1  
   - `Susceptible` → 0  
6. Encoded `Measurement Sign` as numeric values:  
   - `<=` → -1  
   - `<` → -2  
   - `=` → 0  
   - `>` → 1  
   - `>=` → 2  
7. Applied one-hot encoding to `Antibiotic` and `Testing Standard`.

---

## 📈 Model Training & Evaluation

### Models Used:
- Random Forest
- Logistic Regression
- Support Vector Machine (SVM)

### Evaluation Metrics:
- Accuracy  
- Precision  
- Recall  
- F1-score  
- Confusion Matrix  

### Results:

#### 🔍 Random Forest:
- Accuracy: **0.99**
- Precision: 0.99  
- Recall: 0.99  
- F1-score: 0.99  

#### 🔍 Logistic Regression:
- Accuracy: **0.99**
- Precision: 0.99  
- Recall: 0.99  
- F1-score: 0.99  

#### 🔍 Support Vector Machine:
- Accuracy: **0.99**
- Precision: 0.99  
- Recall: 0.99  
- F1-score: 0.99  

---

## 📊 Feature Importance (Random Forest)

The most influential features in predicting ciprofloxacin resistance were:

| Rank | Feature                        | Importance |
|------|--------------------------------|------------|
| 1    | Measurement Value              | High       |
| 2    | Measurement Sign               | High       |
| 3    | Testing Standard_CLSI / EUCAST | Moderate   |

> These suggest that MIC levels and clinical testing standards play a strong role in resistance classification.

---

## 📌 Citation

**Dataset citation:**  
> Valeria Maciel (2024). *E. coli Resistance Dataset*.  
> [https://www.kaggle.com/datasets/valeriamaciel/e-coli-resistance-dataset](https://www.kaggle.com/datasets/valeriamaciel/e-coli-resistance-dataset)

---

## 📁 Notes

- This project is intended for **educational purposes only**, not clinical or publication use.
