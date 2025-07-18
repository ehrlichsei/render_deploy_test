# Render Deployment Test

A simple Flask web application to test deployment on Render.

## Local Development

1. Clone this repository:
   ```
   git clone <your-repo-url>
   cd render_deploy_test
   ```

2. Create and activate a virtual environment:
   ```
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Run the application:
   ```
   python app.py
   ```

5. Open your browser and navigate to `http://localhost:5000`

## Deploying to Render

1. Create a free account on [Render](https://render.com/)

2. From the Render dashboard, click "New" and select "Web Service"

3. Connect your repository or use the "Deploy from existing repository" option

4. Configure your web service with these settings:
   - **Name**: Your app name (e.g., render-deployment-test)
   - **Environment**: Python
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `gunicorn app:app`

5. Click "Create Web Service"

Render will automatically build and deploy your application. Once the deployment is complete, you can access your app at the provided URL.

## Project Structure

- `app.py`: The main Flask application
- `templates/`: HTML templates for the web pages
  - `index.html`: Home page
  - `about.html`: About page
- `requirements.txt`: Python dependencies
- `Procfile`: Instructions for Render on how to run the application
