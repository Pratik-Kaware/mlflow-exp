## 📁 Project Structure

```plaintext
mlflow-tracking-tutorial/
├── data/             # Dataset (optional or downloaded in script)
├── artifacts/        # Saved models, plots, or logs
├── experiment.py     # Main experiment script
├── requirements.txt  # List of dependencies
├── README.md         # Project documentation
└── mlruns/           # MLflow experiment tracking directory (auto-generated)
```
🧱 Requirements

    Python 3.6+

    pip

    Virtualenv (optional but recommended)

🔧 Setup Instructions

    Clone this repository

git clone https://github.com/<your-username>/mlflow-tracking-tutorial.git
cd mlflow-tracking-tutorial

    Create a virtual environment (optional)

python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

    Install dependencies

pip install -r requirements.txt

    Start MLflow UI

mlflow ui

Navigate to: http://localhost:5000

    Run the experiment

python experiment.py

🧪 What the Script Does

    Trains a basic ML model (e.g., Linear Regression)

    Logs:

        Parameters like alpha, iterations, etc.

        Metrics such as RMSE, accuracy

        Artifacts such as trained models, confusion matrices

    Saves everything in the mlruns/ directory

    Visualize and compare runs via the MLflow UI

🔍 Sample Commands for Manual Use

import mlflow

mlflow.set_experiment("linear-regression-demo")

with mlflow.start_run():
    mlflow.log_param("alpha", 0.01)
    mlflow.log_metric("rmse", 0.45)
    mlflow.sklearn.log_model(model, "model")

📚 Useful Links

    MLflow Official Docs

    MLflow Tracking Docs

🤝 Contributions

This is a personal learning project. Feel free to fork it and play around with MLflow yourself!
