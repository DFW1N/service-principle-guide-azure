# service-principle-guide-azure
This is a walk through guide for people to make an Azure Service Principle to use to deploy resources on Azure.

This repoistory has been designed to show step by step how to create a service principle and extract the values for it to use for Terraform deployments.

[Lab Exercises File Structure Github Repoistory](https://github.com/DFW1N/terraform-lab-file-structure)

# Prerequisites

1. Azure Subscription

# Create Service Principle Account in Azure and setup permissions

1. Log into https://portal.azure.com/ 
2. Open Azure Active Directory and click on App Registrations 

3. Click on “+ New App Registration” button and fill the details. Provide a meaningful name and Click on “Register” button 
![image](https://user-images.githubusercontent.com/45083490/133249547-4f07b3ac-285a-4ef2-83a1-9296b08f765b.png)

4. Note down the details on the next screen. You need Application ID and Tenant ID later when setting up the connection details
![image](https://user-images.githubusercontent.com/45083490/133249475-046789f1-be72-4409-aa95-7e1269e21ffb.png)

5. Select Certificates & Secrets on left hand side and click on “+ New Client Secret” button
