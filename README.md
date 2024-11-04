# Serverless-Event-Driven-Architecture-with-CI-CD

![Screenshot 2024-11-03 202218](https://github.com/user-attachments/assets/4987abe2-9d8d-4874-b084-c2c077e5d6f1)

</p>

This lab focuses on building a serverless architecture on AWS to send and store messages in DynamoDB using API Gateway and Lambda. This lab demonstrates how to design a lightweight, scalable serverless application on AWS, which is commonly used for backend APIs, data processing tasks, and other event-driven workflows.




<h2>Environments and Technologies Used</h2>

- AWS Lambda
- AWS API Gateway
- Amazon DynamoDB
- AWS CodePipeline
- AWS CodeBuild
- AWS IAM
- GitHub
- YAML
- Powershell
- AWS CLI

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Linux (Amazon Linux 2)
- AWS Lambda’s Execution Environment 

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1 - Define Infrastructure with Terraform
- Step 2 - Write a Lambda Function with Python
- Step 3 - Set Up CI/CD with AWS CodePipeline
- Step 4 - Set Up CodePipeline to Use GitHub
- Step 5 - Set Up the Build Stage
- Step 6 - Test the Architecture

<h2>Deployment and Configuration Steps</h2>

- Step 1 - Use Terraform to automate the provisioning of AWS resources like Lambda, API Gateway, and DynamoDB.

- 1. Terraform main.tf:

![Screenshot 2024-10-28 193434](https://github.com/user-attachments/assets/b8196c8e-1bcc-44a2-bd22-5890cdb9ebe5)
![Screenshot 2024-10-28 193458](https://github.com/user-attachments/assets/c66c7188-b48a-440c-b8c2-60fec3aaeeaa)

- 2. IAM Role for Lambda (iam.tf):

![Screenshot 2024-10-28 194346](https://github.com/user-attachments/assets/1881cd82-bbc2-45e5-bc39-49962517de05)

- 3. Deploy with Terraform
     - Terraform init
![Screenshot 2024-10-28 200424](https://github.com/user-attachments/assets/3460de15-7878-4021-8392-b8d7be680bd5)
![Screenshot 2024-10-28 201411](https://github.com/user-attachments/assets/c3925852-1708-4af9-9ccf-e83e03fc8bbc)

- Step 2 - Write a Lambda Function with Python

![Screenshot 2024-10-28 202917](https://github.com/user-attachments/assets/d4c1009d-2ec7-408e-8f16-abf1716eff1b)

  1. Zip the files

![Screenshot 2024-10-28 204125](https://github.com/user-attachments/assets/7e68055f-344b-41d3-9468-a7780ac18373)

   2. Plan the deployment with Terraform

![Screenshot 2024-10-28 204451](https://github.com/user-attachments/assets/17619449-9f16-478b-bb66-9400af99c59f)
![Screenshot 2024-10-28 204506](https://github.com/user-attachments/assets/dfdaf3ca-d1e9-4f30-af6c-c4e0a386d745)
![Screenshot 2024-10-28 204523](https://github.com/user-attachments/assets/5bbfe164-5701-4001-bbab-8844c0be1020)

- Step 3 - Set Up CI/CD with AWS CodePipeline using Github

![Screenshot 2024-10-31 165728](https://github.com/user-attachments/assets/30ca38b2-3815-40c3-8aa0-61eee0f713a7)

-  Initialize the Git Repository
![Screenshot 2024-10-31 171421](https://github.com/user-attachments/assets/1bf306f4-ec72-4ad8-b79b-52b89a29a925)
![Screenshot 2024-10-31 173006](https://github.com/user-attachments/assets/a4165eca-e580-4ac1-95dc-cdb6fcd5f339)

- Step 4: Set Up CodePipeline to Use GitHub

- 1. Go to the AWS Management Console → CodePipeline.
- 2. Click Create Pipeline.
- 3. Enter a name for your pipeline and click Next.
![Screenshot 2024-10-31 203556](https://github.com/user-attachments/assets/fa6b5379-2f60-403c-b9e4-c2f9fe35bd0e)
![Screenshot 2024-10-31 204032](https://github.com/user-attachments/assets/91eeab70-64cb-4ed2-933f-48f1205335a7)
![Screenshot 2024-10-31 204116](https://github.com/user-attachments/assets/c150b1fd-fea6-4d32-974c-a79cf3d6f77b)
![Screenshot 2024-10-31 222933](https://github.com/user-attachments/assets/3cdf419c-4d33-49d0-ad20-8dde094b2426)

- Step 5: Set Up the Build Stage

- 1. Create a new CodeBuild project:
- Use an Ubuntu image with Terraform and Python installed.
- In Buildspec (this file instructs CodeBuild what to do), create a buildspec.yml file in your repository with the following content:

![Screenshot 2024-10-31 224854](https://github.com/user-attachments/assets/c7132e25-0e2f-4245-a9c9-a5e6cd508830)

- This configuration does the following:
1. Install phase: Installs Terraform and Python 3.8.
2. Pre-build phase: Initializes Terraform.
3. Build phase: Applies the Terraform configuration.
4. Artifacts: Specifies that all files should be saved as artifacts after the build.
5. Save and commit the buildspec.yml file to your repository:

![image](https://github.com/user-attachments/assets/d02fa78c-cdda-4115-84b2-818fc87d982e)

- Step 6: Test the Architecture

- 1. Test API Gateway Endpoint:
- Get the API Gateway URL from the console.
- Use Postman or curl to send a POST request:

![Screenshot 2024-11-03 200607](https://github.com/user-attachments/assets/9b1844be-6da3-4da3-aa11-e84e22d115eb)

- Verify DynamoDB:

- Check DynamoDB to confirm that the event was stored.
![Screenshot 2024-11-03 200750](https://github.com/user-attachments/assets/551343e6-4302-4007-866d-57a5018a27ea)

















       





