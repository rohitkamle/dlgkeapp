# dlgkeapp

# Sample Web Application Deployment

This repository contains files and configurations to deploy a sample web application on a Kubernetes cluster using GitHub Actions.

## Prerequisites

Before running the GitHub Actions workflow, make sure you have performed the following steps:

1. **Configure Google Cloud SDK**: Execute the commands in `gcloud-commands.sh` in your Google Cloud Shell or ensure that you have configured the Google Cloud SDK.

2. **Update GitHub Action Secrets**:

    - `GCP_REGION`: Set this to your desired Google Cloud region.
    - `GKE_CLUSTER_NAME`: Set this to the name of your GKE cluster.
    - `ARTIFACT_URL`: Set this to the URL of your Google Cloud Artifact Registry repository.

## Repository Structure

- `.github/workflows/app-deploy.yaml`: GitHub Actions workflow file for deploying the application.
- `helm-chart/`: Helm chart for deploying the web application.
  - `values.yaml`: Configuration file for Helm values.
- `webapp1/`: Sample web application files.
  - `Dockerfile`: Dockerfile for building the web application image.
  - `index.html`: Sample HTML code for the web application.

## GitHub Actions Workflow

The GitHub Actions workflow performs the following steps:

1. **Build Docker Image**: Builds the Docker image for the web application.
2. **Push to Artifact Registry**: Pushes the Docker image to the specified Artifact Registry repository.
3. **Deploy with Helm**: Deploys the web application to the Kubernetes cluster using Helm.

## Helm Chart Configuration

You can customize the deployment using the Helm chart configuration in `helm-chart/values.yaml`. Update this file to change deployment parameters.

## How to Run

1. Fork this repository.
2. Update the GitHub Action secrets in your forked repository settings.
3. Commit changes to trigger the GitHub Actions workflow.
4. Monitor the workflow progress in the "Actions" tab of your GitHub repository.

