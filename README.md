# Titanic Survival Prediction: The Pipeline Approach
[![Machine Learning](https://img.shields.io/badge/Domain-Machine%20Learning-blue)](https://scikit-learn.org/)
[![Engineering](https://img.shields.io/badge/Workflow-ML%20Pipelines-orange)](https://scikit-learn.org/stable/modules/compose.html#pipeline)
[![Dataset](https://img.shields.io/badge/Dataset-Titanic%20Kaggle-green)](https://www.kaggle.com/c/titanic)

## 🏗️ Project Overview
This repository demonstrates a highly organized approach to solving the Titanic survival prediction challenge. Instead of manual data cleaning, this project utilizes **Scikit-Learn Pipelines**. 

The goal is to build a robust "assembly line" for data—where raw input goes in, and a prediction comes out—ensuring that every transformation applied to the training data is identically applied to the test data.

---

## 🛠️ Technical Workflow

### 1. Automated Preprocessing
Using `ColumnTransformer`, the pipeline treats different features with specialized logic:
*   **Numerical Features (Age, Fare):** Handling missing values using median imputation to maintain statistical consistency.
*   **Categorical Features (Sex, Embarked):** Converting text labels into numerical vectors using One-Hot Encoding without manual intervention.

### 2. The Scikit-Learn Pipeline
The pipeline consolidates the following into a single object:
*   **Imputation:** Filling in the gaps in the data.
*   **Encoding:** Making the data "machine-readable."
*   **Scaling:** Normalizing features to ensure fair weight distribution.
*   **Classification:** Training a model (e.g., Random Forest or Logistic Regression) on the cleaned data.

### 3. Benefits of this Architecture
*   **Prevents Data Leakage:** Statistics (like the mean age) are only calculated on the training set, never the test set.
*   **Code Cleanliness:** Reduces hundreds of lines of manual preprocessing into a few modular steps.
*   **Deployment Ready:** The entire pipeline can be exported as a `.pkl` file and used directly in a production web app (like Streamlit).

---

## 💻 Tech Stack
*   **Language:** Python 3.9+
*   **Libraries:** Scikit-Learn, Pandas, NumPy
*   **Dataset:** Titanic (Kaggle)
*   **Environment:** Jupyter Notebook

---

## 🚀 Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/titanic-classification-ml-pipelines.git](https://github.com/your-username/titanic-classification-ml-pipelines.git)

2. **Install Dependencies:**
   ```bash
   pip install scikit-learn pandas numpy

3. **Run the Notebook:**

   Execute `ML-using-pipeine.ipynb` to see the automated transformation and training process in action.
