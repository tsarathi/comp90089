# MIMIC-IV on Google BigQuery: Setup Guide

## Table of Contents
1. [Access MIMIC-IV Dataset on PhysioNet](#access-mimic-iv-dataset-on-physionet)
2. [Setup Python Virtual Environment](#setup-python-virtual-environment)
3. [Install Google Cloud SDK](#install-google-cloud-sdk)
4. [Initialize Google Cloud Account](#initialize-google-cloud-account)
5. [Run Jupyter Notebook](#run-jupyter-notebook)

### 1. Access MIMIC-IV Dataset on PhysioNet
To access MIMIC-IV in BigQuery, you need to link your PhysioNet account to Google Cloud and request access to the MIMIC-IV dataset.

#### Steps:
- Link your PhysioNet account to your Google Cloud account by following these instructions: [PhysioNet Profile Settings](https://mimic.mit.edu/docs/gettingstarted/cloud/link/).
- After linking, request access to MIMIC-IV on the PhysioNet project page. It is recommended to select the **BigQuery option**: [MIMIC-IV Access Request](https://mimic.mit.edu/docs/gettingstarted/cloud/request/).
- Once access is granted, you’ll receive a confirmation email. For detailed instructions on accessing MIMIC-IV in BigQuery, visit: [BigQuery Access Guide](https://mimic.mit.edu/docs/gettingstarted/cloud/bigquery/).
- Activate Google Cloud’s 90-day free trial, if needed, and access BigQuery here: [BigQuery Console](http://console.cloud.google.com/bigquery).

### 2. Setup Python Virtual Environment
A virtual environment is recommended for isolated package management.

1. Install `virtualenv`:
    ```bash
    pip install virtualenv
    ```
   
2. Create and activate the virtual environment (named `comp90089` in this case):
    ```bash
    virtualenv comp90089
    source comp90089/bin/activate
    ```

3. Install necessary packages within the virtual environment:
    ```bash
    comp90089/bin/pip install google-cloud-bigquery jupyter
    ```

### 3. Install Google Cloud SDK
To manage your Google Cloud resources, install the Google Cloud SDK.

1. Install Google Cloud SDK:
    ```bash
    brew install --cask google-cloud-sdk
    ```
2. Initialize the SDK:
    ```bash
    gcloud init
    ```

### 4. Initialize Google Cloud Account
After installing the SDK, authenticate with your Google Cloud account to access BigQuery.

1. Run the following to initialize your account:
    ```bash
    gcloud auth application-default login
    ```
2. Select or create a project and set up billing if prompted.

### 5. Run Jupyter Notebook
After setting up everything, you can start a Jupyter Notebook to interact with MIMIC-IV data.

1. Start the Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
