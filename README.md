# Serverless-Event-Driven-Architecture-with-CI-CD
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1 - Define Infrastructure with Terraform
- Step 2 - Write a Lambda Function with Python
- Step 3 - Set Up CI/CD with AWS CodePipeline
- Step 4

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

- Step 3 - Set Up CI/CD with AWS CodePipeline







       





