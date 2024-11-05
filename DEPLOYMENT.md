
# Deployment Guide for SkyCast Weather App on Render

This guide provides step-by-step instructions to deploy the SkyCast Streamlit weather app on [Render](https://render.com/).

## Prerequisites

- A [GitHub](https://github.com/) account with your project code pushed to a repository.
- A [Render](https://render.com/) account.
- An OpenWeatherMap API key.

## Steps

### 1. Setup a GitHub Repository
1. Organize your project folder with the following files:
   - **app.py**: Main Python file containing the Streamlit app code.
   - **README.md**: Project description and information.
   - **requirements.txt**: List of dependencies (e.g., `streamlit`, `pyowm`, `pytz`, `plotly`, `matplotlib`).

2. To generate a `requirements.txt` file, run:
   ```bash
   pip freeze > requirements.txt
   ```

3. Push your project to a GitHub repository.

### 2. Create an Account on Render
- Sign up or log in on [Render.com](https://render.com/).

### 3. Deploy the Streamlit Application on Render
1. From your Render dashboard, click **New** and select **Web Service**.

2. Connect your GitHub account and select your repository with the Streamlit app.

3. **Configure your Web Service**:
   - **Name**: Choose a name for your app (e.g., `skycast-weather-app`).
   - **Region**: Choose the closest region to your primary user base.
   - **Branch**: Select the branch with your app’s code (e.g., `main`).
   - **Build Command**: `pip install -r requirements.txt`.
   - **Start Command**: `streamlit run app.py --server.port $PORT`.

4. **Environment Variables**:
   - Add your OpenWeatherMap API key as an environment variable:
     - **Key**: `API_key`
     - **Value**: Your OpenWeatherMap API key

5. **Instance Type**: Choose free or paid instance as per your needs.

6. Click **Create Web Service** to deploy. Render will start building and deploying your app.

### 4. Access and Share Your Deployed Application
- Render will provide a URL for your app once deployed. Visit this URL to confirm the app is running.

### 5. Additional Tips
- **Logs**: Check the Logs section on Render for troubleshooting.
- **Environment Variable Updates**: To update your API key, go to Environment Variables in Render.

---

Your Streamlit app should now be live and accessible online! 
