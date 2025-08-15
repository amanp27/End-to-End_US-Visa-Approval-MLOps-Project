# 🛂 End-to-End US Visa Approval Prediction — MLOps Project

## 📌 Why I Chose This Project

**Problem Statement:**  
The US visa approval process is complex, involving multiple factors such as applicant qualifications, employer details, job category, and historical approval rates. Manual review of applications is time-consuming and prone to bias or inconsistency. For applicants, uncertainty creates stress and delays in career or personal plans.

**Proposed Solution:**  
This project predicts the likelihood of US visa approval using historical data. I designed a **fully automated MLOps pipeline** to handle data processing, model training, deployment, and monitoring in real time — ensuring the system remains reliable even as new data trends emerge.

**Why it’s Important:**  
- Speeds up decision support for applicants and authorities  
- Demonstrates **industry-grade MLOps skills**  
- Bridges **data science** and **software engineering** best practices

---

## 🚀 Project Highlights

- **End-to-End ML Pipeline**: Data ingestion → validation → transformation → model training → evaluation → model pusher
- **Cloud Deployment**: AWS S3 (data & model storage), ECR (Docker image registry), EC2 (application hosting)
- **Containerization**: Dockerized application for consistent environments
- **CI/CD Automation**: GitHub Actions for continuous integration and deployment
- **Model Monitoring**: Evidently AI for detecting **data drift**
- **Modular Architecture**: Each stage is isolated and reusable

---

## 🏗 Project Architecture

```mermaid
flowchart LR
    A[Data Source] --> B[Data Ingestion]
    B --> C[Data Validation]
    C --> D[Data Transformation]
    D --> E[Model Training]
    E --> F[Model Evaluation]
    F --> G[Model Pusher]
    G --> H[AWS S3/ECR/EC2 Deployment]
    H --> I[Monitoring with Evidently AI]
```

## Project Structure
```
End-to-End_US-Visa-Approval-MLOps-Project/
│
├── .github/workflows/          # CI/CD pipelines
├── notebooks/                  # Experimentation & EDA notebooks
├── us_visa/
│   ├── components/              # Pipeline stages (ingestion, validation, etc.)
│   ├── configuration/           # AWS/MongoDB configs
│   ├── pipelines/               # End-to-end orchestrators
│   ├── utils/                    # Utility functions
│
├── Dockerfile                   # Containerization
├── requirements.txt             # Dependencies
├── setup.py                     # Package setup
├── app.py / demo.py              # App entry points
└── README.md
```

## 🛠 Tech Stack
* Language: Python
* Data Storage: MongoDB, AWS S3
* Modeling: Scikit-learn, Pandas, NumPy
* Containerization: Docker
* Cloud: AWS S3, ECR, EC2
* Orchestration & CI/CD: GitHub Actions
* Monitoring: Evidently AI

## Workflow

1. Experimentation in Notebooks
    * Data exploration, feature engineering, and initial model selection

2. Pipeline Components

    * Data Ingestion: Fetch raw data from MongoDB / S3
    * Data Validation: Schema & missing values checks
    * Data Transformation: Encoding, scaling, and feature prep
    * Model Training: Train ML models & save best version
    * Model Evaluation: Check accuracy, precision, recall, F1
    * Model Pusher: Upload trained model to S3 & trigger deployment

3. Dockerization
    * Create image, push to AWS ECR

4. Deployment
    * Launch container on AWS EC2

5. Monitoring
    * Use Evidently AI to track data drift and trigger retraining

## Model Monitoring (Evidently AI)

The system automatically generates reports on:
    * Data drift
    * Target drift
    * Feature distribution changes

This ensures model reliability even as new visa applications deviate from training data.


## 🎯 Key Takeaways
* Demonstrates MLOps Maturity — covers full lifecycle, automation, and monitoring
* Cloud-Native — deployable on AWS with scalable infrastructure
* Recruiter-Friendly Skills — combines DS, DevOps, and software engineering best practices
* Production-Ready — automated pipelines mean minimal manual intervention
