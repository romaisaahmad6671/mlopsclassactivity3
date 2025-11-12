# Triggering CI Pipeline

# 🚀 MLOps Class Activity: CI/CD Pipeline using GitHub Actions

[![CI Pipeline](https://github.com/romaisaahmad6671/mlopsclassactivity3/actions/workflows/ci-pipeline.yml/badge.svg)](https://github.com/romaisaahmad6671/mlopsclassactivity3/actions/workflows/ci-pipeline.yml)

This repository is part of the **MLOps course activity** on **Continuous Integration and Deployment (CI/CD)** for Machine Learning.  
The goal is to automate a complete ML workflow using **GitHub Actions** — from preprocessing to training, evaluation, and optional containerization.

---

## 🎯 Learning Objectives

By completing this activity, you will learn how to:

- Understand CI/CD concepts as applied to ML projects  
- Automate **data preprocessing**, **model training**, and **evaluation** using GitHub Actions  
- Automatically **upload trained model artifacts** (e.g., `.pkl` or `.zip` files)  
- *(Optional)* Build and push **Docker images** after successful training  

---


## 🧩 Repository Structure

```
mlops-ci-activity/
│
├── data/                      # Optional: sample dataset (if used)
│
├── preprocess.py              # Preprocessing script
├── train.py                   # Model training script
├── evaluate.py                # Model evaluation script
├── requirements.txt           # Dependencies
├── Dockerfile.train           # Docker image for training
├── Dockerfile.serve           # Docker image for serving
│
└── .github/
    └── workflows/
        └── ci-pipeline.yml    # GitHub Actions workflow definition
```

---

## ⚙️ Step-by-Step Instructions

### 🧭 1. Fork the Repository
Click **“Fork”** (top-right corner) to create a copy under your own GitHub account.

---

### 🧭 2. Trigger the CI Pipeline
1. Open your **forked** repo → click on `README.md` → click the ✏️ **Edit** icon.  
2. Add a blank line or write a small comment like:  

3. Scroll down → click **Commit changes** (keep “Commit directly to main”).  
4. Go to the **Actions** tab → watch the **CI Pipeline** run automatically.

---

### 🧭 3. Observe Workflow Steps
When you open the workflow run, you’ll see:
- ✅ Checkout repository  
- ✅ Set up Python  
- ✅ Install dependencies (`pip install -r requirements.txt`)  
- ✅ Run preprocessing (`python preprocess.py`)  
- ✅ Train the model (`python train.py`)  
- ✅ Evaluate results (`python evaluate.py`)  
- ✅ Upload trained model & metrics as **Artifacts**

---

### 🧭 4. Download Artifacts
After a successful run (green ✔):
1. Scroll to the **bottom** of the workflow run page.  
2. Find the **Artifacts** section (e.g., `model_artifact.zip`, `metrics.json`).  
3. Click to **download** your trained model and evaluation results.

---

## 💻 Run Locally (Optional)

If you’d like to run everything on your own computer instead of GitHub Actions:

```bash
# 1. Clone your fork
git clone https://github.com/romaisaahmad6671/mlopsclassactivity3.git
cd mlopsclassactivity3

# 2. Create a virtual environment
python -m venv .venv
# Activate it:
# Windows → .venv\Scripts\activate
# macOS/Linux → source .venv/bin/activate

# 3. Install dependencies
pip install --upgrade pip
pip install -r requirements.txt

# 4. Run the scripts
python preprocess.py
python train.py
python evaluate.py


## 📚 References

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [MLOps with GitHub Actions](https://mlops.community/github-actions-for-mlops/)
- [Continuous Delivery for Machine Learning (CD4ML)](https://martinfowler.com/articles/cd4ml.html)
