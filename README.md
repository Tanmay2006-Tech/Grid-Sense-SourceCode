<div align="center">

# 🚦 GridSense

### AI-Powered Traffic Operations Co-Pilot for Bangalore

Predict Congestion • Optimize Resource Deployment • Learn from Historical Incidents

[Live Demo](https://grid-sense-gridsense.vercel.app)

</div>

---

## Overview

GridSense is an AI-powered decision-support platform built for Bangalore Traffic Police.

The system predicts traffic congestion severity before incidents escalate and recommends operational actions including officer deployment, barricade allocation, and diversion planning.

GridSense combines machine learning, explainable AI, similarity search, scenario simulation, and a continuous officer feedback loop into a single operational dashboard.

---

## Problem Statement

Traffic authorities currently rely heavily on experience-based decision making during large public events, accidents, road closures, and VIP movement.

Key challenges include:

- No congestion forecasting before incidents occur
- Resource allocation based on intuition rather than data
- No explainability for deployment decisions
- No structured post-incident learning process
- Limited ability to compare incidents with historical cases

---

## Solution

GridSense provides:

### 📊 City Risk Index
Real-time city-wide congestion risk monitoring.

### 🤖 Congestion Prediction
Predicts traffic severity as:

- Low
- Medium
- High

### 🧠 Explainable AI
Displays the key factors contributing to each prediction.

### 🚔 Resource Optimizer
Recommends:

- Officer Count
- Barricades
- Diversion Routes

### 🔄 What-If Simulation
Allows authorities to test scenarios such as:

- Road Closure ON/OFF
- Planned vs Unplanned Events

### 🔍 Similar Historical Incidents
Uses cosine similarity across 63 engineered features to identify comparable past incidents.

### 📝 Officer Feedback Loop
Captures actual outcomes and tracks prediction accuracy over time.

---

# System Architecture

```text
Historical Traffic Data
            │
            ▼
Feature Engineering (63 Features)
            │
            ▼
 ML Ensemble Model
 ├─ LightGBM (30%)
 ├─ CatBoost (40%)
 └─ XGBoost (30%)
            │
            ▼
Prediction Engine
            │
            ▼
Deployment Recommendations
            │
            ▼
Officer Feedback Loop
```

---

# Dataset

| Metric | Value |
|----------|----------|
| Dataset | Bangalore Traffic Incident Dataset |
| Records | 8,173 |
| Time Period | Jan 2024 – May 2024 |
| Features | 63 Engineered Features |

---

# Model Performance

| Metric | Score |
|----------|----------|
| Accuracy | 63.8% |
| Macro F1 Score | 0.640 |
| High-Risk Recall | 75.5% |

GridSense prioritizes identifying high-risk congestion events over maximizing overall accuracy.

---

# Repository Structure

```text
GridSense/
│
├── Grid-Sense-Frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── README.md
│
├── Grid-Sense-Backend/
│   ├── api.py
│   ├── pipeline.py
│   ├── requirements.txt
│   ├── data/
│   └── README.md
│
└── README.md
```

---

# Tech Stack

## Frontend

- React 19
- TypeScript
- Vite
- Tailwind CSS
- Framer Motion
- Recharts
- Leaflet

## Backend

- Flask
- Python

## Machine Learning

- LightGBM
- CatBoost
- XGBoost
- Scikit-Learn
- Optuna

## Deployment

- Vercel (Frontend)
- Render (Backend)

---

# Running The Project

## Backend

```bash
cd Grid-Sense-Backend

pip install -r requirements.txt

python api.py
```

Backend runs on:

```text
http://localhost:5000
```

---

## Frontend

```bash
cd Grid-Sense-Frontend

pnpm install
```

Create `.env`

```env
VITE_API_URL=http://localhost:5000
```

Run:

```bash
pnpm dev
```

Frontend runs on:

```text
http://localhost:5173
```

---

# Live Demo

Frontend:

https://grid-sense-gridsense.vercel.app

---

# Source Repositories

Frontend:
https://github.com/ghost33218/Grid-Sense

Backend:
https://github.com/Tanmay2006-Tech/gridsense-backend

---

# Team

Built for Gridlock Hackathon 2.0

### GridSense
Predict. Deploy. Prevent.
