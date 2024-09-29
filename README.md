# Predicting Artist Song Popularity using Machine Learning (Phase 1)

## Project Overview

The goal of this project is to predict the popularity of major artists like The Weeknd's songs using machine learning. By analyzing musical features like tempo, energy, and danceability from Spotify and external factors like social media mentions, the model can predict how popular a song might become. The solution has potential applications in music marketing, playlist curation, and artist promotion.

## Problem Statement

In a competitive digital music landscape, artists, record labels, and streaming platforms need data-driven insights to understand which songs will resonate with audiences. Predicting song popularity before or soon after release can help optimize marketing campaigns, playlist placements, and promotion strategies. Most traditional approaches rely on historical trends or subjective factors, often unable to maximize a song's potential.

This project addresses the problem by providing a predictive model for song popularity, enabling stakeholders to make informed decisions earlier in the release cycle.

## Value Proposition

The value of this project lies in its potential to:

- **Improve Music Marketing**: Artists and labels can use predictive insights to allocate promotional efforts toward songs with higher hit potential.
- **Enhance Playlist Curation**: Streaming platforms can improve their playlist recommendations by prioritizing songs predicted to perform well.
- **Boost Engagement and Revenue**: With early insights into a song's popularity, platforms can better target their audience, leading to increased engagement and revenue.

## Technical Overview

The project uses a data-driven approach to predict song popularity through the following steps:

1. **Data Collection**:
   - **Spotify API**: Collect features such as tempo, energy, danceability, and popularity scores.
   - **External Sources**: Gather social media mentions via the Twitter API and Google Trends to capture external song engagement.

2. **Data Preprocessing and Feature Engineering**:
   - Clean and preprocess data from Spotify and external sources.
   - Engineer additional features like time-based trends, sentiment analysis of lyrics, and artist popularity metrics.

3. **Model Building**:
   - Train and test multiple machine learning models like Linear Regression, Random Forest, XGBoost to predict the song’s popularity score.
   - Evaluate models using metrics such as RMSE, MAE, and R-squared to identify most accurate model.

4. **Deployment**:
   - Deploy the model as a web app hosted on AWS for user-friendly way to interact with and showcase the model.

5. **Maintenance**:
   - Set up automated retraining pipelines to improve the model as new data becomes available.
   - Implement monitoring to track prediction performance over time.

## Roadmap

1. **Phase 1: Data Collection**: 
   - Integrate Spotify API and external sources for data collection.
   
2. **Phase 2: Feature Engineering and EDA**:
   - Analyze relationships between features and popularity.
   - Create derived features like sentiment analysis of song lyrics.

3. **Phase 3: Model Building and Evaluation**:
   - Train multiple models, tune hyperparameters, and evaluate their performance.

4. **Phase 4: Deployment**:
   - Build and deploy an API hosted on AWS for real-time song popularity predictions.

5. **Phase 5: Continuous Improvement**:
   - Automate data collection and retraining processes.
   - Implement monitoring and alerting for prediction accuracy and model drift.

## Getting Started

To set up the project, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/sharkz0912/song-popularity-predictor.git
   cd song-popularity-predictor