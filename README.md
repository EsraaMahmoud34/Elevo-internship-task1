# 📚 Student Performance Prediction

This project predicts students' **Exam Scores** based on different academic, personal, and social factors.

## 📊 Dataset

* **Rows:** 6,607
* **Columns:** 20
* **Target Variable:** `Exam_Score`

Features include:
`Hours_Studied`, `Attendance`, `Parental_Involvement`, `Access_to_Resources`, `Extracurricular_Activities`, `Sleep_Hours`, `Previous_Scores`, `Motivation_Level`, `Internet_Access`, `Family_Income`, `Teacher_Quality`, `School_Type`, `Peer_Influence`, `Physical_Activity`, `Learning_Disabilities`, `Parental_Education_Level`, `Distance_from_Home`, `Gender`.

---

## 🛠️ Workflow

### 1. Data Preprocessing & Cleaning

* Handle missing values (`Teacher_Quality`, `Parental_Education_Level`, `Distance_from_Home`).
* Encode categorical features → numeric.
* Scale numerical features using **StandardScaler**.
* Split into **train/test sets**.

### 2. Visualization

* Correlation heatmap for numeric features.
* Boxplots & scatter plots (features vs target).
* Pairwise feature interactions.

### 3. Models Used

* **Linear Regression**
* **Polynomial Regression**
* **Ridge Regression** (best after hyperparameter tuning with `GridSearchCV`)
* **Lasso Regression**
* **ElasticNet Regression**
* **Decision Tree Regressor**

### 4. Evaluation Metrics

* **R² Score (train & test)**
* **MAE (Mean Absolute Error)**
* **RMSE (Root Mean Squared Error)**

📈 **Ridge Regression** with tuned `alpha` gave the best balance between train & test performance.

---

## 🚀 Deployment

The project is deployed with **Streamlit**.

### Steps to Run Locally

1. **Clone the repo**

```bash
git clone <your-repo-link>
cd <your-repo-name>
```

2. **Create virtual environment (optional but recommended)**

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```
3. Install dependencies:

pip install -r requirements.txt

Run the Streamlit app:

streamlit run app.py

4. **Run the Streamlit app**

```bash
streamlit run app.py
```

This will open a local URL ([http://localhost:8501/](http://localhost:8501/)) where you can interact with the model.

---

## 📂 Project Structure

```
├── data/                  # dataset (if included)
├── notebooks/             # EDA & training notebooks
├── app.py                 # Streamlit app for deployment
├── ridge_model.pkl        # saved trained Ridge model
└── README.md              # project documentation
```

---

Tech Stacks:
```
pandas
numpy
matplotlib
seaborn
scikit-learn
joblib
streamlit
```
⚡ How to Run

Clone the repo:

git clone https://github.com/EsraaMahmoud34/Elevo-internship-task1.git
cd student-performance-prediction

🎯 Results

Best Model: Ridge Regression (after hyperparameter tuning with GridSearchCV)

Test R² Score: ~0.70

MAE: ~0.45

RMSE: ~1.80

📊 The Ridge model achieved the best trade-off between bias and variance compared to other tested models (Linear, Polynomial, Lasso, ElasticNet, Decision Tree).

👩‍💻 Author

Esraa Mahmoud
🎓 AI & Data Science Student @ Ain Shams University
🚀 USAID Pioneer Alumni | Machine Learning Enthusiast
