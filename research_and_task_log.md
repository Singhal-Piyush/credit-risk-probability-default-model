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

- **Load the dataset** : Dataset is huge with about 5.8 GB of on device ussage.
    - 145 features and 2 Million plus observations.

 - **Meta Data of Dataset** : 145 features are present in the dataset which makes it difficult to analyze the dataset for null values, unique categories for categorical feature.
    - With the help of the datatset_meta_data(dataset) function which helps to extract various details like non-null values, null_values count, percentage of null values, 
    unique catogeries for categorical features and it's datatype. 
    - Helped to view in dataframe format made it easy for analyzing the features at one go. 

    **Task**
        - [x] Duplicate values.[Completed - 2025-08-14 ]
        - [] Correct Datatypes. [Completed - ]
        - [] Converting feature into more meaningful format. [Completed - ]
        - [] Missing values. [Completed - ]

### 📅 2025-08-14

- **Duplicate Values** - There were no duplicate values in the loan dataset.

- **Analysis of Null values** - According to the output of the dataset_meta_data() function, dataset has around 78 features with missing or null values. 
    - we can club these features depending on the no. of missing values or percentage of missing values. 
    - As this model will be used to evaluate the borrower before the issuing of the loan or credit line, therefore much of the features with missing values can be dropped. 

- **Identifying the Target Column** - We are making model to predict loan_status. 
    - 'loan_status" variable have too make categories. 
    - we have selected to predict only Fully Paid and Charged Off categories.
    - Class imbalance was observed and has to be taken care off.

- **Feature Selection** -  


    **Task**
    - [x] Identify the Target Column and value distribution [Completed - 2025-08-14]
    - [] Class imbalance issue in the loan dataset. [completed - ]
    - [] Identify the feature that are tracked after the issuance of the loan.  [Completed - ]
    - [] Remove these features which are tracked after issusing loan. [Completed - ]
    - [] Drop the features with too many Null values. [Completed - ]


## ✅ Completed Tasks
- **2025-08-13**
    - [x] CSV File Compression - Dropped the idea of crompession file as the resulted file is still larger than 100MB.[Completed - 2025-08-13]
    - [x] Load dataset. [Completed - 2025-08-13]
    -  [x] Get the basic details about the dataset-  Completed using the dataset_meta_data() function. [completed - 2025-08-13]

- **2025-08-14**
    - [x] Duplicate values. [completed - 2025-08-14]
    - [x] Identify the Target Column [Completed - 2025-08-14]
    - 


## ⏳ Pending Tasks

- [] Correct Datatypes (To be handle during EDA) []
- [] Converting feature into more meaningful format. (Handle During EDA) []
- [] Missing values.
- [] Identify the feature that are tracked after the issuance of the loan.  [Completed - ]
- [] Remove these features which are tracked after issusing loan. [Completed - ]
- [] Drop the features with too many Null values. [Completed - ]
- [] Class imbalance issue in the loan dataset. [completed - ]


---

## 🧠 Research Ideas
- Check how I want to handle the imbalance dataset issue in the loan dataset.


