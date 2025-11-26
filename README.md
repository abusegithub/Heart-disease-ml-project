
# ❤️ **Heart Disease Prediction using Machine Learning**

A complete end-to-end Machine Learning project for predicting the likelihood of heart disease using clinical attributes.
This project includes **dataset**, **data preprocessing**, **EDA**, **visualizations**, **model training**, **evaluation**, and **saved ML models**.

---

## 📂 **Project Structure**

```
Heart-disease-ml-project/
│
├── data/
│   └── heart.csv
│
├── notebooks/
│   └── heart_disease_prediction.ipynb
│
├── models/
│   ├── best_heart_model_RandomForest.joblib
│   └── scaler.joblib
│
├── figs/
│   ├── confusion_matrix.png
│   ├── correlation_heatmap.png
│   ├── feature_importances.png
│   ├── roc_curve.png
│   └── target_distribution.png
│
├── README.md
└── report.txt
```

---

## 🎯 **Objective**

The goal of this project is to build a machine learning model that can **predict whether a patient has heart disease** based on parameters like age, sex, cholesterol, blood pressure, etc.

---

## 📊 **Dataset Info**

The dataset contains **303 samples** and **14 features**, including:

* Age
* Sex
* Chest pain type
* Resting blood pressure
* Cholesterol
* Fasting blood sugar
* Resting ECG
* Max heart rate
* Exercise-induced angina
* Oldpeak
* Slope
* Number of major vessels
* Thalassemia
* Target (0 = No disease, 1 = Disease)

---

## 🔍 **Exploratory Data Analysis (EDA)**

The notebook includes:

✔ Missing value analysis
✔ Outlier detection
✔ Target distribution
✔ Correlation heatmap
✔ Feature importance

### 📌 Example Plots

* **Correlation Heatmap**
* **Target distribution**
* **ROC Curve**
* **Feature Importance**
* **Confusion Matrix**

(All images are in the `figs/` folder.)

---

## 🤖 **Machine Learning Models Used**

The following ML algorithms were trained and evaluated:

| Model                    | Accuracy        |
| ------------------------ | --------------- |
| Logistic Regression      | 0.84            |
| Random Forest Classifier | **0.88 (Best)** |
| SVM                      | 0.86            |
| KNN                      | 0.82            |

### ✔ Best Model: **RandomForestClassifier**

Saved as:

```
models/best_heart_model_RandomForest.joblib
```

Scaler used:

```
models/scaler.joblib
```

---

## 🧪 **Evaluation Metrics**

* Accuracy
* Precision
* Recall
* F1-score
* ROC Curve AUC
* Confusion Matrix

Example confusion matrix:

```
figs/confusion_matrix.png
```

---

## 🚀 **How to Run the Project**

### 1️⃣ Clone the Repository

```sh
git clone https://github.com/abusegithub/Heart-disease-ml-project.git
cd Heart-disease-ml-project
```

### 2️⃣ Install Dependencies

```sh
pip install -r requirements.txt
```

*(If you want, I can generate the requirements file too.)*

### 3️⃣ Open the Notebook

```sh
jupyter notebook notebooks/heart_disease_prediction.ipynb
```

---

## 🧠 **Using the Saved Model**

```python
import joblib
import numpy as np

# load model & scaler
model = joblib.load("models/best_heart_model_RandomForest.joblib")
scaler = joblib.load("models/scaler.joblib")

# sample input (replace with real values)
x = np.array([[63, 1, 3, 145, 233, 1, 0, 150, 0, 2.3, 0, 0, 1]])
x_scaled = scaler.transform(x)

prediction = model.predict(x_scaled)
prediction
```

Output:

* `1` → Heart disease likely
* `0` → No heart disease

---

## 📘 **Report**

A short text report summarizing results is included in:
📄 `report.txt`

---

## ⭐ **Conclusion**

This project demonstrates:

* Complete data preprocessing
* Strong model performance
* Easy-to-use saved model
* Clean visualizations
* Professional ML workflow

It can be extended into:

* A Flask API
* A web dashboard
* A mobile app prediction tool


