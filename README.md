# 🧠 Ensemble Learning – Voting Classifier

This project is part of my **Data Science** course, where I experiment with combining multiple models to improve predictive performance using the `VotingClassifier`.
This experiment demonstrates **ensemble learning** using a **hard voting strategy** with multiple classical machine learning models.  
The goal is to compare individual model performance with the ensemble result.

---

## 🏗️ Model Architecture

```mermaid
graph TD

VC["VotingClassifier
---
voting: hard
weights: None"]

LR["LogisticRegression
solver: liblinear
C: 1.0
max_iter: 100"]

SVC["SVC
kernel: rbf
C: 1.0
gamma: scale"]

GNB["GaussianNB
var_smoothing: 1e-09"]

VC --> LR
VC --> SVC
VC --> GNB
````

---

## 📊 Classification Report (VotingClassifier)

```bash
              precision    recall  f1-score   support

           0       0.88      0.90      0.89        71
           1       0.70      0.64      0.67        25

    accuracy                           0.83        96
   macro avg       0.79      0.77      0.78        96
weighted avg       0.83      0.83      0.83        96


```

---

## 📈 Accuracy Comparison

```bash
LogisticRegression 0.8333333333333334
SVC 0.7395833333333334
GaussianNB 0.8125
VotingClassifier 0.8333333333333334
SVC 0.7395833333333334
VotingClassifier 0.8333333333333334

```

---

## 🧪 Conclusions

* ✅ **VotingClassifier** achieved the **same accuracy as the best individual model**
* ⚖️ Ensemble improves **stability** and reduces model variance
* 📌 Hard voting works well when base models are **diverse**

---

## 🛠️ Tech Stack

* **scikit-learn**
* **NumPy / Pandas**
* **Matplotlib / Seaborn**
* **Python**

👤 **Piotr Lipiński** 🗓️ *Finished: January 2026* 📫 *Contributions welcome!*
