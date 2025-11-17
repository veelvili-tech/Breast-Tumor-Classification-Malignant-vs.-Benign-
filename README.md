# Classification-of-Breast-Tumors

INTRODUCTION 

This repository contains all the steps for building a machine learning model to classify breast tumors as benign or malignant using structured medical data. It includes data preprocessing, exploratory analysis, feature selection, model training, evaluation, and performance visualization to support accurate and explainable predictions in healthcare.

# NOTEBOOK_FINAL

Project Overview

The notebook walks through the full process of developing a classification model using supervised learning techniques. It is structured to support both beginners and intermediate learners who want to understand how to build and evaluate models in Python.

# Key Components
1. Data Preprocessing
   
Handling missing values, encoding categorical variables, feature scaling.

3. Exploratory Data Analysis (EDA)
   
Visualizations and statistical summaries to understand data distribution and relationships.

5. Feature Selection
   
Identifying key predictors that contribute most to classification.

7. Model Building
   
Training multiple models including Logistic Regression, Random Forest, and XGBoost

9. Model Evaluation
    
Comparing performance using accuracy, precision, recall, F1-score, confusion matrix, and ROC-AUC.

11. Cross-Validation
    
Ensuring generalizability with k-fold validation techniques.

# DEPLOYMENT 
This project includes a Streamlit-based web application for classifying breast tumors (benign vs. malignant) using trained machine learning models. The folder structure supports both backend model logic and frontend user interface integration, making it suitable for deployment on platforms like Streamlit Cloud, Replit, or local servers.

# Project Structure
.streamlit/	Configuration for Streamlit UI, including layout and theming.

assets/	Static assets such as images or data files used in the app.

attached_assets/	Additional files, possibly icons or supporting visuals.

app.py	Main entry point for the Streamlit app – runs the frontend interface.

app_fixed.py, app.py.bak	Alternative or backup versions of the app file.

model.py	Contains the machine learning model loading and prediction logic.

utils.py	Helper functions for data processing and utility tasks.

model_performance.py	Script to analyze and visualize model evaluation metrics.

breast_cancer_awareness.py	Likely contains visual or educational content related to awareness.

generated-icon.png	Icon for branding in the app UI.

pyproject.toml, uv.lock	Package management and dependency locking.

.replit	Replit-specific configuration for deployment.

# How to Run (Local Setup)

Install dependencies

pip install -r requirements.txt

Run the app

streamlit run app.py

# Deploy to Streamlit Cloud

Push your project to GitHub.

Go to Streamlit Cloud.

Connect your repo and select app.py as the entry file.

Configure .streamlit/config.toml for appearance or caching if needed.

# Replit Deployment

This project is also Replit-ready (.replit and uv.lock included).

Simply upload to Replit and run. Streamlit UI will launch automatically.

# Purpose

This deployment enables users to interactively classify tumor data through a friendly web interface. It demonstrates the integration of ML models into real-time applications and promotes awareness in medical AI.



