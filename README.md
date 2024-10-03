# Predicting Artist Song Popularity using Machine Learning (Design Phase)

## Table of Contents
1. [Project Overview](#1-project-overview)
2. [Problem Statement](#2-problem-statement)
3. [Value Proposition](#3-value-proposition)
4. [System Design](#4-system-design)
   - [Architecture Overview](#41-architecture-overview)
   - [System Architecture Diagram](#42-system-architecture-diagram)
5. [Software Development Lifecycle (SDLC)](#5-software-development-lifecycle-sdlc)
   - [Strategy Phase](#51-strategy-phase)
   - [Design Phase](#52-design-phase)
   - [Development Phase](#53-development-phase)
   - [Testing Phase](#54-testing-phase)
   - [Deployment Phase](#55-deployment-phase)
   - [Maintenance Phase](#56-maintenance-phase)
6. [Getting Started](#6-getting-started)
7. [Future Work](#7-future-work)


## 1. Project Overview

This project aims to predict the popularity of songs by major artists, such as The Weeknd, using **machine learning**. By analyzing **musical features** from the **Spotify API** and incorporating **external factors** like **social media mentions** from **Meta Graph API** and **Google Trends**, the model can forecast how popular a song might become. This model has potential applications in **music marketing**, **playlist curation**, and **artist promotion**, providing a data-driven way to optimize these strategies.

---

## 2. Problem Statement

In the digital music landscape, the ability to **predict song popularity** before or soon after release is vital for artists, record labels, and streaming platforms. Most existing methods rely on **historical trends** or subjective judgment, which can limit the ability to maximize a song’s potential. Early-stage popularity prediction can help stakeholders make **informed decisions** about **marketing**, **promotion**, and **distribution strategies** to increase user engagement and revenue. 

This project addresses the **gap in early-stage predictive analytics** by developing a **data-driven model** that forecasts a song's success using both **musical characteristics** and **external engagement metrics** like social media. 

---

## 3. Value Proposition

The **key value** this project offers is its ability to provide **real-time, predictive insights** into song popularity, helping artists and platforms make **proactive** and **strategic decisions**. 

- **For Artists and Record Labels**: Predict which songs are more likely to become hits, optimizing marketing campaigns and promotional efforts around high-potential tracks.
- **For Streaming Platforms**: Enhance **playlist curation** by including songs predicted to perform well, improving user engagement and experience.
- **For Marketing Teams**: Identify **trending songs** early to capitalize on viral trends, resulting in improved targeting for ads and promotions.
- **For Listeners**: Personalize recommendations by prioritizing potential hits, improving discovery and user satisfaction on music streaming platforms like **Spotify** and **Apple Music**.

---

## 4. System Design

### 4.1 Architecture Overview
This project follows a **modular architecture** to ensure scalability, maintainability, and ease of deployment. The system consists of the following components:

1. **Data Collection Layer**: Integrates with the **Spotify API**, **Meta Graph API**, and **Google Trends API** to collect both **musical features** and **social media engagement data**. Data is collected, cleaned, and stored in a **PostgreSQL** database.
   
2. **Preprocessing Layer**: Processes and transforms the raw data, applying **data cleaning**, **normalization**, and **feature engineering**.
   
3. **Modeling Layer**: Multiple **machine learning models** are trained, evaluated using **cross-validation**, and optimized. Experiment tracking using **MLflow** and **hyperparameter tuning** are performed to ensure the best model is selected and deployed for real-time predictions, with continuous monitoring for performance and drift detection.
   
4. **API Layer**: A **RESTful API** built using **FastAPI** allows external applications to access the model for predictions. The API communicates with the trained model and serves the prediction results to the frontend.

5. **Frontend (Web Application)**: A **React** frontend allows users to input song details and visualize the predicted popularity score along with insights such as feature importance.

6. **Deployment Layer**: The entire system is deployed on **Heroku** for hosting the API and web app, with model artifacts stored in **PostgreSQL**. A continuous integration and deployment pipeline is established using **GitHub Actions** to automate testing and deployment of the web app and API. 

7. **Monitoring and Maintenance**: Continuous monitoring using **New Relic** for tracking API performance, response times, and error rates. **Prometheus** with **Grafana** is used to monitor machine learning model performance and detect model drift. **Sentry** is integrated for real-time logging and error tracking across both the FastAPI backend and React frontend. Model retraining is triggered automatically based on performance drops or data drift, using **Heroku Scheduler** for managing the retraining pipeline.

### 4.2 System Architecture Diagram

![System Architecture Diagram](https://github.com/sharkz0912/song-popularity-predictor/blob/main/System%20Design%20Diagram.png)

---

## 5. Software Development Lifecycle (SDLC)

This project follows a complete **software development lifecycle (SDLC)** to ensure that all phases from planning to deployment and maintenance are systematically executed for a robust and scalable solution.

### **5.1 Strategy Phase**
- **Objective**: Build a machine learning model to predict song popularity, leveraging both musical features and external engagement metrics.
- **Success Metrics**: Measure model performance using **RMSE, MAE**, and **R-squared**, with success defined by delivering actionable insights for stakeholders in the music industry.

### **5.2 Design Phase**
- **System Design**: A **modular architecture** (as detailed in section 4.1) is employed, ensuring scalability, maintainability, and efficient data handling.
- **Data Flow Planning**: The design ensures that data is efficiently collected, processed, and flows through the system from APIs to model training, all the way to user-facing predictions via the frontend.

### **5.3 Development Phase**
- **Data Collection**: Integrated with **Spotify API**, **Meta Graph API**, and **Google Trends API** to gather song features and engagement data.
- **Feature Engineering**: Key features like **sentiment analysis** and **time-based trends** are engineered to improve model performance.
- **Model Building**: Multiple models (e.g., **XGBoost**, **Random Forest**) are trained and tuned, with **MLflow** used for tracking experiments and hyperparameter tuning.
- **Frontend Development**: Built a **React web app** to allow users to input song details and view real-time popularity predictions.

### **5.4 Testing Phase**
- **Unit Testing**: Used **pytest** for testing the data collection, preprocessing, and API layers to ensure system robustness.
- **Model Validation**: Validated the model using **cross-validation** techniques to ensure generalizability to unseen data.
- **User Acceptance Testing (UAT)**: Tested the web application with end users or simulated environments to ensure functionality and user satisfaction.

### **5.5 Deployment Phase**
- **CI/CD Pipeline**: Implemented a **CI/CD pipeline** using **GitHub Actions** to automate testing, integration, and deployment of the FastAPI and React frontend components.
- **Deployment**: Deployed the entire system (API and frontend) on **Heroku**, ensuring seamless deployment and scalability.

### **5.6 Maintenance Phase**
- **Model Retraining**: Set up an automated pipeline to retrain the machine learning model as new data becomes available.
- **Monitoring**: Integrated tools like **Prometheus/Grafana**, **Sentry**, and **New Relic** to monitor API performance, detect model drift, and track user activity. This ensures continuous system reliability and responsiveness.

---

## 6. Getting Started

---

## 7. Future Work

---