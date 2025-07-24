
# 🚨 Visualizing and Predicting Crime in Los Angeles

[![License: Public Domain](https://img.shields.io/badge/License-Public%20Domain-green.svg)](https://catalog.data.gov/dataset/crime-data-from-2020-to-present)  
![Python](https://img.shields.io/badge/Python-3.10+-blue) ![Jupyter](https://img.shields.io/badge/Notebook-EDA%20%2B%20ML-brightgreen) ![Machine Learning](https://img.shields.io/badge/ML-LogReg%2C%20XGBoost%2C%20RF-important)

## 📌 Project Overview

This project explores and predicts crime incidents in Los Angeles using LAPD open data from **2020 to Present**. The goal is twofold:

1. **Visualize crime patterns** across time and geography.
2. **Predict whether a reported incident results in an arrest**, using classification models.

This analysis helps city officials, law enforcement, and researchers make data-driven decisions around public safety and resource allocation.

---

## 📊 Data Source

**Los Angeles Police Department (LAPD) - Crime Data from 2020 to Present**  
🔗 [Official Dataset Link (Data.gov)](https://catalog.data.gov/dataset/crime-data-from-2020-to-present)

- Metadata Updated: July 12, 2025  
- Frequency: Bi-weekly updates (due to system transition)  
- Format: CSV, JSON, XML  
- Fields include: crime date, location, victim age/sex/descent, weapon used, crime code, arrest flag, etc.

📁 Only a **cleaned subset** of the dataset is used in this repo due to GitHub file size limits. See the above link for the complete dataset.

---

## 📂 Project Structure

```
📁 Visualizing-Crime-LA/
├── data/
│   └── la_crime_data_cleaned.csv
├── notebooks/
│   ├── Crime_data_EDA.ipynb
│   └── machine_learning_modeling.ipynb
├── presentations/
│   └── Final_Presentation.pptx
├── reports/
│   └── ADTA_5940_Final_Project_Paper.docx
└── README.md
```

---

## 📌 Key Objectives

- 🧹 Clean and preprocess LAPD crime data  
- 📊 Perform exploratory and geospatial data analysis (EDA)
- 🗺️ Map high-crime zones using lat/lon coordinates
- 🔎 Identify temporal trends (by hour, day, season)
- 🤖 Build predictive models to classify **whether an arrest occurs**
- 📈 Compare model performance using metrics like accuracy, F1, ROC-AUC

---

## 🔬 Tools & Technologies

- **Languages**: Python 3.10
- **Libraries**:
  - `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`
  - `scikit-learn`, `xgboost`
  - `folium` for geospatial mapping
- **Notebook**: Jupyter
- **Dashboard**: Tableau (optional)
- **Data Cleaning**: Manual + pandas-based preprocessing

---

## 🧠 Machine Learning Models

We compared three machine learning models to predict crime categories using spatial and temporal features:

- **Logistic Regression**:
  - Accuracy: 66%
  - Weighted F1-Score: ~0.48
  - Limitations: Poor at predicting minority crime categories.

- **XGBoost Classifier**:
  - Accuracy: 66%
  - Weighted F1-Score: 0.52
  - Shows better handling of class imbalance than Logistic Regression.

- **Random Forest (Grouped Classes)**:
  - Accuracy: 59%
  - Macro F1-Score: 0.37
  - Best for balanced predictions across grouped crime categories (Property, Violent, Other).

🔍 The Random Forest model provided the most equitable classification results, especially for less frequent crime types.
Target variable: `Arrest Flag (1 = Arrested, 0 = Not Arrested)`

---

## 📍 Visual Insights

- Heatmaps showing **crime hotspots** (Downtown LA, South LA, etc.)
- Time-series plots of **crime frequency over months/years**
- Boxplots of **victim age vs crime type**
- Weapon usage vs arrest rates

🧭 Helps identify areas and times that need higher patrolling.

---

## 💡 Real-world Applications

- **Public Safety Planning**: Allocate officers based on predicted hotspots
- **Policy Making**: Understand arrest disparities by crime type and location
- **Predictive Policing** (ethically): Forecast high-risk events and timings

---

## 🧾 Author

**Amrutha Vamshi Goud**  
📧 avamshi9099@gmail.com  
📍 Master's in Advanced Data Analytics  
📍 University of North Texas, 2025

---

## 📢 Disclaimer

This analysis is purely academic and intended for learning. Predictions do not represent real-time or official LAPD insights. Data may contain transcription errors or geospatial inaccuracies due to anonymization.
