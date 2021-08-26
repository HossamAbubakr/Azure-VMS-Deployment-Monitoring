# Azzy Voting App, Azure VMS Deployment And Monitoring

## Table of Contents

- [Summary](#Summary)

- [Technologies](#Technologies)

- [Structure](#Structure)

- [Configuration](#Configuration)

- [Deployment](#Deployment)

## Summary

This voting website was configured, migrated and deployed to Azure as part of my **Cloud Developer using Microsoft Azure Nanodegree from Udacity**.

**It demonstrates my understanding and ability to configure the following :**

#### Azure Services

Azure Alert.  
Azure Monitor.  
Azure RunBook.  
Azure Automation.  
Azure VM Scale Sets.  
Azure Kubernetes Service.  
Azure Application Insights.    

#### Development

Create Azure and communicate with Azure Insight using the opencensus library to collect telemetry and performance data.

#### Deployment

Deploy an application using Azure VM Services.  
Configure auto scaling rules using VM Scale Sets.  
Configure Kubernetes Service for deployment and scaling.  

## Technologies
Flask was used for the backend.  
Python was used as the language of choice.   
Azure VM Services was used for hosting the app.    
Azure App Insights was for collecting telemetry data.  
Azure VM Scalte Sets was used for the autoscaling of the VM.

## Structure

```
|   azure-pipelines-instructions.md
|   azure-pipelines.yaml
|   azure-vote-all-in-one-redis.yaml
|   azure-vote.yaml
|   cloud-init.txt
|   create-cluster.sh
|   docker-compose.yaml
|   README.md
|   requirements.txt
|   setup-script.sh
|
+---azure-vote
|   |   config_file.cfg
|   |   Dockerfile
|   |   main.py
|   |
|   +---static
|   |       default.css
|   |
|   \---templates
|           index.html
|
+---instruction-screenshots
|       add-resource-vm-2.png
|       add-resource-vm-3.png
|       add-resource-vm.png
|       add-resource.png
|       configure-pipeline.png
|       create-new-pipeline.png
|       create-new-project.png
|       pipeline-connection-success.png
|       pipeline-connection.png
|       review-pipeline.png
|       run-pipeline.png
|       view-environment.png
|
\---submission-screenshots
    +---application-insights
    |       README.md
    |
    +---autoscaling-vmss
    |       README.md
    |
    +---kubernetes-cluster
    |       README.md
    |
    \---runbook
            README.md
```


## Configuration

### Look for
```python
key = 'Instrumentation Key'
```
And replace with your Azure App Insight Instrumentation Key

## Deployment

You will need the following : 
- [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)

Run the included configuration script **/setup-script.sh**  
```bash
 # Fork the current repo to your Github account. 
 # Clone locally
 git clone https://github.com/hossamabubakr/Azure-VMS-Deployment-Monitoring
 cd Azure-VMS-Deployment-Monitoring
 # Log in to Azure using 
 az login
 # The cloud-init.txt will install and start the nginx server
 # (a load balancer) and a few Python packages. 
 chmod +x setup-script.sh
 ./setup-script.sh
``` 

Then follow the details instructions in **/azure-pipelines-instructions.md**

