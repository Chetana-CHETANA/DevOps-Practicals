# Practical 04: Installation of Jenkins and Building a Basic Jenkins Job

## 1. Aim
Install Jenkins, configure the Jenkins server, and create and run a basic Jenkins job.

## 2. Requirements
- Ubuntu Linux
- Java JDK 21
- Jenkins
- Internet Connection
- Web Browser

## 3. Theory
Jenkins is an open-source automation tool used for Continuous Integration and Continuous Delivery (CI/CD). It helps automate software building, testing and deployment through Jenkins jobs.

## 4. Procedure
Step 1: Update the Ubuntu package list.
Step 2: Install Java JDK 21 and required packages.
Step 3: Add the Jenkins repository key and repository.
Step 4: Install Jenkins.
Step 5: Start and enable the Jenkins service.
Step 6: Check the Jenkins service status.
Step 7: Open Jenkins in a web browser and unlock it using the initial admin password.
Step 8: Create a new Jenkins job.
Step 9: Select the Execute Shell build step and enter commands.
Step 10: Build the job and verify the console output.

## 5. Commands

**Install Java and required packages:**
```bash
sudo apt update
sudo apt install fontconfig openjdk-21-jre -y
```

**Add Jenkins repository:**
```bash
sudo mkdir -p /etc/apt/keyrings
sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc https://pkg.jenkins.io/debian-stable/jenkins.io-2026.key
echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/" | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
```

**Install and start Jenkins:**
```bash
sudo apt update
sudo apt install jenkins -y
sudo systemctl enable --now jenkins
sudo systemctl status jenkins
```

**Get initial admin password:**
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

**Commands inside Jenkins job (Execute Shell):**
```bash
echo "Jenkins Build Started"
echo "DevOps Practical"
```

## 6. Result
Successfully installed and configured Jenkins, created a basic Jenkins job, and executed it successfully.
