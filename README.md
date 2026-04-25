# 🏏 IPL Prediction Engine 2026  
### ⚡ End-to-End Machine Learning + Simulation System

---

## 🚀 Overview

This project builds a **complete IPL prediction engine** using historical ball-by-ball data (2008–2025).

Instead of simple classification, it models the IPL as a **probabilistic system**, where:

- Every match outcome is predicted using ML  
- Entire seasons are simulated match-by-match  
- Team strength evolves dynamically (form tracking)  
- Final winners are derived using **Monte Carlo simulation**

👉 This makes the system closer to **real-world uncertainty modeling**, not just static prediction.

---

## 🏆 Final Prediction

### 🔴 Predicted IPL 2026 Winner: **RCB**  
> Derived from 1000+ simulated seasons using probability-based match outcomes

---

## 🧠 Key Capabilities

- 📊 **Match-Level Prediction**  
  Uses trained ML model (`predict_proba`) to estimate win probability  

- 🔁 **Dynamic Team Form**  
  Rolling performance (last 5 matches) updates during simulation  

- 🧮 **Season Simulation Engine**  
  Recreates full IPL schedule and generates realistic points table  

- 🎯 **Monte Carlo Simulation**  
  Runs 1000+ seasons to compute championship probability distribution  

- 🤖 **Multi-Model Training**  
  Compares multiple ML algorithms and selects best performer  

---

## 🧪 Machine Learning Pipeline

### 🔹 Feature Engineering
- Team win rate (historical strength)  
- Head-to-head performance  
- Rolling form (momentum)  
- Toss advantage (neutral baseline)

---

### 🔹 Models Used
- Logistic Regression  
- Random Forest  
- Extra Trees  
- XGBoost  
- LightGBM  

---

### 🔹 Model Selection Strategy
- Accuracy (classification performance)  
- Log Loss (probability calibration — critical for simulation)

---

## 🔁 Simulation Logic

### Match Prediction
- Input: team1 vs team2 features  
- Output: probability (team1 wins)  
- Winner sampled probabilistically (not deterministic)

---

### Season Engine
- Uses real IPL schedule  
- Updates team form after each match  
- Builds dynamic points table  

---

### Monte Carlo Layer
- Repeat season simulation 1000+ times  
- Count how often each team wins  
- Convert to **win probability (%)**

---

## 📊 Outputs Generated

- 📌 Predicted Points Table  
- 📌 Team-wise Win Probability (%)  
- 📌 Historical Performance Trends  

---

## 📂 Dataset

📥 Source:  
https://www.kaggle.com/code/arbazkhan971/indian-premier-league-analysis-2008-2025  

⚠️ Dataset is not included due to size constraints.

---

## ⚙️ Setup & Run (All Steps in One)

```bash
# 1️⃣ Clone repository
git clone https://github.com/your-username/IPL-Prediction.git
cd IPL-Prediction

# 2️⃣ Install dependencies
pip install -r requirements.txt

# 3️⃣ Download dataset from Kaggle
# → Extract CSV

# 4️⃣ Place dataset here:
# data/raw/IPL.csv

# 5️⃣ Run notebook
jupyter notebook
# Open → notebooks/TRAINING.ipynb
# Run all cells
