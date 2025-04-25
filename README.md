# mlops-zoomcamp

1. Introduction

## 1.1 Introduction

1.2 Environment preparation

1.2.1 GitHub Codespaces

## Code:

Recommended development environment: Linux

## Step 1: Download and install the Anaconda distribution of Python
wget https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh

bash Anaconda3-2022.05-Linux-x86_64.sh


## Step 2: Update existing packages
sudo apt update
## Step 3: Install Docker and Docker Compose
Follow the instructions here: install-using-the-repository

Set up Docker's apt repository.

# Add Docker's official GPG key:
sudo apt-get update

sudo apt-get install ca-certificates curl

sudo install -m 0755 -d /etc/apt/keyrings

sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc

sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \

  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \

  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update

## Install the Docker packages.

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

To run docker without sudo:

sudo groupadd docker
sudo usermod -aG docker $USER

## Step 4: Run Docker
docker run hello-world

