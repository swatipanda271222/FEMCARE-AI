# FemCare AI – Intelligent PMOS Risk Assessment Platform

<p align="center">
  <img src="public/favicon.ico" width="120" alt="FemCare AI Logo">
</p>

An AI-powered full-stack healthcare application designed to assist in the early screening of **Polycystic Ovarian Morphological Syndrome (PMOS)** (formerly widely referred to as **PCOS**). FemCare AI combines Machine Learning, FastAPI, and a modern React frontend to deliver personalized risk assessment, interactive visualizations, and evidence-based lifestyle recommendations.

> **Disclaimer:** This application is intended for educational and research purposes only. It does **not** replace professional medical diagnosis or clinical consultation.

---

## Overview

FemCare AI was developed as a final-year engineering project to demonstrate the integration of Machine Learning with modern web technologies.

The system allows users to complete a guided health assessment based on clinically relevant indicators such as:

- Age
- Weight
- Height
- Menstrual cycle information
- Waist-to-hip ratio
- Lifestyle habits
- Hormonal symptoms

The collected information is processed by an optimized Machine Learning model, which predicts PMOS risk probability and presents the results through an interactive dashboard.

---

# Features

- AI-powered PMOS risk prediction
- Optimized Random Forest Machine Learning model
- AutoML experimentation using TPOT
- Bayesian Hyperparameter Optimization using Optuna
- CTGAN synthetic data augmentation
- Interactive multi-step assessment
- Personalized health recommendations
- Hormonal balance analysis
- Risk probability visualization
- Contribution breakdown dashboard
- Responsive modern UI
- FastAPI REST API backend
- React + TypeScript frontend
- Fully responsive design

---

# Machine Learning Pipeline

The deployed model follows the pipeline below:

Original Dataset

↓

Clinical Feature Selection

↓

Data Cleaning & Preprocessing

↓

CTGAN Synthetic Data Augmentation

↓

AutoML Model Search (TPOT)

↓

Bayesian Hyperparameter Optimization (Optuna)

↓

Optimized Random Forest Classifier

↓

Model Deployment (FastAPI)

---

# Technology Stack

## Machine Learning

- Python
- Scikit-learn
- Pandas
- NumPy
- TPOT AutoML
- Optuna
- CTGAN
- Random Forest
- Joblib

---

## Backend

- FastAPI
- Uvicorn
- REST API
- Pydantic
- Joblib
- Pandas

---

## Frontend

- React
- TypeScript
- Vite
- Tailwind CSS
- Framer Motion
- React Router DOM
- React Query
- Lucide React
- Sonner
- Recharts
- shadcn/ui

---

# Project Structure

```text
FemCare-AI
│
├── backend
│   ├── main.py
│   ├── model.pkl
│   ├── feature_columns.pkl
│   ├── requirements.txt
│   └── ...
│
├── frontend
│   ├── src
│   │   ├── pages
│   │   ├── components
│   │   ├── services
│   │   ├── hooks
│   │   └── lib
│   │
│   ├── public
│   ├── package.json
│   └── vite.config.ts
│
└── README.md
```

---

# Model Input Features

The prediction model uses the following 15 clinically selected features:

- Age
- Weight
- Height
- Menstrual Cycle Regularity
- Cycle Length
- Hip Circumference
- Waist Circumference
- Waist-to-Hip Ratio
- Weight Gain
- Hair Growth
- Skin Darkening
- Hair Loss
- Pimples
- Fast Food Consumption
- Regular Exercise

---

# System Architecture

```text
User

↓

React Frontend

↓

FastAPI REST API

↓

Optimized Machine Learning Model

↓

Prediction + Probability

↓

Interactive Dashboard

↓

Personalized Recommendations
```

---

# Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/FemCare-AI.git

cd FemCare-AI
```

---

# Backend Setup

```bash
cd backend

python -m venv .venv

# Windows
.venv\Scripts\activate

pip install -r requirements.txt

python -m uvicorn main:app --reload
```

Backend runs at

```
http://127.0.0.1:8000
```

---

# Frontend Setup

```bash
cd frontend

npm install

npm run dev
```

Frontend runs at

```
http://localhost:5173
```

---

# API Endpoint

### POST

```
/predict
```

### Example Request

```json
{
  "age": 24,
  "weight": 65,
  "height": 160,
  "irregular_cycle": 1,
  "cycle_length": 40,
  "hip_size": 36,
  "waist_size": 34,
  "whr": 0.94,
  "weight_gain": 1,
  "hair_growth": 1,
  "skin_darkening": 1,
  "hair_loss": 0,
  "pimples": 1,
  "fast_food": 1,
  "exercise": 0
}
```

---

### Example Response

```json
{
  "prediction": 1,
  "probability": 92.34
}
```

---

# Frontend Features

- Landing Page
- Multi-Step Assessment
- Animated Background
- Glassmorphism UI
- AI Result Dashboard
- Contribution Breakdown
- Hormonal Balance Analysis
- Lifestyle Insights
- Personalized Recommendations
- Responsive Design

---

# Future Improvements

- User authentication
- Historical prediction tracking
- Doctor dashboard
- Report generation (PDF)
- Cloud deployment
- Mobile application
- Explainable AI (SHAP/LIME)
- Electronic Health Record integration

---

# Contributors

Developed as a Final Year Engineering Project.

**Pratyus Pradhan**

GitHub:
https://github.com/pratyushimself

---

# License

This project is released for educational and academic purposes.

---

# Acknowledgements

- Kaggle PCOS Dataset
- Scikit-learn
- FastAPI
- React
- Tailwind CSS
- TPOT
- Optuna
- CTGAN
- Framer Motion
