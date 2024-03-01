# Simple-Python-Web-Application
Simple Python Web Application
# Jenkins-CI-CD-pipeline-for-flask-application
Jenkins CI CD pipeline for flask application

1. Setup:
Step 1: Install Jenkins on Ubuntu Linux VM
1. Launch your Ubuntu Linux virtual machine.
2. Open a terminal window.
3. Add the Jenkins repository key to the system using the following command:

wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -

4. Add the Jenkins repository to the system's sources list with the command:

sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'

5. Update the package index using: sudo apt update

6. Install Jenkins by running: sudo apt install jenkins

7. Start the Jenkins service: sudo systemctl start jenkins

8. Enable Jenkins to start on boot: sudo systemctl enable jenkins: sudo systemctl enable jenkins

Step 2: Configure Jenkins with Python and Libraries  

Open a web browser and navigate to http://localhost:8080 (replace localhost with the IP address of your virtual machine if accessing remotely).
Follow the on-screen instructions to complete the Jenkins setup wizard, including setting up an admin user and installing recommended plugins.
Once Jenkins is set up, navigate to Manage Jenkins > Manage Plugins > Available tab.
Search and install plugins related to Python and any necessary libraries, such as "Python Plugin" and any other plugins required for your project.
Navigate to Manage Jenkins > Global Tool Configuration and configure Python installations with the necessary libraries.


2. Source Code:

Step 1: Fork Repository
Go to the provided Python web application repository on GitHub.
Click on the "Fork" button to create a copy in your GitHub account.

Step 2: Clone Repository into Jenkins
SSH into your Ubuntu Linux virtual machine.
Clone the forked repository using Git.

git clone https://github.com/kaverigojre/Simple-Python-Web-Application.git

3. Jenkins Pipeline:
Step 1: Create Jenkinsfile
In the root directory of your Python application repository (GitHub Repository), create a file named Jenkinsfile.
This file will define the stages and steps of your Jenkins pipeline.
Step 2: Define Pipeline Stages
Open the Jenkinsfile in a text editor.
Define your pipeline stages using the Jenkins Pipeline syntax.

In this Jenkinsfile:

The Build stage installs dependencies using pip.

The Test stage runs unit tests using pytest.

The Deploy stage is a placeholder for deploying the application to a staging environment. You'll need to replace the placeholder with your deployment steps.

The post section defines actions to be taken after the pipeline completes, either successfully or with a failure.

Step 3: Commit and Push
Save the Jenkinsfile in your repository.
Commit the changes and push them to your GitHub repository.

Step 4: Configure Jenkins
Open your Jenkins dashboard.
Create a new pipeline job.
Link the job to your GitHub repository.
Configure Jenkins to use the Jenkinsfile from your repository.

Step 5: Run Pipeline
Trigger the pipeline manually or configure it to run automatically when changes are pushed to the repository.
Jenkins will execute the pipeline, following the defined stages and steps.

5. Notifications:

Install Email Extension Plugin:

Go to Jenkins dashboard.
Click on "Manage Jenkins" > "Manage Plugins".
Navigate to the "Available" tab and search for "Email Extension Plugin".
Install the plugin and restart Jenkins if required.
Configure Email Notifications:

Go to Jenkins dashboard.
Click on "Manage Jenkins" > "Configure System".
Scroll down to the "E-mail Notification" section.
Configure the SMTP server details (e.g., SMTP server, port, credentials, etc.).
Save the changes.
Update Your Jenkinsfile:

Add post-build actions to send email notifications when the build succeeds or fails.





To implement a CI/CD workflow using GitHub Actions for a Python application, follow these steps:

1. Setup:
Use the provided Python application repository on GitHub: Sample Python Application Repository.
Ensure the repository has a main branch and a staging branch.
2. GitHub Actions Workflow:
Create a .github/workflows directory in your repository.
Inside the directory, create a YAML file (e.g., ci_cd_workflow.yml) to define the workflow.
3. Workflow Steps.
4. Environment Secrets:
Use GitHub Secrets to store sensitive information required for deployments, such as deployment keys and API tokens.
5. Documentation:
Update the README.md file with instructions on how the GitHub Actions workflow works and how to configure the necessary secrets.
6. Submission:
Provide the URL to the GitHub repository with the workflow file (ci_cd_workflow.yml) and the updated README.md.

