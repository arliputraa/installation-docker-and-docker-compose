# Installation Docker and Docker Compose on Ubuntu 20.04

## Install Docker

### Update the package index:

    sudo apt-get update
    
### Install packages to allow apt to use a repository over HTTPS:

    sudo apt-get install apt-transport-https ca-certificates curl software-properties-common

### Add Docker’s official GPG key:

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    
![image](https://user-images.githubusercontent.com/110078907/216588492-1a470d84-894d-4e8f-9ec8-bbf58d62b03d.png)

### Add the Docker repository to your system:

    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

### Update the package index again:

    sudo apt-get update
    
### Finally, install Docker:
    
    sudo apt-get install docker-ce

### Verify the installation by running a test Docker container:

    sudo docker run hello-world

![image](https://user-images.githubusercontent.com/110078907/216587959-6b3bad69-e0a2-43cd-99f5-3186c791ba50.png)


## Install Docker Compose

### Download Docker Compose using curl:
change (v2.15.1) for last version 

    sudo curl -L "https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-$(uname -s)-$(uname -m)"  -o /usr/local/bin/docker-compose
    
![image](https://user-images.githubusercontent.com/110078907/216591266-d2431df8-5539-4568-8e2e-c0d97533d330.png)

### Move directory

    sudo mv /usr/local/bin/docker-compose /usr/bin/docker-compose
    
### Apply executable permissions to the binary:

    sudo chmod +x /usr/bin/docker-compose

### Verify the installation by checking the version:

    docker-compose --version

![image](https://user-images.githubusercontent.com/110078907/216590437-fbff5454-b525-4fa7-baef-e7b4fc665dcd.png)

