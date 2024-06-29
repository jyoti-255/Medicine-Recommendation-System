# Medicine Recommendation System using Flask 🩺🔍

## Project Overview

This project implements a disease prediction and information system using Flask, where users can input symptoms and receive predictions about potential diseases. The system also provides descriptions, precautions, medications, recommended diets, and workouts related to the predicted disease.

## Project Components 📦

### Flask App (`app.py`)

The Flask application serves as the backend for the disease prediction system. It handles HTTP requests, processes user input (symptoms), predicts diseases using a pre-trained Support Vector Machine (SVM) model (`svc.pkl`), and retrieves relevant information from various datasets.

#### Dependencies

- Flask: Used for creating the web application and handling HTTP requests. 🌐
- NumPy and Pandas: Required for data manipulation and handling. 🧮🐼
- Pickle: Used for serializing and deserializing Python objects (loading the SVM model). 🥒

#### Datasets

- `symptoms_df.csv`: Contains a list of symptoms mapped to numerical indices.
- `precautions_df.csv`, `workout_df.csv`, `description.csv`, `medications.csv`, `diets.csv`: Provide information related to diseases for display.

#### Helper Functions

- **`helper(dis)`:** Retrieves disease descriptions, precautions, medications, recommended diets, and workouts based on the predicted disease.

#### Model Prediction Function

- **`get_predicted_value(patient_symptoms)`:** Converts user input (symptoms) into a binary vector and predicts the disease using the SVM model.

### Templates (`templates/`)

- **`index.html`:** Main template where users can input symptoms and view disease predictions, descriptions, precautions, medications, diets, and workouts.

- **Other Templates:** Additional pages (`about.html`, `contact.html`, `developer.html`, `blog.html`) providing information about the project, developer, and contact details.

## Usage 🚀

1. Ensure all dependencies are installed using `pip install -r requirements.txt`.
2. Run `python app.py` to start the Flask application.
3. Access the application in your web browser at `http://localhost:5000`.

## Routes

- **`/`:** Home page where users can input symptoms and view disease predictions.
- **`/about`, `/contact`, `/developer`, `/blog`:** Additional pages providing information about the project and developer.

---

