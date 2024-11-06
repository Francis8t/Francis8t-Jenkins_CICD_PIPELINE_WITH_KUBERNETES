# CI/CD Pipeline Integration with Jenkins & Kubernetes
![image](https://github.com/user-attachments/assets/a3fbd286-bc7c-4f79-8ae3-1907ccd0716f)


This project sets up a CI/CD pipeline using Jenkins, Docker, and Kubernetes to streamline software deployment. The pipeline integrates GitHub, Maven, SonarQube, Docker, Jenkins, Argo CD, and Kubernetes for automated, efficient, and reliable application deployment. A more detailed step-by-step guide on going about this project can be accessed on my [Medium Page](https://medium.com/@francis8t/ci-cd-pipeline-with-jenkins-docker-and-kubernetes-for-streamlined-software-deployment-591610efae5e).

## Key Steps

### 1. Prerequisites
- Set up a GitHub repository for source control and generate a personal access token for authentication.
- Launch an AWS EC2 instance to host Jenkins and other tools.
- Configure security groups to allow access to required ports.

### 2. Install Jenkins on EC2
- SSH into the EC2 instance and install Java.
- Use a script to install Jenkins, then configure it by accessing the Jenkins UI.
- Install necessary plugins, including Docker and SonarQube scanner plugins.

### 3. Set Up Jenkins Pipeline
- Create a new Jenkins pipeline job.
- Configure the pipeline to use a Jenkinsfile from the GitHub repository for build instructions.
- Define stages in the Jenkinsfile to:
  - Check out code from GitHub
  - Build the application with Maven
  - Run tests and SonarQube analysis
  - Package the application into a Docker image
  - Deploy the application to a Kubernetes cluster

### 4. Configure SonarQube for Code Quality Checks
- Install SonarQube on the EC2 instance.
- Allow access on port 9000 for the SonarQube dashboard.
- Generate a SonarQube token and add it to Jenkins credentials for integration.

### 5. Install Docker and Configure Permissions
- Install Docker on the EC2 instance.
- Grant Docker permissions to Jenkins and Ubuntu users to enable Docker commands in Jenkins.

### 6. Set Up Kubernetes Cluster and Argo CD
- Install Minikube and kubectl for local Kubernetes setup.
- Install Argo CD for managing application deployments on Kubernetes.
- Configure Argo CD UI for easier access and create an application for deployment.

### 7. Deploy and Monitor Application
- Use Jenkins to trigger pipeline builds.
- Monitor pipeline execution in Jenkins.
- Access SonarQube for code quality reports and Argo CD for deployment status.

### Conclusion
This CI/CD pipeline enhances development efficiency by automating build, test, and deployment stages. Integrating GitHub, Jenkins, SonarQube, Docker, Argo CD, and Kubernetes facilitates faster and more reliable software delivery.

---

Feel free to modify or expand on this README to include specific configurations or additional notes related to the project.
