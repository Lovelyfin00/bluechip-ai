# 🏦 Loan Prediction Model  

## 🚀 2024 Bluechip AI Data Science Hackathon  

This project was developed as part of the **Bluechip AI Data Science Hackathon**. The goal is to build a **Loan Prediction Model** using **Random Forest Classification** to determine whether an applicant will be approved for a loan based on various features such as income, credit history, and demographic details.  

---

## 📂 Dataset  

The project uses two datasets:  
1. **Train.csv** – Used for training the model.  
2. **Test.csv** – Used for testing the model.  

### **Features in the Dataset**  

| Feature | Description |
|---------|------------|
| `Loan_ID` | Unique identifier for a loan |
| `Gender` | Applicant's gender (Encoded: 0 = Male, 1 = Female) |
| `Married` | Marital status (Encoded: 0 = No, 1 = Yes) |
| `Dependents` | Number of dependents |
| `Education` | Education level (Encoded: 0 = Not Graduate, 1 = Graduate) |
| `Self_Employed` | Self-employment status (Encoded: 0 = No, 1 = Yes) |
| `ApplicantIncome` | Income of the applicant |
| `CoapplicantIncome` | Income of the co-applicant |
| `LoanAmount` | Loan amount applied for |
| `Loan_Amount_Term` | Term of the loan (in months) |
| `Credit_History` | Credit history status (Encoded: 1 = Good, 0 = Bad) |
| `Property_Area` | Area where the property is located (Encoded: 0 = Rural, 1 = Semiurban, 2 = Urban) |
| `Loan_Status` | Target variable (Encoded: 0 = No, 1 = Yes) |

---

## 🔍 Steps in the Project  

### **1️⃣ Data Collection**  
- The training dataset (`Train.csv`) and test dataset (`Test.csv`) are loaded into Pandas DataFrames.  


### **2️⃣ Exploratory Data Analysis (EDA)**  
- **Checking Data Structure:** `train_df.info()`, `test_df.info()`
- **Summary Statistics:** `train_df.describe()`, `test_df.describe()`
- **Missing Values Analysis:** `train_df.isna().sum()`, `test_df.isna().sum()`
- **Data Visualization:** Seaborn plots are used to understand distributions of key features.  

### **3️⃣ Data Preprocessing**  
- **Handling Missing Values**  
  - Filled missing values in `Gender`, `Married`, `Dependents`, `Self_Employed`, `LoanAmount`, `Loan_Amount_Term`, and `Credit_History` using **mode or median**.
  
- **Feature Engineering**  
  - Created a new feature: `Total_Income = ApplicantIncome + CoapplicantIncome`.  

- **Encoding Categorical Features**  
  - Converted categorical values (`Loan_Status`, `Gender`, `Education`, `Married`, `Self_Employed`) into numerical values.  

### **4️⃣ Model Training**  
- **Splitting Data**  
  - Training dataset split into **train (80%) and test (20%)**.  

- **Random Forest Classifier**  
  - A **RandomForestClassifier** is used for loan prediction.  
  - Model performance is evaluated using **confusion matrix, accuracy score, and ROC curve**.  

### **5️⃣ Model Evaluation**  
- **Accuracy Score**
- **Confusion Matrix**
- **Classification Report**
- **ROC Curve**

## 📊 Results & Insights  
- The model effectively predicts loan approval with **high accuracy**.  
- **Credit_History** and **Total_Income** are key indicators of loan approval.  
- The confusion matrix and classification report show **balanced performance** with minimal misclassification.  
- ROC curve analysis indicates a **strong predictive capability**.  
- Further improvements can be made by **hyperparameter tuning** and **feature engineering**.  

---

## 🛠️ Future Improvements  
- Experiment with **other ML models** like **XGBoost, LightGBM, or Neural Networks**.  
- Improve feature selection using **Principal Component Analysis (PCA)** or **Recursive Feature Elimination (RFE)**.  
- **Hyperparameter tuning** with **GridSearchCV** or **RandomizedSearchCV** for better optimization.  
- Use **cross-validation techniques** to avoid overfitting and improve generalization.  
- Enhance data preprocessing by handling outliers and testing **scaling techniques (StandardScaler, MinMaxScaler)**.  
