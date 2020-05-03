# -IIEC-RISE-Docker-Project-
JOOMLA  DEVELOPMENT ENVIRONMENT WITH  MSQL DATABASE


PROJECT OBJECTIVE
------------------
Confiruration of Joomla server and mySQL server on Docker containers and connecting between them.

PREREQUISITES:
-----------------

In order to complete the steps in this guide, you will need the following:

1. Root access to the OS.
2. YUM properly configured
3. Docker installed
4. MySQL image installed
5. PhpMyAdmin and Joomla images installed

STEPS:
-------

STEP 1: Prior to running the docker services, you are required to disable the firewall
and SELinux using the following command:
      systemctl stop firewalld

STEP 2: Disabling the SELinux:
       setenforce 0

STEP 3: Start docker services:
systemctl start docker

STEP 4: Pull the latest version of Joomla and phpmyadmin docker images from hub.docker.com
docker pull joomla:latest
docker pull phpmyadmin/phpmyadmin

STEP 5 Pull the latest version 5.7 of MySQL docker image from hub.docker.com
docker pull mysql:5.7

STEP 6: To see all docker images:
docker images

STEP 7: Create a directory named “joomla” in the root folder:
mkdir joomla

STEP 8: Create a file named “docker-compose.yml” inside the “joomla” directory.
cd joomla
vim docker-compose.yml

STEP 9: Enter the source code

STEP 10: Run the docker-compose file: docker-compose up

STEP 11: Inpect the Joomla container using its container ID:
docker inspect [CONTAINER ID]

STEP 12: Get the IP address of Joomla container.

STEP 13: Open the browser and browse with URL:
        10.10.100.20:8092

STEP 14: Proceed with the Joomla installation steps and finish configuring the website.







