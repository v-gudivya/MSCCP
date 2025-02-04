# Integrating Google Cloud Platform Cloud Monitoring into Microsoft Sentinel
## Table of Contents
- [Introduction](introduction)
- [Step 1 Install the connector](step-1-install-the-connector)
- [Step 2 Add new collector](step-2-add-new-collector)
- [Step 3 Fill in required details](step-3-fill-in-required-details)
- [Terrraform scripts](terraform-scripts)
### Introduction
The Google Cloud Platform Cloud Monitoring Codeless Connector for Microsoft Sentinel enables seamless integration of Google Cloud Platform Cloud Monitoring logs with Microsoft Sentinel without the need for custom code. Developed as part of the Codeless Conector Platform(CCP), this connector simplifies the process of collecting and ingesting Cloud Monitoring logs from Google Cloud Platform into Microsoft Sentinel.
### Step 1 Install the connector
Install the **Google Cloud Platform Cloud Monitoring** connector from `Content Hub`
### Step 2 Add new collector
- After installing the connector, navigate to `Data Connectors` and select on the Google Cloud Platform Cloud Monitoring Connector.
- A new window pops up in the bottom, and click on `Open Connector Page`.
- Now, click on `Add new collector` button.
### Step 3 Fill in required details
Navigate to Google Cloud Console and select the project you want to monitor and fetch the following fields
- `Project ID` and `Project Number`: You can find these details in the home page of the project.
- `GCP subscription name`: If the subscription already exists, search for **Pub/Sub** section in the search bar and navigate to the subscription tab. You can find the details about subscrition name and subscription state.
- If the subscription does not exist, go to the **Topics** section and create a new topic with the desired topic ID.
- After the topic is created, proceed to the **Subscriptions** section and create a new subscription with the desired subscription ID by selecting the specific topic ID.
- Provide the appropriate details for the below mentioned fields based on your requirement:
  - Delivery Type
  - Message retention duration
  - Expiration period
  - Acknowledgement deadline
  - Subscription filter
  - Exactly once delivery
  - Message ordering
  - Dead lettering
  - Retry policy
- `Workload identity pool ID` and `Workload identity provider ID`: To get this ID, you must run the terraform script for Cloud Monitoring in cloud shell of Google Cloud Platform. You can find the script files in the home page of the connector or find them in the steps provided below.
### Terraform scripts
