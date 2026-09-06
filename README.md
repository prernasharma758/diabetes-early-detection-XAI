# diabetes-early-detection-XAI
AI-Based Early Detection of Diabetes Complications using XGBoost, Random Forest, and SHAP.
Topic : AI-Based Early Detection of Diabetes Complications: Balancing Accuracy and Interpretability
This repository contains the official implementation, datasets, and Explainable AI (XAI) framework presented in our research paper on early diabetes complication risk screening.
Project Abstract :
Diabetes is a critical global health concern, particularly prominent in India, where nearly 40% to 50% of cases are left undiagnosed until later stages. This research directly addresses the classic performance-interpretability trade-off in healthcare AI. We propose a hybrid machine learning optimization framework validated across two distinct data environments: the standard PIMA Indian dataset and an advanced clinical dataset from Medical City Hospital.Our findings show that when the machine learning models are provided with advanced laboratory biomarkers, tree-based ensemble frameworks achieve peak accuracy, with Random Forest reaching 99.00% and XGBoost achieving 98.50%. To transition these high-performing "black-box" models into trustworthy clinical systems, we integrated the SHAP (SHapley Additive exPlanations) framework. This allows medical professionals to clearly understand the underlying logic behind each prediction.
Key Research Findings :
Our experimental results highlight how model performance and diagnostic reliance shift when transitioning from basic features to advanced multi-system clinical biomarkers:
PIMA Indian Dataset: All models performed similarly, with baseline accuracies ranging between 72% and 75%. In this basic dataset, Glucose Concentration was identified by SHAP as the top explanatory marker.
Medical City Dataset: The introduction of comprehensive clinical profiles caused a massive jump in performance. Logistic Regression achieved 94.00%, Decision Tree hit 96.50%, while Random Forest topped the matrix at 99.00%.
Clinical Alignment: With the advanced dataset, the model automatically shifted its priority from highly fluctuating daily sugar levels to long-term health indicators like HbA1c and Cholesterol. This computational behavior aligns perfectly with actual medical science and clinical guidelines.
Proposed Methodology :
Data Pipeline: Text columns (like Gender) are processed using LabelEncoder. Missing data points are handled using Median value imputation, and all features are scaled using StandardScaler prior to an 80/20 train-test split.
Model Selection: The architecture balances simple, highly transparent models (Logistic Regression, Decision Trees) against complex tree ensembles (Random Forest, XGBoost) to evaluate performance across different data environments.
Explainable AI Framework: SHAP calculates mathematical attribution scores for parameters like HbA1c and BMI, ensuring the model's decisions can be validated and trusted by doctors.
Repository Structure :
To keep the project clean and organized, the files are structured as follows:
data/: Contains the CSV datasets used for cross-repository training.
notebooks/: Stores the Jupyter notebooks tracking data preprocessing, model comparisons, and SHAP explainability analyses.
Main Directory: Features the core documentation (README) and the open-source usage permissions (LICENSE).
 Future Roadmap :
Connect the predictive machine learning engine directly to live hospital network databases.
Integrate additional multi-system biometric features, such as kidney damage and heart-related indicators.
Develop and deploy a lightweight, real-time Streamlit web dashboard to support remote diagnostics via mobile phones in rural health screening camps.
