# 🏎️ F1 Analytics Project

![F1 Logo](https://camo.githubusercontent.com/7efe61a391ed58a4c8fd614b9f6c36618935754f1d6bac17f22c7340853ab221/68747470733a2f2f75706c6f61642e77696b696d656469612e6f72672f77696b6970656469612f636f6d6d6f6e732f7468756d622f332f33332f46312e7376672f3235363070782d46312e7376672e706e67)
---

## 🚀 Key Features

### 🔹 1. Race-Level Analytics
- Pit-stop efficiency  
- Driver positioning and overtakes  
- Aggression score modeling  
- Lap consistency metrics  
- Team execution patterns  

### 🔹 2. Driver-Level Analytics
- Season consistency  
- Average finishing position  
- Performance trends  
- Driver–tire efficiency  
- Positional gain vs aggression  

### 🔹 3. Team (Constructor) Analytics
- Pit crew performance  
- Tire usage strategy  
- Season scoring predictability  
- Strengths on wet/dry races  

### 🔹 4. Tire Compound Strategy Engine
- Stint length modeling  
- Compound efficiency (position gain per lap)  
- Weather-dependent behavior  
- Driver/Team tire profiles  

### 🔹 5. Predictive Machine Learning Model
Built using:
- XGBoostClassifier  
- Feature engineering from DriverSeason table  
- Hyperparameter tuning  
- Probability-based ranking  
- Feature importance analysis  

Predicts:
- 🥇 **Next season's winner**  
- 🏆 Constructor-influenced performance  

### 🔹 6. Interactive Streamlit App
Upload any F1 dataset and:
- View analytics dashboards  
- Explore driver/team comparisons  
- Generate tire strategy insights  
- Predict the next champion  

---

## 🧹 Data Cleaning Summary

### ✅ Race-Level Fixes
- Standardized compound naming  
- Removed pit time outliers (<15s or >40s)  
- Fixed missing stint values  
- Validated lap and timing logic  

### ✅ Stint & Pit Logic Fixes
- Ensured **stints = pit_stops + 1**  
- Corrected last stint anomalies  
- Removed duplicates  
- Cleaned aggression score outliers  

---

## 🧱 Data Model (Constellation Schema)

### **Fact Tables**
- `Fact_PitStops` — granular event-level pit/stint data  
- `DriverRace` — engineered per-race metrics  
- `DriverSeason` — season-level aggregates  

### **Dimensions**
- Driver  
- Constructor  
- Race  
- Season  
- Tire Compound  

This schema supports BI dashboards and ML training pipelines.

---

## 🧠 Machine Learning Model

### **Objective**  
Predict the **next season's driver champion**.

### **Model**  
`XGBoostClassifier`

### **Engineered Features Include:**
- avg_finish  
- avg_points  
- total_points  
- aggression  
- avg_pit_time  
- avg_pos_gain  
- races_attended  
- constructor_strength  

### **Output**  
- Champion prediction  
- Probability ranking  
- Feature importance chart  

---

## 🖥️ Streamlit App

Run the app:

```bash
streamlit run app.py
```

Includes:
- Dataset upload
- Automated cleaning
- Analytics dashboard
- Tire strategy insights
- Season winner prediction

---

## 📦 Installation

1. **Clone repo**
```bash
git clone https://github.com/YOUR-USERNAME/F1-Analytics.git
cd F1-Analytics
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Launch notebooks**
```bash
jupyter notebook
```

4. **Start Streamlit app**
```bash
streamlit run app.py
```

---

## 🛠️ Technologies Used

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Machine Learning: Scikit-learn, XGBoost
- Streamlit
- Power BI
- DAX
- SQL
- Git & GitHub

---

## 🔮 Future Enhancements

- Add race winner prediction model
- Integrate lap-time simulation
- Add neural network performance model
- Extend dataset to older seasons
- Deploy full web dashboard with authentication

---

## 🤝 Contributions

Pull requests, issues, and suggestions are welcome!

---

## ⭐ Support

If you found this project interesting, please ⭐ star the repo — it helps a lot!

