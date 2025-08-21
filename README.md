# 🩺 Diabetes Prediction Model

This project is a machine learning model built to predict whether a patient has diabetes based on medical diagnostic data.  
The dataset used is the **Pima Indians Diabetes Dataset**, which is licensed under **CC0: Public Domain**, meaning it is free to use and share.

---

## 📂 Project Structure

- `Diabetes_prediction.ipynb` → Main Jupyter Notebook containing code, explanations, and results.  
- `diabetes.csv` → Dataset used for training and testing.  
- `requirements.txt` → Python dependencies.  
- `.gitignore` → Ignore unnecessary files (cache, logs, etc.).  
- `xgb_diabetes_model.pkl` → Saved trained model for reuse.  

---

## ⚙️ Methodology

1. **Data Preprocessing**  
   - Handled missing/invalid values.  
   - Scaled features for better model performance.  

2. **Model Training**  
   - Tried multiple classification models.  
   - Selected the best-performing model based on evaluation metrics.  

3. **Threshold Tuning**  
   - Adjusted probability threshold to improve recall.  

---

## 📊 Why Recall is Prioritized Over Accuracy/Precision?

In **medical prediction tasks** (like diabetes detection):  
- **False Negative (missed detection)** is more dangerous than a **False Positive**.  
- Recall measures the ability of the model to correctly identify all actual positive cases (patients with diabetes).  
- By prioritizing recall, we reduce the chances of missing a patient who actually has diabetes, which is critical in healthcare.  

Hence, the model is tuned to maximize **recall**, even if it slightly reduces accuracy or precision.  

---

## 🔑 Key Results (after threshold adjustment)

- **Accuracy:** ~75%  
- **Precision (Positive class):** ~61%  
- **Recall (Positive class):** ~80%  
- **F1-Score (Positive class):** ~69%  

This means the model successfully detects **most diabetic patients** while keeping false positives at a reasonable level.  

---

## 🚀 Usage

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/Diabetes-Prediction.git
cd Diabetes-Prediction
