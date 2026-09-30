# Diabetes_Prediction
# 🩸 DiabetesAI – Diabetes Risk Prediction System

**DiabetesAI** is a machine-learning-based diabetes risk prediction and analytics web application built using **Python and Streamlit**.

The application uses a **Decision Tree Classifier** to analyze eight clinical input features and estimate diabetes probability. It provides an interactive dashboard with prediction results, risk categories, analytics, prediction history, dataset exploration, and model information.

> ⚠️ **Medical Disclaimer:** This project is intended for educational, portfolio, and analytical demonstration purposes only. It is **not a medical diagnostic system** and should not be used for clinical decision-making.

---

## ✨ Features

* 🔮 **Diabetes Risk Prediction**

  * Enter patient clinical parameters
  * Generate diabetes prediction
  * Display diabetes probability
  * Display risk category

* 📊 **Interactive Analytics**

  * Historical classification ratio
  * Risk-level distribution
  * Total assessments
  * Positive and negative predictions
  * Average risk score

* 📜 **Prediction History**

  * Automatically stores prediction results
  * Records timestamp and patient input values
  * Export prediction history as CSV

* 🗂️ **Dataset Explorer**

  * View dataset records
  * Display number of records and features
  * Explore feature distributions
  * Analyze Outcome distribution

* 🤖 **Machine Learning Model**

  * Decision Tree Classifier
  * Maximum depth: 7
  * Minimum samples leaf: 15
  * Eight numerical input features

* 📈 **Interactive Visualizations**

  * Risk probability gauge
  * Radar chart
  * Pie charts
  * Histograms
  * Feature distribution charts

* 🎨 **Modern Dashboard**

  * Streamlit interface
  * Dark theme
  * Glassmorphism-style cards
  * Responsive dashboard layout

---

## 🧠 Machine Learning Model

The application uses a **Decision Tree Classifier** for diabetes classification.

### Model Configuration

| Parameter             | Value                    |
| --------------------- | ------------------------ |
| Algorithm             | Decision Tree Classifier |
| Maximum Depth         | 7                        |
| Minimum Samples Leaf  | 15                       |
| Minimum Samples Split | 2                        |
| Target Variable       | Outcome                  |
| Number of Features    | 8                        |

The model predicts:

* `0` → No diabetes classification
* `1` → Diabetes classification

---

## 📥 Input Features

The model uses the following eight features:

1. **Pregnancies**
2. **Glucose**
3. **Blood Pressure**
4. **Skin Thickness**
5. **Insulin**
6. **BMI**
7. **Diabetes Pedigree Function**
8. **Age**

The application maintains the same feature ordering when sending data to the trained model.

---

## 🏗️ Project Structure

```text
DiabetesAI/
│
├── app.py
├── diabetes.csv
├── diabetes_model.pkl
├── diabetes_features.pkl
├── diabetes_prediction.ipynb
├── prediction_history.csv
├── requirements.txt
└── README.md
```

### File Description

| File                        | Description                         |
| --------------------------- | ----------------------------------- |
| `app.py`                    | Main Streamlit application          |
| `diabetes.csv`              | Diabetes dataset                    |
| `diabetes_model.pkl`        | Trained Decision Tree model         |
| `diabetes_features.pkl`     | Saved model feature ordering        |
| `diabetes_prediction.ipynb` | Model development/training notebook |
| `prediction_history.csv`    | Stores prediction history           |
| `requirements.txt`          | Python dependencies                 |
| `README.md`                 | Project documentation               |

---

## ⚙️ Technologies Used

* **Python**
* **Streamlit**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Plotly**
* **Pickle**
* **Jupyter Notebook**

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/DiabetesAI.git
```

Move into the project directory:

```bash
cd DiabetesAI
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Application

```bash
streamlit run app.py
```

The application will open in your browser.

---

## 📦 Requirements

Create a file named `requirements.txt`:

```text
streamlit
pandas
numpy
scikit-learn
plotly
```

---

## 🔄 Application Workflow

```text
Patient Clinical Data
        ↓
Input Validation
        ↓
Feature DataFrame
        ↓
Trained Decision Tree Model
        ↓
Prediction + Probability
        ↓
Risk Classification
        ↓
Interactive Visualization
        ↓
Prediction History
        ↓
CSV Report
```

---

## 📊 Risk Classification

The application categorizes diabetes probability into four levels:

| Probability | Risk Level        |
| ----------: | ----------------- |
|       0–30% | 🟢 Low Risk       |
|      30–60% | 🟡 Moderate Risk  |
|      60–80% | 🟠 High Risk      |
|     80–100% | 🔴 Very High Risk |

These categories are implemented as application display categories and should **not be interpreted as clinical diagnostic thresholds**.

---

## 🖥️ Dashboard Sections

### 🏠 Overview

Provides an introduction to the DiabetesAI platform and displays the main clinical feature scope.

### 🔮 Prediction Engine

Allows users to enter the eight clinical parameters and execute a prediction.

### 📊 Analytics Hub

Displays statistics and visualizations based on stored prediction records.

### 📜 Prediction History

Displays previously executed predictions and allows the history to be exported as CSV.

### 🗂️ Dataset Explorer

Allows exploration of the diabetes dataset and feature distributions.

### 🤖 Model Architecture

Displays the Decision Tree configuration and feature ordering.

### 📚 Clinical Insights

Provides educational information about selected diabetes-related biomarkers.

### ℹ️ About

Provides information about the project and technologies used.

---

## 📈 Prediction Output

After submitting patient parameters, the application displays:

* Model classification
* Diabetes probability
* Assessed risk category
* Classification confidence
* Risk probability gauge
* Normalized patient metric radar chart
* Contributory input insights
* Downloadable CSV clinical summary

The application also records prediction information with a timestamp in `prediction_history.csv`.

---

## 🎯 Project Objectives

The main objectives of this project are:

1. To demonstrate the use of machine learning for diabetes risk classification.
2. To develop an interactive healthcare analytics dashboard.
3. To visualize machine-learning prediction results.
4. To provide an easy-to-use interface for educational demonstration.
5. To maintain a history of prediction results.
6. To demonstrate integration of a trained ML model with Streamlit.

---

## 🔐 Important Note

The `.pkl` files contain serialized machine-learning objects. Only use model files from trusted sources.

Do not upload sensitive patient information or personally identifiable medical data to a public GitHub repository.

For a public repository, consider adding the following to `.gitignore`:

```text
__pycache__/
*.pyc
.venv/
venv/
.env
prediction_history.csv
```

---

## 📌 Future Enhancements

Possible future improvements include:

* Model performance evaluation dashboard
* Multiple machine-learning algorithms
* Model comparison
* ROC-AUC visualization
* Confusion matrix
* Feature importance visualization
* User authentication
* Database integration
* PDF report generation
* Cloud deployment
* Improved data validation
* Explainable AI features

---


The predictions generated by this application should not be considered a medical diagnosis or a substitute for professional medical advice. Always consult a qualified healthcare professional for medical evaluation and treatment decisions.
