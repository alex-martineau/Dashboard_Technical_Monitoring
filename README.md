# 📊 Dashboard Technical Monitoring

## 🚀 Description

This project is a Streamlit application that creates an interactive credit scoring dashboard.
It connects to an external API to download a scoring model and perform creditworthiness predictions, integrating visual analytics with Plotly, SHAP, and Seaborn.

## 📂 Project Structure

- dashboard.py → Main Streamlit application.
- requirements.txt → Python dependencies.
- runtime.txt → Python version used.
- Procfile → Launch file for deployment (Heroku/Render).
- my_file.csv → Customer data (⚠️ must be present to run the dashboard).

## 🛠 Local Installation

**1. Clone the repository**

git clone https://github.com/alex-martineau/Dashboard_Technical_Monitoring.git
cd Dashboard_Technical_Monitoring

**2. Create a virtual environment**

python -m venv venv
source venv/bin/activate # Linux / Mac
venv\Scripts\activate # Windows

**3. Install dependencies**

pip install --upgrade pip
pip install -r requirements.txt

**4. Add environment variables**

Create a .env file at the root of the project:

MODEL_PASSWORD=Credit-Scoring-2025
API_URL=https://my-scoring-app-546acd78d8fa.herokuapp.com/

(⚠️ These values ​​must be adapted according to your scoring API.)

**5. Launch the dashboard**

streamlit run dashboard.py

Then open http://localhost:8501
in your browser.

## ☁️ Deployment (Heroku / Render)

**1. Heroku**

heroku create my-scoring-dashboard
git push heroku main

Configure the environment variables on Heroku:

heroku config:set MODEL_PASSWORD=Credit-Scoring-2025
heroku config:set API_URL=https://my-scoring-app-546acd78d8fa.herokuapp.com/

**2. Render**

- Create a new web service → Choose your GitHub repository.
- Start command:
web: streamlit run dashboard.py --server.port=$PORT --server.enableCORS false

- Add the MODEL_PASSWORD and API_URL environment variables to the Render configuration table.

**🔒 Security**

- ⚠️ MLflow is vulnerable below 2.22.2. Make sure to update your requirements.txt file:
mlflow>=2.22.2
mlflow-skinny>=2.22.2
- ⚠️ Never put passwords or API keys in clear text in your code → use environment variables.
- ⚠️ Check the integrity of the downloaded model before loading it with joblib.load().

**✅ To-do / Improvements**

- Add an integrity check (hash/signature) on the downloaded model.
- Document the expected format of my_file.csv.
- Migrate to Python 3.11 (more future-proof than 3.10).
- Implement automated tests.

## 👨‍💻 Author

**Alexandre Christophe Dominque Martineau**
- [GitHub](https://github.com/alex-martineau)
- [LinkedIn](https://www.linkedin.com/in/alexandre-martineau-170ab973/)
