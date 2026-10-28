# Student Math Score Prediction

This project trains a regression model to estimate a student's math score from
their reading and writing scores, test-preparation status, and student context.
The math score is the prediction target and is not included among the model
inputs.

## Run the application

Install the dependencies listed in `requirements.txt`, then start the Flask app:

```powershell
python app.py
```

Open `http://127.0.0.1:5000` in your browser and choose **Make a prediction**.
Enter reading and writing scores and the requested student details to see the
estimated math score.

## Retrain the model

From the project root, run:

```powershell
python -m src.components.data_ingestion
```

This splits the source dataset, transforms the features, trains the regression
model, and saves the model and preprocessor under `artifacts/`.