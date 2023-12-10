# Auto Scaling Flask App

## Overview
This project is an implementation of a scalable, auto-scaling web application using Flask, deployed on Azure App Services. It demonstrates the application of Flask knowledge to build a web-hosted app that scales automatically based on user demand.
Video: [Click Here](https://drive.google.com/file/d/1_8HVdRz2ULlDu73NZJUHgxxn3xqZXkf0/view?usp=drive_link)

## Instructor
Lead Instructor: Derek Wales

## Requirements
- [Azure App Services](https://azure.microsoft.com/en-us/services/app-service/)
- Docker
- Flask

## Installation & Running the Application

### Step 1: Clone the Repository
Clone this repository to your local machine using:
```bash
git clone https://github.com/nogibjj/levia_individual_proj4.git
```
### Step 2: Set up Azure App Service
- Follow Azure's documentation to set up an App Service.
 (Reference: https://learn.microsoft.com/en-us/azure/developer/python/tutorial-containerize-simple-web-app-for-app-service?tabs=web-app-flask)
- Ensure that the service is configured for auto-scaling.

### Step 3: Docker Setup
To get your Flask application running inside a Docker container, follow these steps:

1. **Install Docker**: If you haven't already installed Docker on your machine, download and install it from [Docker's official website](https://www.docker.com/get-started).

2. **Build the Docker Image**: Navigate to the root directory of the cloned repository where the Dockerfile is located and run the following command to build the Docker image:
    ```bash
    docker build -t myflaskapp .
    ```
   This command creates a Docker image named `myflaskapp` based on the instructions in your Dockerfile.

3. **Run the Docker Container**: After successfully building the image, you can run the container locally to test the application. Use the command:
    ```bash
    docker run -p 5000:5000 myflaskapp
    ```
   This command runs the container and maps the container's port 5000 to the local machine's port 5000. You can then access the Flask application by navigating to `http://localhost:5000` in your web browser.


### Step 4: Deploy to Azure
- Push the Docker container to DockerHub or Azure Container Registry.
- Deploy the container to Azure App Service.

## App
- Azure Setup
![Azure Setup](https://github.com/nogibjj/levia_individual_proj4/blob/main/images/azure.png)

- Dockerhub
![Dockerhub](https://github.com/nogibjj/levia_individual_proj4/blob/main/images/dockerhub.png)
- App
![APP1](https://github.com/nogibjj/levia_individual_proj4/blob/main/images/page1.png)
![APP2](https://github.com/nogibjj/levia_individual_proj4/blob/main/images/page2.png)

## Criteria
- A README.md file (15 points): This should clearly explain what the project does, its dependencies, how to run the program, and conclude with actionable and data-driven recommendations to a hypothetical management team.
    - Clarity and completeness of README: 10 points
    - Quality of conclusion and recommendation: 5 points
- GitHub Repo (20 points): A complete GitHub Repo that contains all required scripts and documentation to run your application.
- Flask App (20 points):
    - Functionality within Docker/(Platform): 10 points
    - Creativity/sophistication, full credit (all 20 points for this section) will be given to students who have a functioning embedded LLM within Flask, otherwise: 10 points.
- Use of DockerHub (Or equivalent) (10 points): Hosting your functioning container on DockerHub.   
- Azure Web App (Or equivalent) (15 points): Successfully deploying your container via Azure Web App to a public endpoint. This can be done either directly from Docker or through Azure container registry.
- Video Demo (20 points): A YouTube link in README.md showing a clear, concise (2-5min) walkthrough and demonstration of your application.      
    The video should be high-quality (both audio and visual), not exceed the given time limit, and be linked in the README via a private or public YouTube link.
    Clarity of explanation: 8 points
    Quality demonstration of the project: 7 points
    Quality of video and audio: 5 points
