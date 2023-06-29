# GCP App Test
Using App Engine to deploy a todo app and then launching it as the exported Terraform code.

## GCP CLI Setup

### Ubuntu

Official installation docs can be found [here](https://cloud.google.com/sdk/docs/install#deb).

```bash
# Install Updates
sudo apt-get update

# Install Software Dependencies
sudo apt-get install apt-transport-https ca-certificates gnupg curl sudo

# Add the gcloud CLI distribution URI as a package source.
echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list

# Import the Google Cloud public key
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key --keyring /usr/share/keyrings/cloud.google.gpg add -

# Update and install the gcloud CLI
sudo apt-get update && sudo apt-get install google-cloud-cli

# 

```

## Launch a Sample Node app

App Engine samples can be found in [this](https://github.com/GoogleCloudPlatform/nodejs-docs-samples/tree/main/appengine) repo.


```bash
# Copy over a sample app.
cp nodejs-docs-samples/appengine/hello-world/standard/* gcp-app-test

# Install Node Dependencies
npm install

# Run the App to test It
node app.js
```