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

![Access Secrets](https://github.com/user-attachments/assets/9063db54-6c4b-4d1a-8e40-eb25a42528b0)
![Username and password](https://github.com/user-attachments/assets/c273849d-3a1b-4204-a954-cba4daf99a28)
![Add Secrets](https://github.com/user-attachments/assets/52609f57-d4e2-4532-924b-6d52e2b5e590)
![Web App](https://github.com/user-attachments/assets/c60616c9-1f95-4181-99fb-187f2dce5b27)
![Click the URL](https://github.com/user-attachments/assets/510f4d3f-0a67-4bb8-8fb2-b7592f2b625e)
![Output](https://github.com/user-attachments/assets/d2ff7d04-29b7-4f03-be9f-b81268c06d15)






