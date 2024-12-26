<h1 align="center">🌟 Stress Detection and Relief Recommendations 🌟</h1>

<p align="center">
  A machine learning-based system to detect stress levels, recommend relief actions, and provide a suicide action plan based on the predicted stress level. 🚨💡✨
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue" />
  <img src="https://img.shields.io/badge/Random--Forest-Accuracy%3A%201.00-success" />
  <img src="https://img.shields.io/badge/XGBoost-Accuracy%3A%201.00-success" />
  <img src="https://img.shields.io/badge/Meta--Model-Accuracy%3A%200.96-important" />
</p>

---

## 📖 Overview

This project uses machine learning algorithms to predict stress levels from user data and provide tailored recommendations for stress relief. It also includes a **Suicide Action Plan** feature for high-risk users, aiming to promote mental well-being and offer critical assistance.

---

## 💡 Features

1. **Stress Level Detection**: Predicts stress levels based on input data.
2. **Relief Recommendations**: Offers personalized stress-relief techniques.
3. **Suicide Action Plan**: Provides a detailed plan and resources for high-risk individuals.
4. **Meta-Model Implementation**: Combines multiple classifiers for enhanced prediction accuracy.

---

## 🛠️ Technologies Used

- **Programming Language**: Python
- **Machine Learning Algorithms**:
  - Random Forest Classifier (Accuracy: 1.00)
  - XGBoost Classifier (Accuracy: 1.00)
  - Logistic Regression (Accuracy: 0.89)
  - Support Vector Machine (SVM) (Accuracy: 0.41)
  - KMeans Clustering (Accuracy: 0.43)
- **Meta-Model**: Combines all five algorithms (Accuracy: 0.96)

---

## 🚀 How It Works

### 1️⃣ Data Processing
- Data preprocessing includes handling missing values, normalization, and feature engineering.

### 2️⃣ Model Training and Evaluation
- Trained five models independently:
  - Random Forest Classifier
  - XGBoost Classifier
  - Logistic Regression
  - Support Vector Machine
  - KMeans Clustering
- Meta-model built using the outputs of the above classifiers for final predictions.

### 3️⃣ Stress Level Prediction
- The system predicts the user's stress level as **Low**, **Moderate**, or **High** based on the input.

### 4️⃣ Recommendations and Suicide Action Plan
- Provides stress-relief recommendations such as meditation, exercise, and therapy.
- For high-stress levels, a suicide action plan is recommended, including hotlines and immediate support measures.

---

## 📊 Accuracy Results

| Algorithm               | Accuracy |
|-------------------------|----------|
| Random Forest Classifier | 1.00     |
| XGBoost Classifier       | 1.00     |
| Logistic Regression      | 0.89     |
| Support Vector Machine   | 0.41     |
| KMeans Clustering        | 0.43     |
| **Meta-Model**           | **0.96** |

---

## ⚙️ How to Run

### 4️⃣ Input Data
Provide your data (e.g., stress-related metrics or survey responses) in the prompted format.

### 5️⃣ View Results
- The system will output the predicted stress level.
- Recommendations or the suicide action plan will be displayed based on the stress level.

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE)

---

## 🔗 References

1. [Scikit-learn Documentation](https://scikit-learn.org/)
2. [XGBoost Documentation](https://xgboost.readthedocs.io/)
