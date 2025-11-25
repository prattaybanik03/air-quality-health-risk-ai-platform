# 🌍 Air Quality AI Decision Support System

![Python](https://img.shields.io/badge/Python-3.9-3776AB?style=flat&logo=python&logoColor=white)
![React](https://img.shields.io/badge/React-18.2-61DAFB?style=flat&logo=react&logoColor=black)
![AWS](https://img.shields.io/badge/AWS-Cloud-FF9900?style=flat&logo=amazon-aws&logoColor=white)
![AI](https://img.shields.io/badge/AI-Random_Forest-green?style=flat)

> **University Capstone Project (High Distinction - 94%)** > A full-stack decision support system that translates complex environmental data into actionable health risk assessments using Machine Learning.

## 🚀 Product Vision
Raw air quality data (e.g., "56 PM2.5") is often meaningless to the average citizen. This platform solves the problem of **data interpretation**. By aggregating global pollution data and running it through a custom Random Forest model, the system classifies **Real-Time Health Risk** and provides location-specific recommendations for at-risk communities.

## 🛠️ Technical Stack
* **Frontend:** React.js, Material-UI (for responsive dashboards), Plotly.js (Data Viz).
* **Backend:** FastAPI (Python) - chosen for asynchronous performance and easy ML integration.
* **AI/ML:** Scikit-Learn (Random Forest Regression & Classification).
* **Data Sources:** IQAir API (Real-time), OpenCage API (Geocoding), NewsAPI.
* **DevOps:** Dockerized containers deployed on AWS.

## 🧠 AI & Data Science Implementation
The core intelligence engine uses a **Random Forest** algorithm trained on 4 merged global datasets (WHO, Global Air).
* [cite_start]**Model Accuracy:** Achieved **91% accuracy** in risk classification[cite: 1812].
* [cite_start]**Performance:** R-squared score of **0.975** for health burden prediction[cite: 1942].
* [cite_start]**Feature Engineering:** Created a custom `total_exposure` aggregate feature to stabilize predictions across different regions[cite: 1823].

## 🏗️ Architecture
The system follows a **Microservices-style** architecture:
1.  **User Layer:** React frontend handles user interactions and visualizations.
2.  **Logic Layer:** FastAPI sanitizes inputs and manages API requests.
3.  [cite_start]**Intelligence Layer:** The ML model is serialized (Pickle) and loaded into memory for low-latency inference[cite: 839].

## 💻 How to Run
```bash
# Backend
cd backend
pip install -r requirements.txt
uvicorn main:app --reload

# Frontend
cd frontend
npm install
npm start
