## Azure Container Deploy

-Project Overview
This repository demonstrates a multi-cloud CI/CD workflow using GitHub Actions to build and deploy a containerized static website to Azure Web App for Containers. The Docker image is hosted on Azure Container Registry (ACR) and pulled automatically by the web app on deployment. This setup mirrors the AWS ECS Fargate deployment in structure and flow.
Tech Stack
- HTML / CSS / Static content
- Docker (Nginx container)
- Azure Container Registry (ACR)
- Azure Web App for Containers
- GitHub Actions (CI/CD pipeline)
---

## Architecture
![image](https://github.com/user-attachments/assets/390105a7-73ed-4920-bf2b-5a55dfb8d1b1)

---
## CI/CD Pipeline Overview
- GitHub Actions is triggered on each push to main.
- Workflow builds the Docker image using Dockerfile located at the root.
- Image is pushed to Azure Container Registry using secret-based authentication.
- Azure Web App automatically pulls the latest container image on deployment.
  
---

## Deployment Notes
- Region used: Central US
- App Service Plan: F1 (Free Tier)
- Note: East US region was unavailable due to VM quota limitations.

## Repository Structure
azure-container-deploy/
├── index.html
├── style.css
├── images/
├── Dockerfile
└── .github/
    └── workflows/
        └── docker-deploy.yml
---

![Access Secrets](https://github.com/user-attachments/assets/98c722b2-a76b-4545-a7ea-ac17270a26e7)
![Username and password](https://github.com/user-attachments/assets/c8110afa-b760-43aa-b724-b4ff6c188bbc)
![Add Secrets](https://github.com/user-attachments/assets/51486af0-63e3-4fc5-98fd-ec094462d448)
![Web App](https://github.com/user-attachments/assets/41f8910f-7045-47c9-84d5-8036d910d6d9)
![Click the URL](https://github.com/user-attachments/assets/f621189f-e38b-4409-ab84-e0193f0ce21d)
![Output](https://github.com/user-attachments/assets/d429f72b-8124-4b80-b95c-c8805d47194f)













