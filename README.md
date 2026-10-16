# DevOps CI/CD Assessment 

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
