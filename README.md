# Movie-Recommend
# 🎬 Hybrid Movie Recommender System

## 📌 Overview
This project implements a **Hybrid Movie Recommender System** that combines:

- **Content-Based Filtering (CBF)** → based on movie features (genres, year)
- **Collaborative Filtering (CF)** → based on user behavior (ratings)
- **Hybrid Approach** → combines both methods for improved recommendations

The goal is to provide more accurate and personalized movie suggestions.

---

## 📂 Dataset

The system uses:

### Required Columns:
- `movieId` → Unique movie identifier  
- `title` → Movie title (includes year)  
- `genres` → Movie genres (e.g., Action|Comedy)  

---

## ⚙️ How It Works

### 1. Feature Engineering
- Extract year from movie title  
- Clean titles  
- Convert genres into text format  

---

### 2. Content-Based Filtering (CBF)
- Uses **TF-IDF vectorization** on genres  
- Computes similarity using **cosine similarity**

👉 Recommends movies similar to those the user already likes  

---

### 3. Collaborative Filtering (CF)
- Builds a **user-item matrix**  
- Applies **Singular Value Decomposition (SVD)**  
- Predicts missing ratings  

👉 Learns patterns across users  

---

### 4. Hybrid Model

The final recommendation score is calculated as:


Where:
- `α = 0` → Pure Collaborative Filtering  
- `α = 1` → Pure Content-Based  
- `α = 0.5` → Balanced Hybrid  

---

## 📊 Evaluation

Model performance is evaluated using:

- **RMSE (Root Mean Squared Error)**  

This measures how close predicted ratings are to actual ratings.

---
