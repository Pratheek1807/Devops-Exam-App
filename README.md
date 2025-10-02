												Steps For The Project
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

*********************************************
1. Launch Ubuntu 
*********************************************
Open below ports - 
Type: All TCP, Protocol: TCP, Port range: 0 - 65535*
Type: All ICMP - IPv4, Protocol: ICMP, Port range: All
Type: SSH, Protocol: TCP, Port range: 22*
Type: Custom TCP, Protocol: TCP, Port range: 3000*
Type: Custom TCP, Protocol: TCP, Port range: 8081
Type: Custom TCP, Protocol: TCP, Port range: 8080*
Type: HTTPS, Protocol: TCP, Port range: 443*
Type: Custom TCP, Protocol: TCP, Port range: 6443
Type: HTTP, Protocol: TCP, Port range: 80*

************************************
2. Connect to VM
************************************
sudo su
sudo apt update

************************************
3. Installation of Jenkins
************************************
 jenkins --version ----> Setup the Jenkins Dashboard

************************************
4. Installation of Docker
************************************
vi docker.sh ---->docker --version


************************************
5. Installation of Trivy
************************************
vi trivy.sh ---->  trivy --version

************************************
6. Installation of Docker Scout
************************************
Make sure to Login to DockerHub account in browser

************************************
7. Installation of SonarQube
************************************
docker run -d --name sonar -p 9000:9000 sonarqube:latest

Access SonarQube, after opening port 9000
Default username and Password: admin
Set new password

************************************
8. Jenkins Plugin Installation
************************************
Install below plugins;
SonarQube scanner, Docker, Docker Commons, Docker Pipeline, Docker API, docker-build-step, Pipeline stage view 
Here we need to restart the Jenkins 

************************************
9. Tools Configuration in Jenkins
************************************
Goto the Jenkins console (since we restarted, login again to Jenkins) ---> Manage Jenkins ---> System Configuration ---> Tools ---> SonarQube Scanner Installations ---> ,  Docker Installations ---> Add Docker---> , Version: latest ---> Apply ---> Save

************************************
10. Docker Hub Credentials Configuration
************************************
10.1. Docker hub Credentials Configuration
This is being done because, as soon as the docker image is created, it should get pushed to dockerhub. 
Goto the Jenkins console ---> Manage Jenkins ---> Security ---> Credentials ---> 
Create ---> You can see the docker credentials got created.


1. Accessing the MySQL Database
# Connect to MySQL container
docker exec -it mysql_db mysql -u root -p
# Enter password: rootpass when prompted

2. Common Database Operations
Once connected to MySQL:
-- Show all databases
SHOW DATABASES;

-- Use your application database
USE devops_exam;

-- Show all tables
SHOW TABLES;

-- View the structure of your results table
DESCRIBE results;

-- View all exam results
SELECT * FROM results;





