# Hello World of CI: FastAPI with GitHub Actions and ngrok

This project demonstrates how to run a **FastAPI** app on **GitHub Actions** and expose it publicly using **ngrok**.

## 🚀 How it Works
1. Push code to GitHub.
2. GitHub Actions runs the FastAPI app.
3. **ngrok** generates a public URL for the app.
4. Access the app using the public URL in the GitHub Actions logs.

## 🛠️ Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/VatsAmanJha/hello-world-of-ci.git
   cd hello-world-of-ci
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the app locally (optional):
   ```bash
   uvicorn main:app --host 0.0.0.0 --port 8000
   ```

4. Push to GitHub:
   ```bash
   git push origin main
   ```

## 📝 GitHub Actions Workflow

The workflow is in `.github/workflows/run-api.yml` and does the following:
- Installs **Python 12**.
- Installs dependencies.
- Runs FastAPI.
- Starts **ngrok** to expose the app.

Once the workflow finishes, the **public URL** will be in the GitHub Actions logs.

## 🌍 Access the API

In the GitHub Actions logs, find the **ngrok URL**:
```sh
https://random-ngrok-url.ngrok.io
```
Open it in a browser to see your FastAPI app!

---