
# Besu - Development Environment

In this repository it is included the Dockerfiles and the Docker Compose file to build and deploy two containers:
1) A container running Ganache-CLI
2) A container running Truffle Suite

First, make sure you have docker and docker-compose installed. Then, move into the current directory, and execute the following:
```
docker-compose up -d
```
The latter will build and execute the two containers mentioned above. By executing ```docker ps -a``` you should see the following: 

<p align="center"><img src="hhttps://github.com/UNIC-IFF/BLOC-522/blob/main/figures/docker-ps-a.PNG?raw=true"/></p>

For the smart contracts development etc, we need to attach ourselves in the truffle_suite container. We can do so by executing the following: ```docker exec -it truffle_suite /bin/bash```. If you are runnign windows execute the following instead:  ```winpty docker exec -it truffle_suite sh```. Then in the attached console you execute ```bash``` and we are ready to start writing our code.


Ganache can also be integrated within metamask. Follow the same instructions as in the parent repository and just replace the IP (localhost for local deployment) and the port to 5545.