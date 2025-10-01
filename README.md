# 📂 Dashboard Technical Monitoring & Technology Watch

## 👨‍💻 Context

This repository contains **two separate deliverables** created as part of Project 8 of the Data Scientist course offered by OpenClassrooms & CentraleSupélec :

- Deployment of a **credit scoring dashboard** (visualization, interpretability, API).
- Conducting **technology monitoring** using NLP and Transformer-type models.

⚠️ As the original datasets are large or confidential, they are **not included in this repository**.
The objective is to demonstrate the **methodological and technical approach**, not to provide a directly executable project.

## 📊 Part 1 – Credit Scoring Dashboard

📁 File: dashboard/

This part is from **Project 7**. It illustrates the implementation of a **Streamlit dashboard** to:

- Load and run a scoring model via an external API.
- Visualize a customer's credit scores.
- Explore the data using univariate and bivariate analyses.
- Explain model decisions using **SHAP values** ​​and **Feature Importance**.

**Contents:**

- dashboard.py → Streamlit main application.
- requirements.txt, runtime.txt, Procfile → files required for deployment (Heroku/Render).
- **Not included**: my_file.csv (dataset too large).

**Technologies used:**

**- Python 3.10+, Streamlit, Plotly, SHAP, Seaborn, MLflow, Joblib.**

**For more information:**

👉 See the dashboard's specific README.

## 🔍 Part 2 – Technology Monitoring (NLP)

📁 File: veille_technologique/

This part is from **Project 6**.
It consists of a **methodological note** and a **technical notebook** aimed at comparing two NLP models:

- all-MiniLM-L6-v2 (distilled, lightweight, and fast model).
- bert-base-uncased (heavier reference model).

**Objectives:**

- Evaluate their performance in e-commerce product classification.
- Explore the quality of embeddings (t-SNE, KMeans clustering, ARI).
- Highlight the advantages of distilled models for production use.

**Content:**

- Martineau_Alexandre_2_notebook_veille_022025.ipynb → Complete notebook.
- Martineau_Alexandre_3_methodological_note_022025.pdf → Written note, with interpretation of results.

**Technologies used:**

**- Python, Transformers (Hugging Face), scikit-learn, t-SNE, KMeans.**

## 🚀 Demonstrated strengths

- Deployment of an interactive and interpretable application for credit scoring.
- Implementation of a clear and reproducible workflow for data processing.
- Ability to popularize technology monitoring and link it to concrete use cases.
- Solid knowledge of MLflow, NLP, SHAP, data visualization, and cloud deployment.

## 👤 Author

**Alexandre Christophe Dominique Martineau**
- [GitHub](https://github.com/alex-martineau)
- [LinkedIn](https://www.linkedin.com/in/alexandre-martineau-170ab973/)
