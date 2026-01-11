# 🧠 Ensemble Learning with scikit-learn

This repository contains **practical experiments with ensemble learning methods** implemented as part of my **Data Science course**.  
The focus is on understanding how different ensemble techniques improve model performance, stability, and generalization when compared to single estimators.

The project evolves over time and includes experiments with **both regression and classification ensembles**.

---

## 📂 Covered Methods

- ✅ **Voting Classifier** (hard voting)
- ✅ **Bagging & Pasting – Regression**
- ✅ **Bagging & Pasting – Classification**
- 🔜 Further ensemble methods (e.g. boosting, stacking)

Each experiment is documented in a separate Jupyter Notebook.

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

## 📊 Example Results

### 🧩 Bagging & Pasting – Regression

**Best hyperparameters (GridSearchCV):**
```bash
{
  'estimator__max_depth': 12,
  'estimator__min_samples_leaf': 1,
  'estimator__min_samples_split': 2,
  'max_samples': 0.8,
  'n_estimators': 300
}

R² score: 0.9145
```


---

## 🧪 Key Observations

- ⚖️ **Ensemble methods** often match or outperform the best single model
- 📉 **Bagging** reduces variance, especially for high-variance models
- 🧠 **Voting** benefits from model diversity
- 📌 Performance gains depend on both **model choice** and **data characteristics**

---

## 🛠️ Tech Stack

- **Python**
- **scikit-learn**
- **NumPy / Pandas**
- **Matplotlib / Seaborn**
- **SciPy**


👤 **Piotr Lipiński** 🗓️ *Finished: January 2026* 📫 *Contributions welcome!*
