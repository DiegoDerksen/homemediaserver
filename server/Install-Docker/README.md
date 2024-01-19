
## What are we installing?
* Docker
* Docker-Compose
  
## Prerequisites
Linux Server/desktop running Ubuntu 22.04 LTS or newer
*For installing Docker on other Linux distriubtions or different versions than Ubuntu 20.04 LTS, follow the [official installation instructions](https://docs.docker.com/install/).*

## Install Docker, and Docker-Compose

You can still install Docker on a Linux Server that is not running Ubuntu, this does require different commands.

### Install Docker
```
sudo apt update

sudo apt install apt-transport-https ca-certificates curl gnupg-agent software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

sudo apt update

sudo apt-get install docker-ce docker-ce-cli containerd.io
```

### Check if Docker is installed correctly
```
sudo docker run hello-world
```

### Install Docker-Compose

Download the latest version

```
 sudo apt-get install docker-compose-plugin
```

### Check if Docker-Compose is installed correctly
```
sudo docker-compose --version
```

### Add your linux user to the `docker` group
```
sudo usermod -aG docker $USER
```
### Update group memberships
```
newgrp docker
```
