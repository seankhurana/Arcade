
🚀 **LAB: Deploy a Streamlit App Integrated with Gemini Pro on Cloud Run**

Hey everyone! 👋 In this lab, we'll be deploying a Streamlit app integrated with Gemini Pro on Google Cloud Run. This is a great way to showcase your machine learning models or data visualizations in a web app!

🔧 **Code Setup:**

First, clone the repository and navigate to the project directory:

```bash
git clone https://github.com/GoogleCloudPlatform/generative-ai.git
cd generative-ai/gemini/sample-apps/gemini-streamlit-cloudrun
```

Next, set up a virtual environment and install the required packages:

```bash
python3 -m venv gemini-streamlit
source gemini-streamlit/bin/activate
pip install -r requirements.txt
```

🚀 **Deployment:**

Now, let's deploy the Streamlit app to Cloud Run. Replace `YOUR Project ID` and `YOUR Region` with your actual project ID and preferred region:

```bash
GCP_PROJECT='YOUR Project ID'
GCP_REGION='YOUR Region'

streamlit run app.py \
  --browser.serverAddress=localhost \
  --server.enableCORS=false \
  --server.enableXsrfProtection=false \
  --server.port 8080
```

That's it! Your Streamlit app should now be deployed and accessible. Feel free to customize the app and experiment with different features.
Here's Task 2 formatted separately:

```markdown
## Task 2: Create Artifact Repository and Submit Docker Image

### Command to Create Artifact Repository:

```bash
AR_REPO='gemini-repo'
SERVICE_NAME='gemini-streamlit-app' 
gcloud artifacts repositories create "$AR_REPO" --location="$GCP_REGION" --repository-format=Docker
```

### Command to Submit Docker Image to Artifact Repository:

```bash
gcloud builds submit --tag "$GCP_REGION-docker.pkg.dev/$GCP_PROJECT/$AR_REPO/$SERVICE_NAME"
```

Replace `YOUR Project ID` and `YOUR Region` with your actual project ID and preferred region. This will create an artifact repository and submit the Docker image to the repository.

Let me know if you have any questions or need further assistance.
```

Let me know if you have any questions or need further assistance. Happy coding! 🚀


