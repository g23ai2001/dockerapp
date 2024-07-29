# VCC Assignment 1

# Gram to Kilogram Converter Web App

This is a simple web application that converts grams to kilograms. The app is built using basic HTML and JavaScript and is served using an Apache web server within a Docker container. The Docker image is created from scratch then ubuntu filemanagr have been installed on top of it using debootstrap. 

## Table of Contents

- [Description](#description)
- [Process Followed](#process-followed)


## Description

The Gram to Kilogram Converter web app allows users to input a value in grams and convert it to kilograms. This application is containerized using Docker, and an Apache web server is used to serve the static HTML content.

## Process Followed

### Step 1: Install `debootstrap` on your host system 
   ```bash
   sudo apt-get update
   sudo apt-get install -y debootstrap
```


### Step 2: Create the Minimal Ubuntu Filesystem
  ```bash
  mkdir -p ubuntu-base
  sudo debootstrap --variant=minbase jammy ubuntu-base/ http://archive.ubuntu.com/ubuntu/
```

### Step 3: Verify the directory creation:
  ```bash
  ls ubuntu-base
```

### Step 4: Create a tarball of the minimal Ubuntu filesystem:
  ```bash
  sudo tar -C ubuntu-base -cvf ubuntu-base.tar .
  gzip ubuntu-base.tar
```
  
### Step 5: Create HTML File, Dockerfile, docker compose file
 ```bash
    Refer to index.html,Dockerfile and docker-compose.yml
```
	
### Step 6: Build and Run the Docker Container
  ```bash
  docker-compose up --build
  Open your web browser and navigate to http://localhost.
```

# Steps to Download & Run the Project
```bash
  1. Download zip file from Master Branch of Repository. Recommended Host System is Ubuntu. Docker must be installed in Host OS
  2. Unip the project.
  3. Now change the dir to dockerapp-master.
  4. Open Terminal and run docker-compose up --build (use sudo if facing any permission issue).
  5. Open your web browser and Navigate to http://localhost:80
```
  
  
 ### Author
```bash
Roll Number: [G23AI2001]
```
 
