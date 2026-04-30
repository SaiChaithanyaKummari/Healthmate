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
healthmate/
│
├── models/
├── data/
│
├── src/
│   ├── app.py
│   ├── ml/
│   │   ├── model.py
│   │   ├── preprocess.py
│
├── static/
├── templates/
│
├── requirements.txt
├── README.md
```

## ⚙️ Getting Started

### Prerequisites
- Python 3.8 or higher installed on your system.

### Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd Healthmate
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Ensure Models are Generated**:
   If the `models/` folder is empty, run the training script:
   ```bash
   python healthmate_ml.py
   ```

### Running the Application

1. Start the Flask server:
   ```bash
   python app.py
   ```
2. Open your browser and navigate to `http://127.0.0.1:5000`.

## 🧠 Machine Learning Approach

Healthmate uses a two-step prediction process for high accuracy:
1. **Binary Classification (SVM)**: First, it determines if a deficiency is present or not.
2. **Multi-class Classification (XGBoost)**: If a deficiency is detected, this model identifies the specific type.

The models are trained on a comprehensive dataset of health metrics including age, BMI, physical activity, eating habits, and more.

## 📋 Note
This project is for educational/informational purposes. Always consult with a healthcare professional before making significant changes to your diet or lifestyle.

---
Developed as part of the Healthmate project.
