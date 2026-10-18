# AWS DevOps Production Assessment

This repository contains three tasks covering CI/CD automation, S3 and CloudFront static hosting, and AWS Auto Scaling with an Application Load Balancer.

**Note:** Task 2 is partially completed due to pending AWS account verification.


# Task 1: DevOps CI/CD Assessment 

# About

I created a small Flask application and set up a CI/CD workflow to test the code and push the Docker image to Amazon ECR.

# What I Did

 Created a Flask app with a home page and health-check endpoint.
 
 Wrote unit tests using Pytest.
 
 Used GitHub Actions to run tests and build the Docker image.
 
 Configured AWS ECR to store the image.
 
 Deployed the application using Kubernetes manifests.
 
 Checked that both application endpoints were working.

# Tools

Python, Flask, Pytest, Docker, GitHub Actions, AWS ECR, Kubernetes, Minikube.

# Project Check
 Both unit tests passed.
 GitHub Actions workflow completed successfully.
 Docker image was pushed to ECR.
 Two Kubernetes pods were running.
 Application health check returned healthy status.

# Screenshots


### Project Structure

<img width="758" height="225" alt="1 25 final project tree" src="https://github.com/user-attachments/assets/b4351406-ed68-4355-b822-5d12ef316748" />


### Versions
<img width="721" height="310" alt="1 version" src="https://github.com/user-attachments/assets/d9ff61ee-f90c-4aed-af0c-027ec819cf83" />

### Project Directory Created
<img width="942" height="118" alt="1 2 project Dir" src="https://github.com/user-attachments/assets/420f4a74-f267-4dad-bc46-bda9c5b1c8c9" />


### Tests
[Pytest Passed]

<img width="1345" height="236" alt="1 5 pytest passed" src="https://github.com/user-attachments/assets/4cb89c78-4014-44ce-ab7d-fd69e1f3b301" />


### Docker Build
[Docker Build]

<img width="1347" height="513" alt="1 6 image build" src="https://github.com/user-attachments/assets/675c6c5e-a1c9-418a-9574-b100b3452b32" />


### GitHub Actions
[GitHub Actions]

<img width="1350" height="672" alt="1 11 GitHub-Actions-Success" src="https://github.com/user-attachments/assets/61d66c27-b80d-499f-afd9-3e73d73f862c" />


### ECR Image Push
[ECR Image Push]

<img width="1359" height="273" alt="1 14 ECR-Docker-Image-Pushed" src="https://github.com/user-attachments/assets/59a3aa40-6e5f-4805-bcee-f9a53608bda0" />


### CI/CD Result
[CI/CD Success]

<img width="1351" height="669" alt="1 20 test+ ECR success green" src="https://github.com/user-attachments/assets/511a2f82-4743-480a-8cd2-6ba6106b27ca" />


### Kubernetes
[Kubernetes Ready]

<img width="809" height="190" alt="1 22 minukube ready" src="https://github.com/user-attachments/assets/7036206e-5caa-477d-b4d1-6090baa7274c" />


### Kubernetes Deployment
[Deployment Running]

<img width="871" height="140" alt="1 23 Kubernetes_Deployment_Running" src="https://github.com/user-attachments/assets/7e7de8a4-de7a-4fde-ad1c-adf23e1c55e1" />


### Application Health Check
[Health Check]

<img width="783" height="99" alt="1 24 Kubernetes_Application_Health_Check" src="https://github.com/user-attachments/assets/a927c933-eb6a-4d62-8fec-64cdf63cdf2a" />




 



Final Result

I was able to test the application, push its Docker image to ECR, and run it successfully on Kubernetes.




# Task 2: Amazon S3 and CloudFront

## Objective
Host a static website using Amazon S3 and configure Amazon CloudFront as a content delivery network (CDN), with restricted direct access to the S3 bucket.

## AWS Services
Amazon S3

Amazon CloudFront

AWS Support for account verification

## Implementation

1. Created an S3 bucket named `vaibhav-cloudfront-static-demo-2026` in the Mumbai region (`ap-south-1`).
2. Kept the S3 bucket private with Block Public Access enabled.
3. Uploaded the static website's `index.html` file to the S3 bucket.
4. Started configuring a CloudFront distribution using the S3 bucket as the origin.
5. Selected the recommended private S3 origin access configuration.
6. CloudFront distribution creation was blocked by an AWS account verification requirement.

## Screenshots and Evidence

| Screenshot | Description |

SS-01 Created the S3 bucket in the Mumbai AWS region. 
<img width="1348" height="626" alt="2 1 Bucket creataed" src="https://github.com/user-attachments/assets/9152a632-b92d-4257-bc1b-60e21adb462f" />

SS-02 Uploaded the static website's `index.html` object to the S3 bucket. 
<img width="1359" height="589" alt="2 2Object Uploaded " src="https://github.com/user-attachments/assets/2969cf26-3c30-40cc-b1cc-599f7547dcff" />

SS-03 CloudFront distribution creation blocked by the AWS account verification requirement. 
<img width="1350" height="599" alt="2 3 CloudFront_Account_Verification_Error" src="https://github.com/user-attachments/assets/0e373459-b151-4b16-afdf-3c88a7fbc62c" />


## Current Status

**Partially Completed — CloudFront verification pending.**

The S3 bucket was created and the website object was uploaded. CloudFront distribution creation could not be completed because AWS requires account verification.

## Pending Work

Resolve the AWS account verification requirement through AWS Support.

Create the CloudFront distribution with private S3 origin access.

Configure and verify the default root object (`index.html`).

Test website access through the CloudFront distribution domain.

Verify that direct public access to the S3 bucket is restricted.

Perform a CloudFront cache invalidation and capture the result.

## Expected Outcome

Serve the static website through CloudFront while keeping the S3 bucket private. These final steps remain pending until the account verification restriction is resolved.





# Task 3: AWS Auto Scaling Group and Application Load Balancer

## Objective
Deploy a highly available web application using an Application Load Balancer (ALB), an Auto Scaling Group (ASG), and EC2 instances.

## AWS Resources
VPC and public subnets across two Availability Zones

Internet Gateway and route table

Security Groups for ALB and EC2 instances

EC2 Launch Template

Application Load Balancer

Target Group with HTTP health checks

Auto Scaling Group with desired capacity 2

Target tracking scaling policy with average CPU utilization of 70%

## Implementation
1. Created the VPC, subnets, Internet Gateway, and route table.
2. Configured Security Groups for the ALB and EC2 instances.
3. Created a Launch Template with Amazon Linux 2023 and Apache web server user data.
4. Created a Target Group with HTTP health checks on port 80.
5. Created an internet-facing Application Load Balancer.
6. Attached the Target Group to an Auto Scaling Group.
7. Configured the ASG capacity and CPU target tracking policy.
8. Tested the application through the ALB DNS name.
9. Checked target health and reviewed ASG Activity History during replacement testing.

## Evidence
Screenshots 
Created the VPC for the ASG and ALB setup.
<img width="1347" height="354" alt="3 1 devops-asg-vpc" src="https://github.com/user-attachments/assets/ebddccfc-6b41-480f-bb6e-75eff0c356ee" />


Created two subnets in different Availability Zones.
<img width="1363" height="355" alt="3 2 subnet" src="https://github.com/user-attachments/assets/47c160e7-ab0c-4b5c-9634-c1badaf63300" />


Attached the Internet Gateway to the VPC.
<img width="1360" height="241" alt="3 3 Internet Gateway attached" src="https://github.com/user-attachments/assets/9eac5ba1-6ee1-41a5-bcf9-be414e9d8abe" />

Configured the route table and subnet associations.
<img width="1346" height="585" alt="3 4 Route table and subnet associations" src="https://github.com/user-attachments/assets/e1fcf797-6ab8-48e3-9cf8-2ca990c71ae1" />

Created Security Groups for the ALB and EC2 instances.
<img width="1352" height="267" alt="3 5Both Security Groups in same VPC" src="https://github.com/user-attachments/assets/8a332c53-59ef-4756-ad1d-35cc5e7e1ef2" />

Created the EC2 Launch Template with Amazon Linux 2023 and Apache user data.
<img width="1347" height="590" alt="3 6Launch Template created" src="https://github.com/user-attachments/assets/ad2b5435-e367-4c1e-8200-56a9d8f1edcd" />

Created the Target Group with HTTP health checks.
<img width="1348" height="572" alt="3 7 Target Group created" src="https://github.com/user-attachments/assets/16e4a098-2c19-4957-bade-2e2f5983323d" />

Created the internet-facing Application Load Balancer.
<img width="1347" height="583" alt="3 8 ALB Active" src="https://github.com/user-attachments/assets/29b40270-c3bc-414f-b528-bc28a70e749a" />

Configured the Auto Scaling Group capacity.
<img width="1361" height="200" alt="3 9 ASG launch " src="https://github.com/user-attachments/assets/be384c40-1810-4363-8a8a-4cce7340e963" />

Verified instance launch events in ASG Activity History.
Configured CPU target tracking at 70%.
<img width="1338" height="598" alt="3 10 CPU target tracking set to 70%" src="https://github.com/user-attachments/assets/d88d3ce5-6687-4e38-bbf7-61d3af8a1a72" />

Verified web application access using the ALB DNS name.
<img width="1362" height="105" alt="3 11Website accessible through ALB DNS" src="https://github.com/user-attachments/assets/6654aa8f-f173-4135-ae51-d83c3e90da72" />

Verified healthy targets in the Target Group.
<img width="1350" height="602" alt="3 12 Two healthy targets" src="https://github.com/user-attachments/assets/e8700ba0-276c-4e75-9c12-2216d5a884ff" />

Captured target health status during replacement testing.
<img width="1118" height="341" alt="3 13 Unhealthy health-check evidence" src="https://github.com/user-attachments/assets/b58482ed-df2b-4ab0-bbec-09c625df1699" />

Verified the replacement instance became healthy.
<img width="1122" height="392" alt="3 14 — Replacement target healthy" src="https://github.com/user-attachments/assets/19640899-0392-448e-88d6-e63b184a33ec" />


## Result
The application was accessible through the ALB, and the Auto Scaling Group maintained the configured capacity. Scaling and replacement evidence is documented using the actual AWS console results.
