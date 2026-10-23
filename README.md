# 💳 Credit Card Fraud Detection

An end-to-end **Machine Learning classification project** focused on detecting potentially fraudulent credit card transactions.

## 📌 Project Overview

Credit card fraud detection is a highly imbalanced binary classification problem. This project demonstrates a practical ML workflow covering data analysis, preprocessing, model development, evaluation, and fraud prediction.

### Target Variable

| Class | Meaning |
|---|---|
| `0` | Legitimate Transaction |
| `1` | Fraudulent Transaction |

---

## 🎯 Objectives

- Perform Exploratory Data Analysis (EDA)
- Analyze class imbalance
- Clean and preprocess transaction data
- Prepare features for Machine Learning
- Build classification models
- Evaluate model performance
- Understand Precision, Recall and F1-Score
- Detect potentially fraudulent transactions

---

## 🔄 Machine Learning Workflow

```text
Credit Card Dataset
        ↓
Data Loading
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis
        ↓
Class Imbalance Analysis
        ↓
Data Preprocessing
        ↓
Model Development
        ↓
Model Evaluation
        ↓
Fraud / Legitimate Prediction
```

---

## 📊 Dataset

This project uses the **Credit Card Fraud Detection** dataset from Kaggle.

### Dataset Link

👉 **Kaggle:**  
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

The commonly used MLG-ULB dataset contains **284,807 transactions** and **492 fraudulent transactions**, making class imbalance one of the main challenges.

The dataset includes anonymized features `V1` to `V28`, along with `Time`, `Amount`, and the target variable `Class`.

> ⚠️ The dataset is not included in this repository because of its large file size. Download `creditcard.csv` from Kaggle when running the project locally.

---

## ⚠️ Class Imbalance

Fraudulent transactions are extremely rare compared with legitimate transactions. Therefore, **accuracy alone should not be used as the main evaluation metric**.

Important metrics include:

- **Precision**: How many predicted fraud transactions are actually fraud?
- **Recall**: How many actual fraud transactions were detected?
- **F1-Score**: Balance between Precision and Recall
- **ROC-AUC**: Ability to distinguish between classes
- **Confusion Matrix**: Detailed prediction errors

For fraud detection, Recall is particularly important because missing an actual fraudulent transaction can be costly.

---

## 🔍 Exploratory Data Analysis

The project can include:

- Dataset shape and structure
- Data types
- Missing-value analysis
- Duplicate analysis
- Statistical summary
- Fraud vs legitimate transaction distribution
- Transaction amount analysis
- Feature correlation
- Outlier analysis
- Class imbalance visualization

---

## 🧹 Data Preprocessing

Typical preprocessing steps include:

- Missing-value checking
- Duplicate checking
- Feature selection
- Feature scaling where required
- Separating features and target
- Train-test splitting
- Handling class imbalance where required

---

## 🤖 Machine Learning

The project treats fraud detection as a **binary classification problem**.

Suitable algorithms for this problem can include:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting / XGBoost
- Other classification algorithms

The final model should be selected according to the actual evaluation results produced by the project.

---

## 📈 Model Evaluation

| Metric | Purpose |
|---|---|
| Accuracy | Overall prediction correctness |
| Precision | Correctness of fraud alerts |
| Recall | Ability to detect actual fraud |
| F1-Score | Balance between Precision and Recall |
| ROC-AUC | Class discrimination |
| Confusion Matrix | Detailed prediction breakdown |

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Machine Learning
- Statistical Analysis

---

## 📂 Suggested Project Structure

```text
Credit-Card-Fraud-Detection-/
│
├── Data/
│   └── creditcard.csv
│
├── Notebook/
│   └── credit_card_fraud_detection.ipynb
│
├── Model/
│   └── trained_model_files
│
├── Output/
│   ├── plots/
│   └── reports/
│
├── requirements.txt
└── README.md
```

> Adjust the folder/file names if your repository uses a different structure.

---

## 💻 Run Locally

### 1. Clone Repository

```bash
git clone https://github.com/maheshloharr/Credit-Card-Fraud-Detection-.git
```

### 2. Navigate to Project

```bash
cd Credit-Card-Fraud-Detection-
```

### 3. Create Virtual Environment

```bash
python -m venv venv
```

### 4. Activate Environment

**Windows**
```bash
venv\Scripts\activate
```

**macOS / Linux**
```bash
source venv/bin/activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

### 6. Download Dataset

Download `creditcard.csv` from:

https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Then place it in the project's data folder before running the notebook or training workflow.

---

## 📚 Key Learning Outcomes

- End-to-end Machine Learning workflow
- Exploratory Data Analysis
- Imbalanced classification
- Data preprocessing
- Feature engineering
- Classification algorithms
- Model evaluation
- Precision, Recall and F1-Score
- Confusion Matrix analysis
- Fraud detection concepts
- Python-based ML implementation

---

## ⭐ Key Highlights

- 💳 Real-world fraud detection use case
- 📊 Highly imbalanced classification problem
- 🧹 Data preprocessing workflow
- 📈 EDA and visualization
- 🤖 Machine Learning classification
- 🎯 Focus on meaningful fraud-detection metrics
- 🐍 Python implementation
- 📓 Jupyter Notebook workflow
- 📦 Kaggle dataset integration

---

## 🔗 Project Links

### 💻 GitHub Repository

https://github.com/maheshloharr/Credit-Card-Fraud-Detection-

### 📦 Dataset

https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

---

## 👨‍💻 Author

**Mahesh Lohar**

Data Science | Machine Learning | Python | SQL | Power BI

---

## 📌 Disclaimer

This project is intended for **educational and portfolio purposes**. The dataset contains anonymized transaction features and does not provide access to actual cardholder identities or sensitive card information.

If you find this project useful, feel free to ⭐ the repository.
