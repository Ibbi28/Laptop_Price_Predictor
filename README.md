# 💻 Laptop Price Prediction using Regression Models

## 🔍 Objective

This project aims to predict laptop prices based on various features such as RAM, screen resolution, storage type, GPU, CPU, and operating system.  
The goal was to clean, preprocess, and extract meaningful information from raw data and apply multiple regression models to determine the most accurate predictor.

---

## 🛠️ Tools & Technologies

- **Programming Language**: Python  
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost, LightGBM  
- **Environment**: Jupyter Notebook  
- **Techniques Used**: Feature Engineering, Regular Expressions, One-Hot Encoding, Model Evaluation

---

## ⚙️ Approach

### 🔹 Data Cleaning & Preprocessing

- Removed irrelevant and duplicate columns  
- Converted RAM and Weight columns from object to numerical types  
- Standardized screen resolution, touchscreen, IPS display, and calculated PPI (Pixels Per Inch)  
- Extracted structured information from complex CPU, GPU, and Memory fields  
- Categorized operating systems into simplified OS categories  

### 🔹 Feature Engineering

- Created new boolean and numeric columns: `IsTouchScreen`, `HasIPS`, `PPI`, `GpuName`, `OS_Category`, etc.  
- Separated storage into multiple columns: `SSD_GB`, `HDD_GB`, `Flash_Storage_GB`, `Hybrid_GB`  

### 🔹 Model Building & Evaluation

Applied multiple regression algorithms including:

- XGBoost, Random Forest, LightGBM, Gradient Boosting, Extra Trees  
- Ridge, Lasso, Bayesian Ridge  
- K-Nearest Neighbors, SVR, Decision Tree, AdaBoost  

Evaluated using:

- **R² Score** (higher is better)  
- **Mean Absolute Error (MAE)** (lower is better)  

Used pipelines and One-Hot Encoding for proper preprocessing.

---

## 📈 Results

| Model              | R² Score | MAE  |
|--------------------|----------|------|
| 🥇 XGBoost          | 0.9028   | 0.15 |
| 🥈 Random Forest    | 0.8900   | 0.15 |
| 🥉 LightGBM         | 0.8871   | 0.16 |
| Gradient Boosting  | 0.8722   | 0.17 |
| Extra Trees        | 0.8579   | 0.16 |

- **Best Model**: XGBoost with an excellent **R² Score of 0.9028** and **MAE of 0.15**  
- Ensemble models consistently outperformed others

---

## 📌 Key Takeaways

- Careful feature extraction and engineering significantly enhanced model accuracy  
- Ensemble models such as **XGBoost**, **Random Forest**, and **LightGBM** delivered the most reliable predictions  
- The pipeline-based workflow ensures **reproducibility** and **scalability**
