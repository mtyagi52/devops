Project: Build a Docker Jenkins Pipeline to Implement CI/CD Workflow

Objective:
Demonstrate the continuous integration and delivery by building a Docker Jenkins Pipeline.
Solution build should demonstrate below capabilities:

• Availability of the application and its versions in the GitHub
• Track their versions every time a code is committed to the repository
• Create a Docker Jenkins Pipeline that will create a Docker image from the Dockerfile and host it on Docker Hub
• It should also pull the Docker image and run it as a Docker container
• Build the Docker Jenkins Pipeline to demonstrate the continuous integration and continuous delivery workflow
Project goal
is to deliver the software product frequently to the production with high-end quality.
Tools required:
Docker, Docker Hub, GitHub, Git, Linux (Ubuntu), Jenkins
Project Expected Result:
Jenkins pipeline with stages as shown below, demonstrating the Springboot application build and deployment process automated with Docker and Jenkins with 'Pipeline as a Code' approach
[pipeline output image](https://github.com/vdharmaraj/PGDO_Proj3/blob/681fdb351bdec410700e161758e2cacc4ccc9bed/Documentation/Jenkins_pipeline_result.JPG?raw=true)
Project Documentation
Click [here](https://github.com/vdharmaraj/PGDO_Proj3/blob/681fdb351bdec410700e161758e2cacc4ccc9bed/Documentation/PG%20DO%20-%20DevOps%20Certification%20Training_Project-3_Vignesh_Dharmaraj.pdf) to access the project documentation I have created to submit for my DevOps PG certification program requirements
Solution overview:
1) On a Linux (ubantu) machine, we are installing and configuring jenkins server.
2) In the jenkins server we are creating the pipeline based project (with the Jenkinsfile available in this repo as source)
3) First Stage in the pipeline is to pull the latest springboot application (index.html) changes from SCM (Git-Hub) 4) Next stage in the pipeline is to create a build using maven tool and the pom.xml file available in the code repository
5) Next stage in the pipeline will create docker image based on the standard java container with our jar executable created as a result of the build process in the previous step (Dockerfile available in the repo is responsible to create this image)
6) Next stage in the pipleline will push the lastest doker image created in the previous stage to the Docker Hub (remote image repository)
7) Next stage in the pipeline will remove any existing containers of our application
8) Next stage in the pipeline will start new container with the latest image (including our latest changes of springboot application) pulled from docker hub
9) Next stage in the pipeline will remove any old images in our linux machine.
