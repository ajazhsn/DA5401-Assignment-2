# 🍄 PCA & Logistic Regression on Mushroom Dataset  

This repository contains my solution for **DA5401 — Assignment 2**, where we apply **Principal Component Analysis (PCA)** to the Mushroom dataset and evaluate how dimensionality reduction affects classification performance using **Logistic Regression**.  

---

## 📂 Project Overview
- **Dataset**: [Mushroom Classification (UCI/Kaggle)](https://www.kaggle.com/datasets/uciml/mushroom-classification)  
- **Goal**: Reduce dimensionality of a high-cardinality categorical dataset using PCA and compare classification results before and after reduction.  
- **Key Methods**:  
  - One-hot encoding for categorical features  
  - Standardization (scaling)  
  - PCA (variance explained, scree & cumulative plots)  
  - Logistic Regression (baseline vs PCA-reduced)  

---

## 🔍 Steps Covered
1. **Exploratory Data Analysis (EDA)**  
   - Checked class distribution (edible vs poisonous)  
   - Inspected feature cardinality before and after one-hot encoding  

2. **Dimensionality Reduction with PCA**  
   - Computed explained variance ratio per component  
   - Plotted **📈 Scree Plot** and **Cumulative Variance**  
   - Selected optimal number of components (~95% variance retained)  

3. **Classification with Logistic Regression**  
   - **Baseline model**: trained on original standardized dataset  
   - **PCA-transformed model**: trained on reduced dataset  
   - Compared precision, recall, F1-score, and accuracy  

4. **Performance Comparison**  
   - Both models achieved near-perfect accuracy (>99%)  
   - F1-scores showed minor rounding differences (e.g., 0.9988 → 1.00 in sklearn’s default report)  
   - PCA reduced redundancy while keeping predictive power intact  

---

## 📊 Results
| Model                  | Accuracy | F1-Score |
|-------------------------|----------|----------|
| Logistic Regression (Baseline) | 100%   | 1 |
| Logistic Regression (PCA)      | ~99.8%   | ~0.9988 |

> ⚖️ **Insight:** PCA simplified the dataset (fewer dimensions, less redundancy) without significantly hurting classification performance. Logistic Regression proved to be a solid linear baseline for evaluation.  

---

## 🛠️ Tech Stack
- Python 🐍  
- Pandas, NumPy  
- scikit-learn  
- Matplotlib  

---

