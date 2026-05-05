# Bank-Marketing

This project builds a binary classification model to predict whether a customer will subscribe to a term deposit using the UCI Bank Marketing Dataset.
The workflow includes:

Data loading & preprocessing

One‑hot encoding of categorical variables

Logistic Regression model training

Model evaluation using 5 key metrics

SHAP explainability for global & individual predictions

This project demonstrates practical skills in EDA, feature engineering, machine learning, and model interpretability.

📂 Dataset
The dataset comes from the UCI Machine Learning Repository and contains marketing campaign data from a Portuguese bank.

Rows: 45,211

Target variable: y (yes/no — subscription to term deposit)

Features: Demographics, call duration, contact type, previous outcomes, etc.

⚙️ Technologies Used
Python

Pandas

Seaborn / Matplotlib

Scikit‑learn

SHAP

🧹 Data Preprocessing
Steps performed:

Loaded CSV with semicolon separator

Inspected structure (head, info, describe)

One‑hot encoded categorical variables using pd.get_dummies()

Converted target variable:

yes → 1

no → 0

Split data into training/testing sets (80/20)

🤖 Model: Logistic Regression
The model was trained using:

python
model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)
max_iter=1000 ensures convergence due to many dummy variables.

📊 Model Evaluation
The following five key metrics were computed:

Metric	Meaning
Accuracy	Overall correctness
Precision	Correct positive predictions
Recall	Ability to detect actual positives
F1 Score	Balance of precision & recall
ROC AUC	Ability to separate classes


These metrics give a complete view of model performance, especially with imbalanced data.

🔍 SHAP Explainability
Two levels of SHAP analysis were performed:

1. Global Feature Importance
A SHAP summary bar plot shows which features influence predictions the most across the entire dataset.

2. Local Explanations (5 Individual Predictions)
Five customers from the test set were analyzed using SHAP force plots.

For each sample, the model output includes:

Prediction (0 or 1)

Probability of subscribing

Top features pushing the prediction up (toward 1)

Top features pushing the prediction down (toward 0)

This provides transparent, human‑interpretable reasoning behind each prediction.

📁 Project Structure
Code
├── bank_marketing_logistic_regression.ipynb
├── README.md
├── data/
│   └── bank-full.csv
└── images/
    ├── shap_summary.png
    ├── shap_force_1.png
    ├── shap_force_2.png
    ├── shap_force_3.png
    ├── shap_force_4.png
    └── shap_force_5.png
🚀 How to Run the Project
Install dependencies:

bash
pip install pandas seaborn matplotlib scikit-learn shap
Run the Python script or Jupyter notebook.

SHAP plots will display automatically.

📝 Key Insights
Call duration is the strongest predictor of subscription.

Customers with previous successful outcomes are more likely to subscribe.

Contacting customers via cellular performs better than telephone.

SHAP reveals clear patterns in customer behavior and model decision‑making.

📬 Author
Toba Olorunsogo  
Data Scientist & Data Engineer
Winnipeg, MB
GitHub: https://github.com/sogotobz  
LinkedIn: https://www.linkedin.com/in/toba-olorunsogo
