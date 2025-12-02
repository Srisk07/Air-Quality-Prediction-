🌿 Air Quality Prediction using Machine Learning

This project predicts the Air Quality Index (AQI) category based on pollutant levels using a Random Forest Classifier.
The model is trained on the Air Quality Data (India) dataset and deployed using Gradio for a simple, interactive web interface.

📌 Project Overview

This project helps in predicting the AQI Bucket (e.g., Good, Moderate, Poor, etc.) using six major air pollutants:

PM2.5

PM10

NO2

CO

SO2

O3

It includes:
✔ Data Cleaning
✔ Label Encoding
✔ Machine Learning Model Training
✔ Evaluation using Accuracy & Classification Report
✔ Confusion Matrix Visualization
✔ Gradio-based Web App for Real-Time AQI Prediction

📂 Project Structure
📁 air-quality-prediction
│
├── Air_quality_dataset.py       # Main project script
├── rf_aqi_classifier.joblib     # Trained Random Forest model
├── label_encoder.joblib         # Label encoder for AQI bucket
├── README.md                    # Project documentation
└── air-quality-data-in-india.zip # Raw dataset (optional)

📊 Dataset

The dataset comes from:
Air Quality Data in India
Contains daily pollutant details for multiple Indian cities.

Features used:
Feature	Description
PM2.5	Fine particles ≤ 2.5 μm
PM10	Particulate matter ≤ 10 μm
NO2	Nitrogen Dioxide
CO	Carbon Monoxide
SO2	Sulfur Dioxide
O3	Ozone
Target:

AQI_Bucket → Categorized AQI (e.g., Good, Moderate, Poor)

🛠️ Technologies Used

Python

Pandas

NumPy

Scikit-Learn

Matplotlib

Seaborn

Gradio

Joblib

⚙️ Model Training Process

Load dataset from ZIP

Clean missing values

Encode AQI bucket using LabelEncoder

Split training/testing datasets

Train Random Forest Classifier

Evaluate accuracy & generate confusion matrix

Save trained model

📈 Model Performance

The model is evaluated using:

Accuracy Score

Classification Report

Confusion Matrix

The accuracy may vary based on dataset split.

🌐 Gradio Web App

The project includes an interactive Gradio interface to predict AQI category.

Inputs

PM2.5

PM10

NO2

CO

SO2

O3

Output

Predicted AQI Category

▶️ How to Run the Project
1️⃣ Install dependencies
pip install numpy pandas scikit-learn seaborn matplotlib joblib gradio

2️⃣ Run the main script
python Air_quality_dataset.py

3️⃣ Launch Gradio UI

After running, Gradio will show a local URL:

http://127.0.0.1:7860


Click to open the interface.

🧪 Sample Prediction

Enter values like:

PM2.5	PM10	NO2	CO	SO2	O3
100	180	45	0.8	18	70

🡆 Output: "Predicted AQI Category: Moderately Polluted"

📦 Saving & Loading Model

The model and encoder are saved as:

joblib.dump(rf_classifier, "rf_aqi_classifier.joblib")
joblib.dump(le, "label_encoder.joblib")


To load:

model = joblib.load("rf_aqi_classifier.joblib")
label_encoder = joblib.load("label_encoder.joblib")

🚀 Future Enhancements

Deploy Streamlit/Dashboard Version

Add more ML algorithms (XGBoost, SVM)

Add Deep Learning model

Build REST API for AQI Prediction

👨‍💻 Author

Sri Harini
