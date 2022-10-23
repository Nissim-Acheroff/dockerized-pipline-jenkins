# MULTISTAGE BUILD 
#### Docker container pipelines 

The application we are using as a POC can be downloaded from:  https://github.com/rmotr/flask-api-example

##### Running tests and validation in the applicaiton


We are going to build this application inside a docker container and run:
1. Code analysis
2. Unit tests
3. SonarQube for security check

order of execution 



docker create network nexus_nexus

docker run -d --network nexus_nexus --rm --name sonarqube -p 0.0.0.0:9000:9000 sonarqube 

In the browser change the password 

In the conf file of sonarqube add the correct password

docker build --network nexus_nexus -t server-image -f Dockerfile-pipelines .

Add the the DNS in etc/hosts 127.0.0.1.nip.io

Run the container server image docker run -it -p 8080:8080 server-image

Open browser at http://127.0.0.1.nip.io

