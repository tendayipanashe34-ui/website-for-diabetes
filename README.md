# DiabetesIQ - Model + Web App

This repo contains scripts to train/save a simple diabetes classifier and a minimal Flask web app to serve predictions.

Quick steps:

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Place your dataset at `./data/diabetes_dataset.xlsx` (or keep it in Downloads).

3. Train and save model:

```bash
python app/train_and_save.py
```

4. Run the web app (loads saved artifacts from `./model`):

```bash
python app/app.py
```

The app will be available at `http://localhost:5000` and the `/api/predict` endpoint accepts a JSON list of feature values in the same order shown on the form.

Deployment:
- You can deploy this repo to Render, Railway, or any container host. Configure the host to run `python app/app.py`.
- A simple `Dockerfile` is included for container-based deploys.
