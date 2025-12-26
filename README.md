

## 🧠 Personality Detection (Extrovert / Introvert) — Machine Learning Classifier

This project builds a machine-learning classification model to predict whether an individual is an **Extrovert or Introvert** based on behavioral and social-interaction attributes. The workflow includes data cleaning, preprocessing, model comparison, hyperparameter tuning, evaluation, and an interactive prediction component.

---

## 📂 Dataset Features

Key features used:

* Time spent alone
* Stage fear
* Social event attendance
* Going outside frequency
* Feeling drained after socializing
* Friends circle size
* Social media post frequency
* Target label — **Personality (Introvert / Extrovert)**

---

## 🧹 Data Cleaning & Preprocessing

* Label-encoded `Personality`
* Converted Yes/No responses → binary (0 / 1)
* Filled missing values using mean imputation
* Split dataset into train & test sets

---

## 🧪 Model Training & Cross-Validation

Evaluated multiple classifiers using 5-fold CV:

| Model               | Accuracy   |
| ------------------- | ---------- |
| Logistic Regression | 93.41%     |
| Decision Tree       | 86.69%     |
| KNN                 | 92.72%     |
| Random Forest       | 91.62%     |
| AdaBoost            | 92.83%     |
| Gradient Boosting   | 93.10%     |
| XGBoost             | 91.69%     |
| **SVM**             | **93.45%** |
| **Naive Bayes**     | **93.45%** |

**Shortlisted high-performers**

* Logistic Regression
* Gradient Boosting
* SVM
* Naive Bayes

---

## 🔧 Hyperparameter Tuning (GridSearchCV)

### Gradient Boosting

```
{ learning_rate: 0.01, max_depth: 2 }
CV Score: 0.9345
```

### SVM

```
{ C: 0.01, kernel: 'rbf' }
CV Score: 0.9345
```

---

## 🏁 Final Model Performance

Final chosen model: **Bernoulli Naive Bayes**

| Metric        | Score    |
| ------------- | -------- |
| Test Accuracy | **93%+** |
| MSE           | **0.07** |

Also generated:

* Confusion Matrix (heatmap)
* Classification Report

---

## 💻 Interactive Prediction System

User enters:

* time spent alone
* stage fear
* social activity levels
* posting frequency
* friends circle size
* social exhaustion response

The model predicts:

👉 **Introvert** or **Extrovert**

---

## 🛠️ Tech Stack

* Python • NumPy • Pandas
* Scikit-Learn
* XGBoost
* Seaborn / Matplotlib

---

## 🚀 Future Enhancements

* Convert to sklearn Pipeline
* Feature scaling experiments
* Add probability-based predictions
* Deploy using Streamlit

---

