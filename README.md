# JFrogArtifactory


https://www.devopsschool.com/blog/artifactory-install-and-configurations-guide/

#### Artifactory OSS Install in Ubuntu


Step-1: Create an EC2 instance with Ubuntu AMI type t2.xlarge (minimum requirements are 4 cps and 4 GB RAM to install artifactory)

Step-2: Connect to EC2 instance and run below commands

    sudo -i
    
    apt update -y && apt install wget -y
    
    wget https://releases.jfrog.io/artifactory/bintray-artifactory/org/artifactory/oss/jfrog-artifactory-oss/7.21.5/jfrog-artifactory-oss-7.21.5-linux.tar.gz
    
    tar -xf jfrog-artifactory-oss-7.21.5-linux.tar.gz
    
    cd artifactory-oss-7.21.5/
    
    cd app/bin
    
    ./artifactory.sh start
    
    Access the URL: http://publicIPAddress:8082/
    
    # Username/Password - admin/password
    
#### Artifactory OSS Install in Ubuntu using Docker

    docker run -p 8081:8081 -p 8082:8082 -d releases-docker.jfrog.io/jfrog/artifactory-oss:latest

    Access the URL: http://publicIPAddress:8082/
    
    # Username/Password - admin/password
    
    
