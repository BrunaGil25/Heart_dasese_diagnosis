# Heart Disease Diagnosis with Machine Learning

This project applies machine learning techniques to predict heart disease severity using clinical data. It combines data preprocessing, exploratory analysis, class balancing, dimensionality reduction, and modeling — all aimed at uncovering patterns that support diagnostic decisions.

---

## Objectives

- Investigate relationships between clinical variables and diagnosis outcomes  
- Apply binary and multi-class classification models  
- Balance class distributions using SMOTE  
- Visualize diagnostic clusters with PCA and UMAP  
- Evaluate model performance using accuracy, precision, recall, and F1-score  
- Interpret model decisions with feature importance and confusion matrices

---

## Dataset Overview

The dataset contains anonymized patient-level clinical information, including:

| Feature     | Description                                      |
|-------------|--------------------------------------------------|
| `age`       | Age of the patient                               |
| `chol`      | Serum cholesterol level                          |
| `thalach`   | Maximum heart rate achieved                      |
| `cp`        | Chest pain type                                  |
| `oldpeak`   | ST depression induced by exercise                |
| `slope`     | Slope of the ST segment                          |
| `ca`        | Number of major vessels (0–3) via fluoroscopy    |
| `thal`      | Thalassemia result                               |
| `target`    | Diagnosis class (0 = healthy to 4 = severe)      |

Preprocessing included replacing `"?"` values, handling NaNs, converting types, and standardizing the feature space.

---

## Technologies

- Python 3.12  
- pandas, numpy  
- scikit-learn  
- seaborn, matplotlib  
- imbalanced-learn  
- umap-learn  
- Jupyter Notebook

---

## Project Structure

- `diagnosis_notebook.ipynb`: Full analysis pipeline with code, plots, and commentary  
- `images/`: Folder for generated visualizations (e.g., confusion matrix, PCA, UMAP)  
- `requirements.txt`: Package dependencies  
- `README.md`: Project documentation  
- `Data`: DataSet source from https://archive.ics.uci.edu/dataset/45/heart+disease (cleveland.data)

---

## Installation & Setup

To run this project locally, follow these steps:

1. Clone the repository: https://github.com/BrunaGil25/heart-disease-diagnosis

2. Navigate to the project folder: cd heart-disease-diagnosis

3. Create a virtual environment: python -m venv env source \env\Scripts\activate      # On Windows

4. Install required packages: pip install -r requirements.txt

---

## How to Run

Launch Jupyter Notebook:
```bash
jupyter notebook


Run the cells from top to bottom to follow the analysis flow:
- Data loading and cleaning  
- Exploratory visualizations  
- SMOTE resampling  
- Model training and evaluation  
- Dimensionality reduction and interpretation  

## Project Workflow

- **Data Cleaning:** Handles missing values and ensures all features are numeric for reliable analysis.
- **Exploratory Data Analysis (EDA):** Visualizes distributions and relationships among age, cholesterol, chest pain type, heart rate, and sex.
- **Class Balancing:** Uses SMOTE to address class imbalance and improve model fairness.
- **Dimensionality Reduction:** Applies PCA and UMAP to visualize feature space and assess cluster separability.
- **Model Training:** Trains Random Forest and Logistic Regression models for both binary and multi-class diagnosis targets.
- **Evaluation:** Uses accuracy, classification reports, and confusion matrices to assess model performance.
- **Interpretability:** Analyzes feature importance to understand which clinical variables drive predictions.

## Key Results

- No single feature can separate diagnosis classes; combinations of features yield stronger predictions.
- SMOTE improves classification consistency for rare diagnosis classes.
- UMAP and PCA provide insights into feature clustering and diagnosis separability.
- The Random Forest classifier achieves **83.75% accuracy** with balanced precision and recall across all diagnosis levels.
- Features such as `ca`, `chol`, `oldpeak`, and `age` are dominant predictors.

## Future Improvements

- Add an interactive dashboard (Streamlit or Plotly Dash) for real-time prediction and visualization.
- Explore temporal modeling if longitudinal data is available.
- Extend interpretability with SHAP values for individual prediction explanations.
- Validate the model on external datasets for generalization.

---

> This project highlights the importance of robust data preprocessing, visual analysis, and model interpretability in building reliable diagnostic tools for heart disease.



