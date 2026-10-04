# 📊 LendingClub Risk Prediction

## 📌 Overview

This project builds a **binary classification model using Keras** to predict whether a loan will be **fully paid or defaulted** using LendingClub data.

---

## 🎯 Objective

* Predict loan status:

  * `1` → Fully Paid
  * `0` → Charged Off
* Focus on identifying **high-risk borrowers**

---

## 📂 Dataset

* ~396K loan records
* Includes loan details, borrower info, and credit history

> **Note:** The code in this repository is released under the [MIT License](LICENSE). The CSV files (`lending_club_loan.csv`, `lending_club_info.csv`) contain public LendingClub loan data, which is not covered by the MIT License and remains subject to its original terms.

---

## 🧹 Preprocessing

* Removed irrelevant/redundant features (`emp_title`, `title`, `grade`)
* Handled missing values (imputation + row removal)
* One-hot encoded categorical variables
* Feature engineering:

  * Extracted zip codes
  * Converted dates to numeric
* Scaled features using **MinMaxScaler**

---

## 🤖 Model

* Neural Network (Keras):

  * 78 → 39 → 19 → 1 architecture
  * ReLU activations + Dropout
  * Sigmoid output
* Loss: Binary Crossentropy
* Optimizer: Adam

---

## 📈 Results

* **F1 Score (Test):** 0.93
* Strong performance on majority class
* Lower recall for default class due to imbalance

---

## ⚠️ Note

Dataset is **imbalanced (~80% fully paid)** → Accuracy is not reliable; F1-score is used instead.

---

## 🚀 Improvements

* Handle imbalance (SMOTE / class weights)
* Try tree-based models (XGBoost, LightGBM)
* Hyperparameter tuning

---

## 🛠️ Tech Stack

Python, Pandas, NumPy, Scikit-learn, TensorFlow/Keras

---
