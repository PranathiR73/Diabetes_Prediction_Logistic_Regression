## Minor Project 3: Diabetes Prediction using Logistic Regression

## 🚀 Internship Overview
* **Program:** Machine Learning Internship Program
* **Organization:** Unlox Academy
* **Student Name:** Pranathi R
* **Project Type:** Minor Project 3 (ML Classification)

---

## 📌 Project Objective
The objective of this project is to build, evaluate, and interpret a **Logistic Regression** binary classification model to predict whether a patient has diabetes based on diagnostic measurement features.
* **0:** No Diabetes
* **1:** Diabetes

---

## 📂 Dataset Information
* **Dataset Used:** Pima Indians Diabetes Database
* **File Name:** `diabetes.csv`
* **Features Included (8 Inputs):**
  1. Pregnancies
  2. Glucose
  3. BloodPressure
  4. SkinThickness
  5. Insulin
  6. BMI (Body Mass Index)
  7. DiabetesPedigreeFunction
  8. Age

---

## ⚙️ Methodology & Pipeline Workflow
To ensure rigorous data handling and prevent data leakage, the project follows a strict end-to-end machine learning pipeline using `scikit-learn`:
1. **Data Loading & Inspection:** Loaded `diabetes.csv`[cite: 2], examined shapes, data types, and summary statistics.
2. **Handling Invalid Zeros:** Replaced biologically impossible zero values with `NaN` in key health metrics (*Glucose, BloodPressure, SkinThickness, Insulin, and BMI*).
3. **Train-Test Split:** Split the dataset into 80% training and 20% testing sets with class stratification (`stratify=y`).
4. **Preprocessing Pipeline:**
   * **Median Imputation:** Replaced missing values (`NaN`) using the median calculated exclusively from the training set.
   * **Standard Scaling:** Standardized feature distributions to have a mean of 0 and variance of 1.
5. **Model Training:** Trained a **Balanced Logistic Regression** model (`class_weight='balanced'`) to handle class imbalance effectively.
6. **Evaluation & Interpretation:** Evaluated performance using multiple classification metrics, a confusion matrix, ROC-AUC curve, and feature coefficient analysis.

---

## 📊 Evaluation Metrics & Results

| Metric | Score | Interpretation |
| :--- | :--- | :--- |
| **Accuracy** | **0.734** | Overall correct predictions |
| **Precision** | **0.603** | Reliability of positive predictions |
| **Recall** | **0.704** | Detection rate of actual positive cases |
| **F1-score** | **0.650** | Harmonic balance of precision and recall |
| **ROC-AUC** | **0.813** | Overall model class-separation capability |

### Confusion Matrix Breakdown
* **True Negatives (TN):** 75
* **False Positives (FP):** 25
* **False Negatives (FN):** 16
* **True Positives (TP):** 38

---

## 🔍 Key Findings & Limitations
* **Performance:** The model achieves a solid **ROC-AUC score of 0.813** and successfully detects ~70.4% of positive diabetes cases.
* **Feature Importance:** *Glucose* and *BMI* exhibit the strongest positive model coefficients, indicating they are the primary drivers for predicting diabetes.
* **Clinical Relevance:** In medical screening tasks, **Recall** is prioritized to minimize false negatives and ensure potential positive cases are not missed.
* **Limitation:** This small historical dataset represents a specific demographic population. It is designed for learning and educational classification concepts rather than clinical medical diagnosis.

---

## 📁 Repository Structure
```text
├── Pranathi_R_Diabetes_Prediction_Logistic_Regression.ipynb   # Executed Google Colab Notebook
├── Pranathi R_Logistic_Regression_Sep.pdf                     # Final Project Report PDF
└── diabetes.csv                                               # Dataset file
