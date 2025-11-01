# 🏷️ Insurance Premium Predictor FastAPI

## 📘 Project Description
This project is a **FastAPI-based Machine Learning web service** that predicts the **insurance premium category** of a user based on their personal and lifestyle details such as age, BMI, income, city, occupation, and smoking habits.  
It uses a **pre-trained Scikit-Learn model (`model.pkl`)** to perform predictions and provides an easy-to-use REST API endpoint.

---

## ⚙️ Tech Stack
- **FastAPI** — Web framework for building APIs  
- **Uvicorn** — ASGI server for FastAPI  
- **Pydantic v2** — Data validation using `BaseModel` and `computed_field`  
- **Pandas** — DataFrame manipulation  
- **Scikit-learn** — Machine Learning model (pre-trained)  
- **Python 3.12+**

---

## 📦 Project Structure
```
📂 insurance-premium-predictor-fastapi
├── app.py              # Main FastAPI application file
├── model.pkl           # Trained ML model (scikit-learn)
├── requirements.txt    # All dependencies
└── README.md           # Documentation
```

---

## 🚀 Setup Instructions

### 1️⃣ Clone the repository
```bash
git clone https://github.com/<your-username>/insurance-premium-predictor-fastapi.git
cd insurance-premium-predictor-fastapi
```

### 2️⃣ Create a virtual environment
```bash
python -m venv myenv
myenv\Scripts\activate
```

### 3️⃣ Install dependencies
```bash
pip install fastapi uvicorn pandas scikit-learn
```

### 4️⃣ Run the API
```bash
uvicorn app:app --reload
```

### 5️⃣ Test the API
Open your browser and go to:  
👉 [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

---

## 🧠 How It Works
The `/predict` endpoint accepts a JSON input like this:
```json
{
  "age": 30,
  "weight": 70,
  "height": 1.75,
  "income_lpa": 10.5,
  "smoker": false,
  "city": "Pune",
  "occupation": "private_job"
}
```

And returns a predicted insurance premium category:
```json
{
  "predicted_category": "medium_risk"
}
```

---

## 🧩 Features
✅ Uses `@computed_field` to automatically calculate BMI, age group, lifestyle risk, and city tier  
✅ Input validation with type hints and constraints  
✅ JSON response format  
✅ Ready for deployment (Docker/FastAPI)

---
