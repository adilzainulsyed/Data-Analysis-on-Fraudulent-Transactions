Fraud Detection Data Analytics Project
Project Overview: 

This project performs a complete data analytics workflow on a Fraud Detection dataset.
It applies essential preprocessing and statistical analysis techniques to identify relationships between transaction features and fraudulent activity.

The analysis includes:
    1. Data Cleaning
    2. Data Integration
    3. Data Reduction
    4. Data Normalization
    5. Hypothesis Testing
    6. Data Visualization

1. Data Cleaning

    -> Removed duplicate and missing records.
    -> Handled inconsistent or null values in numerical and categorical columns.
    -> Checked and handled outliers in numeric columns using the Interquartile Range (IQR)   method.
    -> Ensured data types were correctly assigned (e.g., isFraud, isFlaggedFraud as integers).

2. Data Integration

    -> Two datasets were integrated:
    -> fraud_detection.csv – main transaction dataset.
    -> customer_info.csv – additional data such as customer age, account type, region, credit score, and KYC verification.
    -> Integration was done using a left join

3. Data Reduction

    -> Selected relevant columns for fraud prediction and analysis (e.g., amount, type, oldbalanceOrg, newbalanceOrig, isFraud, kyc_verified).
    -> Dropped redundant or non-informative features.
    -> Used correlation and variance checks to identify less useful features.

4. Data Normalization

    -> Applied Min-Max scaling on continuous columns (amount, oldbalanceOrg, newbalanceOrig, etc.) to bring values into the range [0, 1].
    -> Ensured no feature dominated due to scale differences.

5. Hypothesis Testing

    -> A Chi-square test for independence was used to test whether KYC verification is related to fraud occurrence.
    -> Hypotheses:

        H₀: Fraud occurrence is independent of KYC verification.

        H₁: Fraud occurrence depends on KYC verification.
    
    -> Test Used: Chi-square test of independence
    -> Decision Rule:
        If p-value < 0.05, reject H₀ and conclude that fraud occurrence depends on KYC verification.

6. Data Visualization

    -> Visualizations were created using Matplotlib and Seaborn, including:

    -> Fraud vs Non-Fraud transaction counts

    -> Distribution of transaction amounts

    -> Correlation heatmap

    -> KYC verification vs Fraud occurrence comparison

Summary of Findings

    -> Fraudulent transactions show distinct behavior in transaction type and amount.
    -> The Chi-square test indicated (if p < 0.05) that fraud occurrence are independent of KYC verification.

Technologies Used

    Python 3.11+

    Pandas

    NumPy

    Matplotlib

    Seaborn

    SciPy

    scikit-learn

Author : Adil Zainul Syed
