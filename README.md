# 🛡️ OfferShield AI
### AI-Based Fake Job & Internship Detection System

OfferShield AI is a Machine Learning-powered web application designed to detect potentially fraudulent job postings and internship offers.

The application allows users to submit job-related information and upload recruitment documents for analysis. It uses a trained machine learning model to identify suspicious recruitment patterns and estimate the likelihood of a job offer being fraudulent.

The system aims to help students, fresh graduates and job seekers identify potentially fake recruitment opportunities and avoid online job scams.

## 🎯 Project Objectives

- Detect fake job postings and internship offers.
- Analyze job descriptions using Machine Learning.
- Process recruitment-related information.
- Estimate the probability of a job posting being spam or fraudulent.
- Maintain verification records for future reference.
- Provide users with an accessible web-based detection system.

## ✨ Key Features

- **Job Description Analysis:** Analyze job descriptions to identify suspicious recruitment content.
- **Document Upload:** Upload recruitment documents for verification.
- **Machine Learning Prediction:** Use a trained model to classify job postings.
- **Scam Probability:** Display the estimated spam probability as a percentage.
- **Risk Classification:** Identify potentially dangerous recruitment offers.
- **Verification Logs:** Store verification details in a database.
- **Web Interface:** Access the system through a Flask-based web application.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| Flask | Web application framework |
| HTML | Frontend structure |
| CSS | Frontend styling |
| JavaScript | Frontend interactions, if implemented |
| Machine Learning | Fake job classification |
| CSV | Dataset storage |
| Pickle (.pkl) | Saved trained model |
| SQL Database | Verification history storage |

## 🧠 Machine Learning Approach

The project uses a trained machine learning model to classify recruitment-related information.

The model is trained using the `fake_job_postings.csv` dataset.

The training and prediction workflow is divided into two main Python files:

- `train_model.py`: Responsible for training the machine learning model.
- `main.py`: Handles the Flask application and uses the saved model for predictions.

The trained model is saved as:

`job_spam_model.pkl`

The application generates a spam probability and uses a 50% threshold in its current result-handling logic to determine the danger flag.

The exact algorithm, text preprocessing techniques and probability calibration should be documented according to the actual training implementation.

## ⚙️ System Workflow

1. The user opens the OfferShield AI web application.
2. The user provides job-related information and/or uploads a recruitment document.
3. The application processes the submitted information.
4. The trained machine learning model analyzes the input.
5. The system generates a spam prediction and probability.
6. The result is displayed on the web interface.
7. Verification details are saved in the database.

## 📂 Project Structure

```text
college_project/
│
├── college_project/
│   ├── static/
│   │   └── CSS, JavaScript and static assets
│   │
│   ├── templates/
│   │   └── HTML templates
│   │
│   ├── uploads/
│   │
│   ├── fake_job_postings.csv
│   ├── main.py
│   └── train_model.py
│
├── uploads/
├── job_spam_model.pkl
├── requirements.txt
├── README.md
├── .gitignore
└── LICENSE
```

*This represents the visible project files, with documentation files shown as recommended additions. Adjust paths if your final project structure differs.*

## 🗄️ Database Integration

The application includes database connectivity through a database connection function.

It uses a `verification_logs` table to store recruitment verification information.

The visible application code references fields such as:

- Company name
- Job title
- Job description
- Uploaded document name
- Prediction-related information

This helps maintain a record of previous verification activities.

## 🚀 Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/OfferShield-AI.git
```

### 2. Navigate to the project directory

```bash
cd OfferShield-AI
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

### 4. Activate the environment

Windows:

```bash
venv\Scripts\activate
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Configure the database

Configure the database connection according to the database system used by the application.

Ensure that the required `verification_logs` table exists.

### 7. Run the application

```bash
python main.py
```

The application runs using Flask's development server. Open the local URL displayed in the terminal.

## 📊 Dataset

The project uses `fake_job_postings.csv` as its training dataset.

The dataset contains recruitment-related information used for developing the fake job detection model.

Dataset provenance, class distribution and preprocessing details should be documented when finalized.

## 📈 Prediction Output

The application provides prediction-related information, including:

- Spam classification status.
- Estimated spam probability.
- Danger flag based on the configured 50% threshold.

Example:

| Parameter | Example |
|---|---|
| Company | ABC Technologies |
| Job Title | Python Developer Intern |
| Prediction | Suspicious |
| Spam Probability | 85% |
| Danger Status | Yes |

*Illustrative output only.*

## 🔮 Future Enhancements

- Improved NLP-based job description analysis.
- More advanced machine learning algorithms.
- Enhanced PDF and image text extraction.
- Company and recruiter verification.
- Explainable AI for suspicious-content identification.
- Improved model performance through larger and more diverse datasets.
- Better verification history and reporting features.

## ⚠️ Disclaimer

OfferShield AI is an academic machine learning project. Predictions are estimates and should not be treated as definitive proof of fraud.

Users should independently verify employers and recruiters before sharing personal information or making payments.

## 👩‍💻 Project Information

**Project Name:** OfferShield AI

**Project Type:** Machine Learning Web Application

**Domain:** Artificial Intelligence, Recruitment Fraud Detection and Cybersecurity

**Framework:** Flask

**Programming Language:** Python

**Project Purpose:** Academic IDP Project

---

⭐ If you find this project useful, consider giving the repository a star!
