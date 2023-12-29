# Spring Boot Based Java Web Application
 
This is a simple Sprint Boot based Java application that can be built using Maven. Sprint Boot dependencies are handled using the pom.xml 
at the root directory of the repository.

This is a MVC architecture based application where controller returns a page with title and message attributes to the view.

## Execute the application locally and access it using your browser
## Let's Do It.

## Step-1 : Create an EC2 Instance. 

Change hostname(Optional):
```
sudo hostnamectl set-hostname Jenkins
sudo systemctl reboot
```
## Step-2 : Let's install JAVA and MAVEN
Update the package index with the following Linux command:
```
sudo apt-get update -y
```
Install OpenJDK:
```
sudo apt install default-jdk -y
```
Verify the installation by running the following command:
```
java -version
```
Install Maven using the command below:
```
sudo apt-get -y install maven
```
Verify the Maven by running the following command:
```
mvn -version
```

## Step-3 : Checkout the repo and move to the directory

```
git clone https://github.com/Pradyumna018/Spring-Boot-Based-Java-Web-Application.git
```
```
cd Spring-Boot-Based-Java-Web-Application
```

## Step-4 : Execute the Maven targets to generate the artifacts

```
mvn clean package
```

The above maven target stroes the artifacts to the `target` directory. You can either execute the artifact on your EC2 Server
(or) run it as a Docker container.


## Step-5 : Execute on server and access the application on http://<public-ip>:8080

```
java -jar target/spring-boot-web.jar
```
## Step-6 : Install docker
```
sudo apt-get update -y
sudo apt  install docker.io -y
```
Add your user to the docker group.
```
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```
## Step-7 : Build the Docker Image

```
docker build -t maven:v1 .
```
## Step-8 : Run the Docker Container
```
docker run -d -p 8010:8080 -t maven:v1
```

Hurray !! Access the application on `http://<ip-address>:8010`

# Thank You ❤️



