# service-principle-guide-azure
This is a walk through guide for people to make an Azure Service Principle to use to deploy resources on Azure.

This repoistory has been designed to show step by step how to create a service principle and extract the values for it to use for Terraform deployments.

[Lab Exercises File Structure Github Repoistory](https://github.com/DFW1N/terraform-lab-file-structure)

# Prerequisites

1. Azure Subscription

# Create Service Principle Account in Azure and setup permissions

1. Log into https://portal.azure.com/ 
2. Open Azure Active Directory and click on App Registrations 

![image](https://user-images.githubusercontent.com/45083490/133249706-c03703b2-4224-434d-ba12-b4b544c322e9.png)

3. Click on “+ New App Registration” button and fill the details. Provide a meaningful name and Click on “Register” button

![image](https://user-images.githubusercontent.com/45083490/133249547-4f07b3ac-285a-4ef2-83a1-9296b08f765b.png)

4. Note down the details on the next screen. You need Application ID and Tenant ID later when setting up the terraform deployment connection via service principle

![image](https://user-images.githubusercontent.com/45083490/133249475-046789f1-be72-4409-aa95-7e1269e21ffb.png)

5. Select Certificates & Secrets on left hand side and click on “+ New Client Secret” button
 
![image](https://user-images.githubusercontent.com/45083490/133249876-a773c663-43bd-46fa-8053-2d7e4e7863bc.png)

6. Add description and click on “Add” button. Copy the secret as you need it later to setup connection

![image](https://user-images.githubusercontent.com/45083490/133249968-e78a98c7-c789-4b7b-8a1d-103a7dc4cc95.png)

**Note: The secret will not display again if you forget to copy. You might need to create another secret. **

7. Search for subscription in Azure search blade and select subscription 

![image](https://user-images.githubusercontent.com/45083490/133250203-30b1242a-f23e-4028-8754-8dd08408edac.png)

8. Select your subscription where you are going to deploy your terraform deployment

![image](https://user-images.githubusercontent.com/45083490/133250294-5ab12f07-8277-4221-b9c7-65a0882c2693.png)

9. Following Diagram display step by step instructions to assign owner role to your App for subscription. Select the app and Save it as owner or contributor

![image](https://user-images.githubusercontent.com/45083490/133250409-98999665-a7ae-49f2-a425-cd16ec0f0fe2.png)

10. Also copy the subscription ID as you need to for your system environment variables or inside your provider.tf file.

![image](https://user-images.githubusercontent.com/45083490/133250500-c3fba1a8-4ba2-439a-88a8-9494509101b7.png)

# Required values for Terraform using a Service Principle


subscription_id = "00000000-0000-0000-0000-000000000000"
client_id       = "00000000-0000-0000-0000-000000000000"
client_secret   = "00000000-0000-0000-0000-000000000000"
tenant_id       = "00000000-0000-0000-0000-000000000000"


