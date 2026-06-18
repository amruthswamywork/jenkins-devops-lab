

Prerequisite
Hardware recommendations-
The system needs an Ubuntu 20.04 server configured. Hardware recommendations for Jenkins, suggests the comprehensive hardware needed for Jenkins installations.

Minimum hardware requirements:

256 MB of RAM
1 GB of drive space (although 10 GB is a recommended minimum if running Jenkins as a Docker container)
Recommended hardware configuration for a small team:

4GB of RAM
50 GB of drive space
Install Java
The only prerequisite for Jenkins installation in Ubuntu 20.04 is Java, as Jenkins is a self-contained Java-based programme. It is recommended to use versions that do not predate Java 8. The most recommended versions are 8, 11, and 17. In this tutorial, steps to install Java 17 will be given. The steps to install JDK on Ubuntu are as follows:

sudo apt-get update

1. Install Java 17:
sudo apt-get install openjdk-17-jdk -y 

2. Verify the installation:
java -version

3.Install Git
sudo apt-get install git -y

4. Git version check:
git --version

5. Install Maven
sudo apt-get install maven -y

6. Verify Maven installation:
maven -version

7. Install Jenkins
To install Jenkins on Ubuntu 20.04, follow these steps:
a.wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo apt-key add -
b. sudo apt-get install jenkins -y
c.Jenkins -version
 
8.Start Jenkins service:
sudo systemctl status jenkin
sudo systemctl start jenkins

sudo ufw allow 8080 : http://localhost:8080

9. Access Jenkins
sudo cat /var/jenkins_home/secrets/initialAdminPassword

Now Good to go! You can access Jenkins by navigating to http://localhost:8080 in your web browser. Use the initial admin password obtained from the previous step to log in and start configuring Jenkins for your projects.

create a new user and set up your Jenkins environment according to your project requirements.

Fallow the steps in the above sections to set up your Jenkins environment and start automating your CI/CD pipelines.