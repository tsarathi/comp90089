# COMP90089-Machine Learning For Health-Group Project-Group17

## Table of Repository Contents
1. [Team Contract](ML4Health_TeamContract_17.pdf)
2. [Project Proposal](ML4Health_proposal_Group17.pdf)
3. [Cohort Extraction and Exploratory Data Analysis](Data_Handling.ipynb)
4. [Data Processing Generic](Process_Data_Generic.ipynb)
5. [Machine Learning Modelling](ML_Models.ipynb)
6. [Feature Importance Analysis](Feature_Importance_ISP_Dataset.ipynb)
7. [Pre-created Dataset of Full Cohort](full_cohort.csv)
8. [Environment Setting Requirements](requirements.txt)

## Project Details

### Objective
This study aims to predict 365-day hospital readmission for ischemic stroke
patients using machine learning models and to identify key predictive features to inform
clinical decision-making.

### Materials and Methods
We used the MIMIC-IV dataset to build and evaluate three
ML models: Random Forest, XGBoost, and PCA Clustering. Due to the class imbalance
in readmission cases, we employed SMOTE oversampling for Random Forest to improve
performance. Hyperparameters for each model were optimized using grid search with
cross-validation, and feature importance was analyzed using clustering and permutation
methods.

### Results
The models achieved moderate performance, with AUC values of 0.64 for Random Forest and 0.78 for XGBoost, indicating limited discriminative ability. While SMOTE improved class balance, the models still struggled to achieve high predictive accuracy. Clustering analysis identified features such as length of stay, troponin T levels, and maximum systolic BP as influential in predicting readmission. Permutation importance for Random Forest highlighted the complex interplay of features affecting patient outcomes.

## Steps to Implement Codes
* Require access to MIMIC-IV database and finish Bigquery settings via the link: [MIMIC-IV Access](https://physionet.org/content/mimiciv/2.2/)
* Set the environment and versions according to the [Environment Setting Requirement](requirements.txt).
* Run the code of [Cohort Extraction and Exploratory Data Analysis](Data_Handling.ipynb), save the full cohort dataset, or use the [Pre-created Dataset of Full Cohort](full_cohort.csv).
* Input Dataset file and apply it by running [Machine Learning Modelling](ML_Models.ipynb), which contains data processing, modelling, evaluation and analysis.
* Run [Feature Importance Analysis](Feature_Importance_ISP_Dataset.ipynb).

## Conclusion
Our results have highlighted the complexity involved in modeling clinical data. In addition, our struggles to establish a cohort that is large, complete, and relevant clinically proved deeply challenging. Prior literature on different datasets suggested ML accuracy for stroke readmission obtained only moderate results. Our findings were in line with this.

**Warm Regards**

Group 17
