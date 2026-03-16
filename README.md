#  Cancer Severity Level Prediction

## Overview
Applyings various Machine Learning classification algorithms to predict the severity level of cancer in patients based on a range of medical and demographic features. The goal is to accurately classify the cancer level as **Low, Medium, or High** to assist in early detection and risk stratification.

## 📊 Dataset
* **Source:** [Cancer Patients Data (Kaggle)](https://www.kaggle.com/datasets/rishidamarla/cancer-patients-data/data)
* **Target Variable:** `Level` (Categorical: Low, Medium, High)
* **Features:** Includes multiple health indicators and lifestyle factors.

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Processing:** Pandas, NumPy
* **Data Visualization:** Seaborn, Matplotlib
* **Machine Learning:** Scikit-Learn, Imbalanced-Learn (SMOTE/Oversampling)

## ⚙️ Methodology & Pipeline
1. **Data Preprocessing:** * Handled missing values and dropped irrelevant identifiers (`Patient Id`, `index`).
   * Encoded the ordinal target variable (`Level`) using `LabelEncoder`.
2. **Handling Class Imbalance:**
   * Applied `RandomOverSampler` strictly to the training data to ensure the models learned minority classes without bleeding data into the test set.
3. **Model Selection & Training:**
   * Evaluated six different classification algorithms: Logistic Regression, Support Vector Machine (SVM), Random Forest, K-Nearest Neighbors (KNN), Naive Bayes (NB), and Decision Tree.
4. **Rigorous Evaluation:**
   * Checked Precision, Recall, and F1-scores using Classification Reports.
   * Analyzed False Positives/Negatives via Confusion Matrices.
   * Validated model stability using **Stratified 5-Fold Cross-Validation**.

## 🏆 Model Performance (Cross-Validation Results)
The models were evaluated using Stratified 5-Fold CV to ensure robustness across different data splits.

| Model | Mean CV Accuracy | Standard Deviation |
| :--- | :--- | :--- |
| **Random Forest** | **1.00** | **0.00** |
| **Decision Tree** | **1.00** | **0.00** |
| **K-Nearest Neighbors** | **1.00** | **0.00** |
| **Logistic Regression** | 0.99 | 0.01 |
| **SVM** | 0.97 | 0.01 |
| **Naive Bayes** | 0.89 | 0.01 |

*Note: Random Forest, Decision Tree, and KNN achieved near-perfect generalization on this specific dataset.*

## 🚀 How to Run Locally

1. Clone this repository:
   ```bash
   git clone https://github.com/naham6/cancer-level-prediction.git
2. Navigate to the Project Folder:
   ```bash
   cd cancer-level-prediction
3. Install Dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
   
