# Project Background
Breast cancer is one of the most prevalent and life-threatening diseases affecting women globally. Early and accurate diagnosis is critical, as it significantly increases survival rates and reduces long-term treatment costs. However, traditional diagnostic methods can be time-consuming, subjective, and prone to inconsistency across practitioners.

This project simulates the work of a **data science team within a healthcare technology company** focused on building an **AI-powered clinical decision support system**. The objective is to assist medical professionals by providing fast, reliable, and interpretable predictions on whether a breast tumor is benign or malignant, based on diagnostic measurements.

The solution aligns with **UN Sustainable Development Goal 3 (Good Health & Well-Being)** by leveraging machine learning to improve early detection, reduce diagnostic errors, and support better healthcare outcomes especially in resource-constrained environments.

**The Python code covering the full machine learning workflow, from data processing to model development, can be found here** [[link](https://github.com/veelvili-tech/Breast-Tumor-Classification-Malignant-vs.-Benign-/blob/main/Full%20Code%20Breast%20Tumor%20Classification.ipynb)].


<img width="845" height="410" alt="Screenshot 2026-02-01 154141" src="https://github.com/user-attachments/assets/4addaa7b-c1e8-4d6f-8b9b-07774fdfa1ef" />

# Business Objective
From a business and healthcare operations perspective, this project aims to:

- Reduce diagnostic uncertainty and human error
- Support early intervention and faster clinical decisions
- Improve consistency in tumor classification
- Demonstrate how AI models can be translated into deployable, real-world tools

# Key Focus Area
Insights and recommendations are provided across the following dimensions:

- Diagnostic Accuracy & Risk Reduction
- Model Reliability & Stability
- Clinical Interpretability
- Deployment & Real-World Usability

# Data Overview
- Dataset: Breast Cancer Wisconsin (Diagnostic) Dataset
- Source: Kaggle (Public Dataset)
- Records: 569 patient samples
- Features: 30 numerical diagnostic measurements
- Target Variable:
      - Malignant (1)
      - Benign (0)
  
The dataset represents real clinical measurements such as tumor radius, texture, perimeter, area, concavity, and symmetry.

# Data Preparation & Quality Checks
To ensure business-grade reliability and model fairness:

- Removed non-predictive identifiers
- Encoded clinical diagnosis into binary outcomes [Malignant = 1 & Benign = 0]
- Addressed class imbalance using SMOTE to avoid biased predictions
- Performed feature scaling to ensure consistency across models
- Conducted correlation analysis to reduce redundancy and overfitting risk

These steps ensure the model learns clinically meaningful patterns, not noise. 

<img width="845" height="410" alt="Screenshot 2026-02-01 153843" src="https://github.com/user-attachments/assets/955373d6-5a70-4a24-8708-e933614ab4ef" />


# Modeling Approach (High-Level)
Three machine learning models were evaluated:

- Logistic Regression – transparent and interpretable baseline
- Random Forest – robust ensemble model with strong generalization
- XGBoost – high-performance gradient boosting model

Models were assessed using accuracy, precision, recall, F1-score, and cross-validation stability.


# Executive Summary (Key Findings)
If a healthcare stakeholder were to take away three key insights, they would be:

- Machine learning can classify breast tumors with >97% accuracy, demonstrating strong potential as a diagnostic support tool.
- Random Forest delivers the most stable and reliable performance, making it suitable for real-world clinical deployment.
- Model interpretability matters — feature importance insights help build clinician trust and adoption.
<img width="845" height="410" alt="Screenshot 2026-02-01 165009" src="https://github.com/user-attachments/assets/cfdf6ff9-6859-4526-b58a-42cfab31860e" />

# Insights Deep Dive
### 1. Diagnostic Accuracy & Patient Risk
- All models achieved very high recall, ensuring malignant cases are rarely missed.
- XGBoost achieved perfect recall but at the cost of higher false positives.
- Random Forest balanced recall and precision, minimizing both missed cancers and unnecessary alarms.

**Business Impact:**
Reduces delayed treatments while avoiding excessive follow-up procedures.

### 2. Model Stability & Reliability
- Cross-validation showed Random Forest had the lowest variance across multiple data splits.
- Stability is essential in medical environments where data distributions may shift.

**Business Impact:**
Ensures consistent performance across hospitals, populations, and devices.

### 3. Interpretability & Clinical Trust
- Random Forest provides feature importance rankings, highlighting which tumor characteristics most influence predictions.
- Supports transparency and explainability in medical decision-making.

**Business Impact:**
Higher adoption likelihood among clinicians and regulators.

### 4. Deployment & Accessibility
- The **Random Forest model** was deployed using Streamlit, creating an interactive web application.
- Users can input diagnostic values and receive instant predictions.

**Business Impact:**
Transforms a machine learning model into a usable healthcare product, not just a technical experiment.

<img width="845" height="410" alt="Screenshot 2026-02-01 165134" src="https://github.com/user-attachments/assets/0e1c7424-42bf-4c91-8dd5-18975fcd11ca" />

# Real-World Applications

- **Clinical Decision Support**: Assist doctors during diagnosis
- **Medical Training**: Educational tool for students and practitioners
- **Telemedicine**: Remote screening support
- **Healthcare AI Prototyping**: Foundation for EMR integration

# Recommendations
Based on the findings, we recommend:

- Deploying Random Forest as the primary production model
- Integrating Explainable AI (SHAP/LIME) for clinician transparency
- Expanding validation using real hospital data
- Migrating to scalable cloud platforms (AWS / Azure) for enterprise readiness
- Exploring EMR system integration for workflow adoption

# Business & Social Impact

This project demonstrates how data science can be translated into a real, deployable healthcare solution, supporting early detection, operational efficiency, and better patient outcomes, directly contributing to SDG 3: Good Health & Well-Being.

# DEPLOYMENT 

### Deployment Architecture
- Frontend: Streamlit Web Interface
- Backend: Pre-trained Random Forest Classifier
- Hosting: Replit Cloud Environment

**User Flow:**
Clinical Input → Model Inference → Clear Prediction Output

This project includes a Streamlit-based web application for classifying breast tumors (benign vs. malignant) using trained machine learning models. The folder structure supports both backend model logic and frontend user interface integration, making it suitable for deployment on platforms like Streamlit Cloud, Replit, or local servers.

# Project Structure
.streamlit/	
Configuration for Streamlit UI, including layout and theming.

assets/	
Static assets such as images or data files used in the app.

attached_assets/	
Additional files, possibly icons or supporting visuals.

app.py	
Main entry point for the Streamlit app – runs the frontend interface.

app_fixed.py, app.py.bak	
Alternative or backup versions of the app file.

model.py	
Contains the machine learning model loading and prediction logic.

utils.py	
Helper functions for data processing and utility tasks.

model_performance.py	
Script to analyze and visualize model evaluation metrics.

breast_cancer_awareness.py	
Likely contains visual or educational content related to awareness.

generated-icon.png	
Icon for branding in the app UI.

pyproject.toml, uv.lock	
Package management and dependency locking.

.replit	
Replit-specific configuration for deployment.

# How to Run 
### Local Setup

Install dependencies

pip install -r requirements.txt

Run the app

streamlit run app.py

### Deploy to Streamlit Cloud

Push your project to GitHub.

Go to Streamlit Cloud.

Connect your repo and select app.py as the entry file.

Configure .streamlit/config.toml for appearance or caching if needed.

### Replit Deployment

This project is also Replit-ready (.replit and uv.lock included).

Simply upload to Replit and run. Streamlit UI will launch automatically.

# Purpose

This deployment enables users to interactively classify tumor data through a friendly web interface. It demonstrates the integration of ML models into real-time applications and promotes awareness in medical AI.



