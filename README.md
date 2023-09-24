HelloWorld Servlet example with corresponding Dockerfile

Use Maven Build first to create war file in Target folder.

mvn clean package

Artifact will be created in target folder.

docker build -t mavenbuild .

Once this is done u will be see image using docker image

Use below command to run the container

docker run -d -p 8080:8080 --name dockercontainer mavenbuild


#### Steps
Create Jenkins Pipeline to Deploy JAVA Application on Tomcat Server
===================================================================
https://www.youtube.com/watch?v=UIAO-9oYt0k

https://github.com/ravir1981/MavenBuild

Amazon Ubuntu - Enable port 8080
sudo apt update
apt install default-jdk

#### Install Jenkins Plugin

Manage Jenkins -> Plugins -> Available -> Deploy to Container

#### Install Tomcat on Ubuntu - Runs in 8080 port
apt install tomcat9 tomcat9-admin
ls -ltr /etc/tomcat9

#### How to access tomcat
<public-ip>:8080

### Edit tomcat-user.xml

https://docs.google.com/document/d/1-PcMo9M0gFWEMW7xKQdTumAuSIlSnKU9F1zkDjKMBq0/edit
Enable user

### Enable tomcat credential in Jenkins
Manage Jenkins -> credential -> Add Credential -> user/pass -> OK

### Now configure Pipeline
Pipeline
Enable git -> Pipeline script from SCM
