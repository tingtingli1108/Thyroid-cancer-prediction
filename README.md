# From Data to Decision: Revolutionizing Thyroid Cancer Risk Stratification with Machine Learning

## 📖 Overview
This project was created by **UC Berkeley MIDS (Master of Information and Data Science)** students as part of the **Applied Machine Learning (W207)** course (Spring 2024).  

The goal of the project is to predict **recurrence of differentiated thyroid cancer** using machine learning models, and to compare our results with findings from a published study. We experiment with multiple algorithms, perform feature selection, and assess the impact of dataset imbalance handling techniques.  

---

## 🎯 Objectives
- Predict thyroid cancer recurrence  
- Reproduce and benchmark results against the **reference publication**  
- Compare multiple machine learning models  
- Perform feature selection to identify the most important clinical predictors:contentReference[oaicite:0]{index=0}  

---

## 📊 Dataset
- **Source:** [Kaggle – Differentiated Thyroid Cancer Recurrence Dataset](https://www.kaggle.com/datasets/joebeachcapital/differentiated-thyroid-cancer-recurrence) :contentReference[oaicite:1]{index=1}  
- **Size:** 383 patient records  
- **Features:** 16 clinicopathologic features + target  
- **Target:** `Recurred` (binary: Yes/No)  
- **Class imbalance:**  
  - Non-recurred: 275 patients  
  - Recurred: 108 patients  
  - Baseline accuracy: 72.8%:contentReference[oaicite:2]{index=2}  

**Key Features include:**  
- ATA Risk Assessment  
- Response  
- Tumor (T), Nodes (N), Metastasis (M)  
- Age  
- Focality, Adenopathology  
- Pathology subtype:contentReference[oaicite:3]{index=3}  

---

## ⚙️ Methodology
1. **Exploratory Data Analysis (EDA)** – distribution of clinical features, imbalance analysis.  
2. **Data Splits:** 60% training / 20% validation / 20% test.  
3. **Imbalance Handling:** Random Oversampling applied to training set.  
4. **Models Evaluated:**  
   - Decision Tree  
   - Random Forest  
   - Support Vector Machine (SVM)  
   - k-Nearest Neighbors (KNN)  
   - Artificial Neural Network (ANN)  
   - LightGBM  
   - Regression analysis with **LASSO** and **Ridge**:contentReference[oaicite:4]{index=4}  

5. **Libraries Used:**  
   - `pandas`, `numpy`, `seaborn`, `matplotlib`  
   - `scikit-learn`, `scipy`  
   - `tensorflow`, `keras`  
   - `imbalanced-learn`:contentReference[oaicite:5]{index=5}  

6. **Feature Selection & Interpretability:**  
   - SHAP (Shapley Additive exPlanations) values  
   - LASSO and Ridge regression to evaluate marginal feature contribution:contentReference[oaicite:6]{index=6}  

---

## 📈 Results
- **Random Forest & SVM** delivered the most robust performance across balanced datasets.  
- **Top predictive features:**  
  - Response  
  - ATA Risk  
  - N (lymph node involvement)  
  - T (tumor size)  
  - Age:contentReference[oaicite:7]{index=7}  
- Balancing the dataset significantly improved model sensitivity without overly sacrificing specificity.  
- Our results **aligned with and sometimes surpassed** the published study, validating our methodology.  
- **Trade-offs observed:** ANN and LightGBM showed more significant sensitivity-specificity tradeoffs compared to Random Forest and SVM:contentReference[oaicite:8]{index=8}.  

---

## ⚠️ Limitations & Next Steps
- **Limitations:**  
  - Small dataset size (383 patients)  
  - Imbalanced target variable  
  - Limited generalizability without multi-center data  

- **Next Steps:**  
  - Explore additional feature engineering and selection techniques  
  - Investigate advanced ensemble methods  
  - Expand dataset with more patients and clinical sources  
  - Continue refining trade-offs between sensitivity and specificity:contentReference[oaicite:9]{index=9}  

---

## 👥 Team
This project was created by UC Berkeley Master of Information and Data Science (MIDS) students as part of Applied Machine Learning course

Agnese Minazzo
Andrew Smit
Tingting Li