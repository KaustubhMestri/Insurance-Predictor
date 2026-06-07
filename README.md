# 🏥 Insurance Premium Category Predictor

## Project Overview
Insurance Premium Category Predictor is an end-to-end Machine Learning application that classifies customers into insurance premium categories based on their demographic and lifestyle information.
The application predicts whether a customer belongs to a Low, Medium, or High insurance premium category. The project combines a Machine Learning model, a FastAPI backend for serving predictions, and a Streamlit frontend that provides an interactive user interface for users.
This project was built to gain practical experience in machine learning model development, API creation, and full-stack deployment of data science applications.

**Disclaimer**: For educational and informational purposes only. Not intended for actual insurance underwriting decisions.

## Problem Statement
Insurance companies often determine premium levels using factors such as age, BMI, smoking habits, family size, and residential region. Estimating the premium category can help insurers assess customer risk and simplify the premium assignment process.
The objective of this project is to build a classification model that predicts the insurance premium category for a customer based on their profile information.

## Key Features
- Classifies insurance premium into Low, Medium, or High categories
- Interactive **Streamlit** frontend for entering customer details
- **FastAPI** backend for real-time model inference
- Input validation using **Pydantic**
- Real-time prediction results displayed instantly

## Tech Stack
<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit"/>
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"/>
  <img src="https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge&logo=pydantic&logoColor=white" alt="Pydantic"/>
</p>

## Installation

Install:
- **Git**: [Download](https://git-scm.com/download/win)
- **Python 3.8+**: [Download](https://www.python.org/downloads/)

### Clone Repository
1. Open CLI.
2. Run:
   ```bash
   git clone https://github.com/KaustubhMestri/Insurance-Predictor.git
   cd Insurance-Predictor
   ```

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Run the Backend
```bash
uvicorn app:app --reload
```
Backend runs at `http://127.0.0.1:8000`

> Interactive API docs available at `http://127.0.0.1:8000/docs`

### Run the Frontend
```bash
streamlit run frontend.py
```

---

## 📖 How to Use

1. Run the **FastAPI backend** first (`uvicorn app:app --reload`)
2. Launch the **Streamlit frontend** (`streamlit run frontend.py`)
3. Enter customer details in the form:
   - Age, Gender, BMI, Number of Children, Smoking Status, Region
4. Click **Predict** — the model returns the premium category instantly

---

## Sample Prediction

**Input:**
```json
{
  "age": 35,
  "sex": "male",
  "bmi": 29.5,
  "children": 2,
  "smoker": "yes",
  "region": "southeast"
}
```

**Output:**
```json
{
  "insurance_premium_category": "High"
}
```

---

## How It Works
1. User enters personal details in the Streamlit app
2. Data is sent to the FastAPI backend via a POST request
3. Pydantic validates the incoming input
4. Trained Scikit-Learn classification model processes the input
5. Predicted premium category (Low / Medium / High) is returned and displayed

## Contributing
1. Create an [issue](https://github.com/KaustubhMestri/Insurance-Predictor/issues).
2. Branch: `feature/<n>` or `bugfix/<n>`
   ```bash
   git checkout -b feature/<n>
   ```
3. Commit:
   ```bash
   git add .
   git commit -m "#<issue> message"
   ```
4. Push:
   ```bash
   git push origin feature/<n>
   ```
5. Submit PR to `main`.

## Author

**Kaustubh Mestri**
This project was developed as part of my machine learning and backend development learning journey, focusing on building practical, deployable solutions using Python and FastAPI.

## License
MIT License. See [LICENSE](LICENSE).
