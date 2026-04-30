# Healthmate: Your AI-Powered Nutritional Companion

Healthmate is a web-based application designed to help users identify potential nutritional deficiencies and receive personalized food recommendations. By leveraging Machine Learning models (SVM and XGBoost), the application analyzes user health data to provide actionable nutritional insights.

## 🚀 Features

- **Nutritional Deficiency Prediction**: Uses a Support Vector Machine (SVM) model to detect if a user is likely to have a nutritional deficiency.
- **Specific Deficiency Classification**: Employs an XGBoost model to classify the specific type of deficiency (e.g., Vitamin D, Iron, etc.).
- **Personalized Recommendations**: Provides specific food suggestions based on the detected deficiency to help users improve their health.
- **User-Friendly Interface**: A simple and intuitive web interface for inputting health data and viewing results.
- **Data-Driven Insights**: Built on a solid nutritional dataset ensuring reliable predictions.

## 🛠️ Technologies Used

- **Backend**: [Flask](https://flask.palletsprojects.com/) (Python)
- **Machine Learning**: [Scikit-learn](https://scikit-learn.org/), [XGBoost](https://xgboost.readthedocs.io/), [Joblib](https://joblib.readthedocs.io/)
- **Data Processing**: [Pandas](https://pandas.pydata.org/), [NumPy](https://numpy.org/)
- **Frontend**: HTML5, Vanilla CSS
- **Environment**: Python 3.x

## 📁 Project Structure

```text
Healthmate/
│
├── dataset/
│   └── nutritional_dataset.csv
├── docs/
├── models/
│   ├── scaler.pkl
│   ├── svm_model.pkl
│   ├── xgboost_model.pkl
│   └── label_encoders.pkl
├── src/
│   ├── app.py
│   └── ml/
│       ├── dataset_creating.py
│       └── healthmate_ml.py
├── static/
│   ├── css/
│   ├── images/
│   └── js/
├── templates/
│   ├── about_us.html
│   ├── index.html
│   ├── questionnaire.html
│   └── results.html
├── requirements.txt
└── README.md
```

## ⚙️ Getting Started

### Prerequisites

- Python 3.8 or higher installed on your system.

### Installation (Windows)

1. **Open PowerShell and navigate to the project root**:

   ```powershell
   cd C:\Users\ASUS\OneDrive\Documents\GitHub\Healthmate
   ```

2. **Create and activate the virtual environment**:

   ```powershell
   python -m venv .venv
   .\.venv\Scripts\activate
   ```

3. **Install the required dependencies**:

   ```powershell
   pip install -r requirements.txt
   ```

4. **Generate or verify the trained models**:
   If you do not have `models/svm_model.pkl`, `models/xgboost_model.pkl`, `models/scaler.pkl`, and `models/label_encoders.pkl`, run:
   ```powershell
   .\.venv\Scripts\python.exe src\ml\healthmate_ml.py
   ```

### Installation (macOS/Linux)

1. **Open a terminal and navigate to the project root**:

   ```bash
   cd ~/OneDrive/Documents/GitHub/Healthmate
   ```

2. **Create and activate the virtual environment**:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install the required dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Generate or verify the trained models**:
   If you do not have `models/svm_model.pkl`, `models/xgboost_model.pkl`, `models/scaler.pkl`, and `models/label_encoders.pkl`, run:
   ```bash
   .venv/bin/python src/ml/healthmate_ml.py or python src/ml/healthmate_ml.py
   ```

### Running the Application

1. **Run the Flask app from the repository root (Windows)**:

   ```powershell
   .\.venv\Scripts\python.exe src\app.py or python src/app.py
   ```

2. **Run the Flask app from the repository root (macOS/Linux)**:

   ```bash
   .venv/bin/python src/app.py
   ```

3. **Open the browser** and go to:

   ```text
   http://127.0.0.1:5000
   ```

4. **Use the web interface** to enter your health data and view the nutritional deficiency prediction and recommendation results.

## 🧠 Machine Learning Approach

Healthmate uses a two-step prediction process for high accuracy:

1. **Binary Classification (SVM)**: First, it determines if a deficiency is present or not.
2. **Multi-class Classification (XGBoost)**: If a deficiency is detected, this model identifies the specific type.

The models are trained on a comprehensive dataset of health metrics including age, BMI, physical activity, eating habits, and more.

## 📋 Note

This project is for educational/informational purposes. Always consult with a healthcare professional before making significant changes to your diet or lifestyle.

---

Developed as part of the Healthmate project.
