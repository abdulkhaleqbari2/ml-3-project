# Heart Disease Prediction Project
A binary classification machine learning project that predicts whether a patient is at risk of Heart Disease based on clinical and demographic attributes — built using Logistic Regression with thorough exploratory data analysis across age, sex, and cholesterol distributions.


📌 Problem Statement
Heart disease is one of the leading causes of death worldwide. Early detection is critical — but manual diagnosis relies heavily on specialist availability and expensive diagnostic tests. This project develops a clinical decision-support model that predicts the likelihood of heart disease from routine medical parameters, enabling faster and more accessible screening.

⚠️ Disclaimer

This project is built for educational purposes only and is not intended for real medical diagnosis. Always consult a qualified medical professional for health decisions.


📊 Dataset
Dataset: Heart Disease Dataset – UCI Machine Learning Repository
File: heart_disease_data.csv
Records: 303 patients | Features: 13 clinical inputs + 1 target
FeatureDescriptionageAge of the patient (years)sexSex (1 = Male, 0 = Female)cpChest pain type (0–3)trestbpsResting blood pressure (mm Hg)cholSerum cholesterol (mg/dl)fbsFasting blood sugar > 120 mg/dl (1 = True, 0 = False)restecgResting ECG results (0–2)thalachMaximum heart rate achievedexangExercise-induced angina (1 = Yes, 0 = No)oldpeakST depression induced by exerciseslopeSlope of the peak exercise ST segmentcaNumber of major vessels colored by fluoroscopy (0–3)thalThalassemia typetarget⭐ 1 = Defective Heart (Disease), 0 = Healthy Heart

🔧 Tech Stack

Language: Python 3
Libraries: Pandas, NumPy, Matplotlib, Scikit-learn
Model: Logistic Regression
Environment: Jupyter Notebook


🚀 Project Workflow
1. Data Loading & Exploration

Loaded the Heart Disease dataset using Pandas
Inspected shape, column names, data types, and descriptive statistics
Confirmed no missing values — dataset was clean and ready for modeling
Verified class distribution: target has two classes — 1 (Disease) and 0 (Healthy)

2. Exploratory Data Analysis (EDA)
🧓 Age Distribution

Plotted a histogram of patient ages to understand the demographic spread
Identified age groups with the highest number of heart disease cases using grouped aggregation

👨‍⚕️ Sex Analysis

Analyzed the sex distribution across the dataset
Computed heart disease case counts broken down by sex — revealing gender-based risk patterns

🩸 Cholesterol Distribution

Compared cholesterol levels between patients with and without heart disease
Overlapping histograms revealed that while cholesterol varies across both groups, patients with disease tend to show distinct distribution patterns

3. Feature Selection & Preprocessing

Selected all 13 clinical features as inputs
Target variable: target (binary — 1: Disease, 0: Healthy)
Train-Test Split: 80% training / 20% testing (random_state=42)

4. Model Training & Evaluation
📊 Logistic Regression

Trained a Logistic Regression classifier — well-suited for binary medical classification tasks
Evaluated on both training and test sets using a full Classification Report (Precision, Recall, F1-Score, Accuracy)


The model demonstrated strong performance on both splits, with no significant overfitting — indicating good generalization to unseen patient data.

5. Prediction on New Patient Data

Built an end-to-end inference pipeline:

Input: 13 clinical values for a new patient
Output: "The person has a Heart Disease" or "The person does not have a Heart Disease"




📂 Project Structure
heart-disease-prediction/
│
├── Project3.ipynb              # Main Jupyter Notebook
├── heart_disease_data.csv      # Dataset
└── README.md                   # Project documentation


💡 Key Learnings

Applied Logistic Regression to a real-world healthcare binary classification problem
Performed domain-driven EDA — analyzing risk factors like age, sex, and cholesterol levels in relation to heart disease
Evaluated model performance using Precision, Recall, and F1-Score — metrics critical in medical ML where false negatives carry high risk
Built a complete patient inference pipeline for real-time predictions on new clinical inputs


🔮 Future Improvements

 Compare with advanced models — Random Forest, XGBoost, and SVM
 Add ROC-AUC curve for a more comprehensive evaluation of classifier performance
 Apply feature importance analysis to identify the most predictive clinical factors
 Deploy as a clinical screening web app using Streamlit or Flask
 Address potential class imbalance using SMOTE or weighted loss
