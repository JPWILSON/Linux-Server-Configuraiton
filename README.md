# Linux-Server-Configuraiton
The following is an overview of one possible procedure for the deployment of a flask web application onto a baseline Ubuntu OS, hosted on Amazon Lightsail. A [sample application](http://ec2-54-157-225-246.compute-1.amazonaws.com) is hosted online for the time being, but I may take it off to avoid the monthly 
Amazon lightsail costs. (Sorry, its not pretty, it was just demonstrating CRUD functionality on Flask). 


## Project Access Details
1. IP Adress: **54.157.225.246**,  Port: 2200
2. Complete url: [http://ec2-54-157-225-246.compute-1.amazonaws.com](http://ec2-54-157-225-246.compute-1.amazonaws.com)

## Project Overview
**Configuration Changes**
- The ssh port was changed from 22 to 2200. 
- Password authentication was disabled, securing the server by only allowing key based authentication. 
- A firewall was setup.
- A user named 'grader' with sudo permission was created. 
- A user named catalog was created for the purpose of connecting to the postgresql database. 
- The timezone was changed.
- A [flask application](https://github.com/JPWILSON/ActivityTracker "Link to flask app: Activity Tracker") was imported and configured to run on a postgresql database (named catalog). 
- Note: The above project was isolated from its the rest of the Ubuntu OS by means of 'virtualenv'.

**Software Installed**
- Postgresql
- Flask Micro Web App Framework
- My [Activity Tracker](https://github.com/JPWILSON/ActivityTracker)
- Git was installed, in order to clone my repo

## Resources
I made use of [stackoverflow](http://stackoverflow.com/) and various online forum threads for assistance and insight. 
In **general**, topics (too many links to include) where the forums were useful included: 
- 'tail' for troubleshooting with apache2 logs 
- chaging the path on client_secrets.json
- installing packages outside of the virtual environment
- changing from sqlite to postgresql (username, password, database all named the same)

In **particular**, the following were useful: 
- The following Digital Ocean Posts: 
  * [Deploying a flash App on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps "How To Deploy a Flask Application on an Ubuntu VPS")
  * [PostgresSQL on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04"How To Install and Use PostgreSQL on Ubuntu 16.04")
- [This](http://sageelliott.com/post/post2-AWS-Flask_setup/ "AWS configuration for flask") post by Sage Elliot




