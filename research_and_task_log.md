Following is the folder structure for the credit risk modelling project.

credit_risk_probability_default_model/

|
├── notebooks/
│   ├── 01_credit_risk_data_exploration.ipynb
│   ├── 02_credit_risk_data_preprocessing.ipynb
│   ├── 03_credit_risk_feature_engineering.ipynb
│   ├── 04_credit_risk_model_training_and_evaluation.ipynb
│
├── final_notebook/
│   └── credit_risk_case_study.ipynb
│
├── data/
│   ├── raw/
|   |   ├── DataDictionary.xlsx
|   |   ├── Loan_Dataset.csv
│   ├── processed/
|   |   ├── Loan_Dataset.csv
│
├── README.md



# Research & Progress Log

### 📅 2025-08-13

- **CSV File Compression** : Raw Dataset is of more than 1 GB, look for better compression like gzip, bzip2.
    - gzip resulted in 326MB and bzip2 resulted in 240MB file. Both cannot be pushed
    to github.
    - command used in bash terminal of git
        gzip -k loan_dataset.csv
        &&
        bzip2 -k loan_dataset.csv
    - -k resulted in keeping the original final and creating the desired compressed 
    version.
    - running dataset.to_csv('dataset.csv.gz', index = False, compression = 'gzip') takes more time than the bash terminal command.

 - **Meta Data of Dataset** : 145 features are present in the dataset which makes it difficult to analyze the dataset for null values, unique categories for categorical feature.
    - With the help of the datatset_meta_data(dataset) function which helps to extract various details like non-null values, null_values count, percentage of null values, 
    unique catogeries for categorical features and it's datatype. 
    - Helped to view in dataframe format made it easy for analyzing the features at one go. 

### 📅 2025-08-14

- **Analysis of Null values** - According to the output of the dataset_meta_data() function, dataset has around 

## ✅ Completed Tasks
- [x] CSV File Compression - Dropped the idea of crompession file as the resulted file is still larger than 100MB.
- [x] Load dataset
- [x] Get the basic details about the dataset-  Completed using the dataset_meta_data() function.
- [x]

## ⏳ Pending Tasks
- []
- []
- []

---

## 🧠 Research Ideas


