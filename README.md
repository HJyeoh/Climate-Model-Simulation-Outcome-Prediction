# Climate-Model-Simulation-Outcome-Prediction

# 🌦️ Climate Model Simulation Outcome Prediction

This project focuses on comparing **Support Vector Machine (SVM)** and **K-Nearest Neighbours (KNN)** classifiers to predict **climate model simulation outcomes** (success or failure) based on 18 input parameters.


## 📘 Project Overview

The goal of this project is to **predict whether a climate model simulation will crash or succeed**, using a dataset containing **540 samples**.
Each sample includes **18 scaled input parameters** (values between 0 and 1) and a **binary outcome label**:

* `0` → Failure
* `1` → Success


## 🧩 Dataset Description

| Column | Description                                             |
| :----- | :------------------------------------------------------ |
| 1      | Latin hypercube study ID (study 1–3)                    |
| 2      | Simulation ID (run 1–180)                               |
| 3–20   | Scaled climate model parameters (values between [0, 1]) |
| 21     | Simulation outcome (0 = failure, 1 = success)           |

---

## ⚙️ Methodology

1. **Data Preprocessing**

   * Dataset split into **80% training** and **20% testing**.
   * Scaling applied to all input features.

2. **Model Training**

   * Two models trained: **SVM** and **KNN**.
   * Multiple configurations tested:

     * Without fine-tuning
     * With fine-tuning
     * With feature selection + fine-tuning

3. **Evaluation**

   * Metrics used: **Accuracy**, **Precision**, **Recall**, **F1-score**, and **Confusion Matrix**.

## 🧠 Key Findings

* **SVM with feature selection and fine-tuning** achieved the **highest accuracy (96.30%)** and the best balance between precision and recall.
* Both models struggled with the **minority class (failures)**, but fine-tuning improved SVM performance significantly.
* **Feature selection and tuning** have a greater positive impact on **SVM** than on **KNN**.

## 🏁 Conclusion

The optimized **SVM** model is the most effective for predicting climate simulation outcomes in this dataset.
Although **KNN** performs reasonably well, it struggles more with **class imbalance**.
For imbalanced datasets, **SVM with feature selection and fine-tuning** is recommended as the superior approach.


## 🧰 Tools & Libraries

* Python 🐍
* Scikit-learn
* NumPy
* Pandas
* Matplotlib 

