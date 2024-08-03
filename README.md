# Docker
Docker and Swarm commands

Here is a comprehensive list of Docker and Docker Swarm CLI commands, including both basic and advanced commands, as well as commands specific to Docker Swarm.

### **Docker CLI Commands**

#### **1. Basic Commands**

- **Check Docker version:**
  ```bash
  docker --version
  ```

- **Show Docker info:**
  ```bash
  docker info
  ```

- **List Docker images:**
  ```bash
  docker images
  ```

- **Pull an image from a registry:**
  ```bash
  docker pull IMAGE_NAME
  ```

- **Remove an image:**
  ```bash
  docker rmi IMAGE_ID
  ```

- **List running containers:**
  ```bash
  docker ps
  ```

- **List all containers (including stopped):**
  ```bash
  docker ps -a
  ```

- **Start a container:**
  ```bash
  docker start CONTAINER_ID
  ```

- **Stop a container:**
  ```bash
  docker stop CONTAINER_ID
  ```

- **Restart a container:**
  ```bash
  docker restart CONTAINER_ID
  ```

- **Remove a container:**
  ```bash
  docker rm CONTAINER_ID
  ```

- **Run a new container:**
  ```bash
  docker run [OPTIONS] IMAGE_NAME
  ```

- **Execute a command in a running container:**
  ```bash
  docker exec -it CONTAINER_ID COMMAND
  ```

- **View container logs:**
  ```bash
  docker logs CONTAINER_ID
  ```

- **Build an image from a Dockerfile:**
  ```bash
  docker build -t IMAGE_NAME .
  ```

- **Tag an image:**
  ```bash
  docker tag IMAGE_ID REPOSITORY:TAG
  ```

- **Push an image to a registry:**
  ```bash
  docker push IMAGE_NAME
  ```

- **Inspect an image or container:**
  ```bash
  docker inspect IMAGE_ID
  ```

- **List Docker networks:**
  ```bash
  docker network ls
  ```

- **Create a new network:**
  ```bash
  docker network create NETWORK_NAME
  ```

- **Inspect a network:**
  ```bash
  docker network inspect NETWORK_NAME
  ```

- **Remove a network:**
  ```bash
  docker network rm NETWORK_NAME
  ```

- **List Docker volumes:**
  ```bash
  docker volume ls
  ```

- **Create a new volume:**
  ```bash
  docker volume create VOLUME_NAME
  ```

- **Inspect a volume:**
  ```bash
  docker volume inspect VOLUME_NAME
  ```

- **Remove a volume:**
  ```bash
  docker volume rm VOLUME_NAME
  ```

#### **2. Advanced Commands**

- **List all images, including intermediate layers:**
  ```bash
  docker images -a
  ```

- **Remove all stopped containers:**
  ```bash
  docker container prune
  ```

- **Remove all unused images:**
  ```bash
  docker image prune -a
  ```

- **Remove all unused networks:**
  ```bash
  docker network prune
  ```

- **Remove all unused volumes:**
  ```bash
  docker volume prune
  ```

- **View Docker system-wide disk usage:**
  ```bash
  docker system df
  ```

- **Clean up unused data:**
  ```bash
  docker system prune
  ```

- **Save an image to a tar file:**
  ```bash
  docker save -o IMAGE_FILE.tar IMAGE_NAME
  ```

- **Load an image from a tar file:**
  ```bash
  docker load -i IMAGE_FILE.tar
  ```

- **Export a container’s filesystem:**
  ```bash
  docker export CONTAINER_ID > CONTAINER.tar
  ```

- **Import a container’s filesystem:**
  ```bash
  docker import CONTAINER.tar
  ```

### **Docker Swarm CLI Commands**

#### **1. Basic Commands**

- **Initialize a Docker Swarm:**
  ```bash
  docker swarm init
  ```

- **Join a node to a Docker Swarm:**
  ```bash
  docker swarm join --token TOKEN SWARM_MANAGER_IP:PORT
  ```

- **Leave a Docker Swarm:**
  ```bash
  docker swarm leave
  ```

- **List nodes in the Swarm:**
  ```bash
  docker node ls
  ```

- **Inspect a node:**
  ```bash
  docker node inspect NODE_ID
  ```

- **Update a node’s availability:**
  ```bash
  docker node update --availability Availability NODE_ID
  ```

#### **2. Service Commands**

- **Create a new service:**
  ```bash
  docker service create [OPTIONS] IMAGE_NAME
  ```

- **List services:**
  ```bash
  docker service ls
  ```

- **Inspect a service:**
  ```bash
  docker service inspect SERVICE_ID
  ```

- **Update a service:**
  ```bash
  docker service update [OPTIONS] SERVICE_ID
  ```

- **Remove a service:**
  ```bash
  docker service rm SERVICE_ID
  ```

- **Scale a service:**
  ```bash
  docker service scale SERVICE_ID=NUM_REPLICAS
  ```

- **List tasks for a service:**
  ```bash
  docker service ps SERVICE_ID
  ```

#### **3. Stack Commands**

- **Deploy a stack from a Compose file:**
  ```bash
  docker stack deploy -c docker-compose.yml STACK_NAME
  ```

- **List stacks:**
  ```bash
  docker stack ls
  ```

- **Inspect a stack:**
  ```bash
  docker stack inspect STACK_NAME
  ```

- **Remove a stack:**
  ```bash
  docker stack rm STACK_NAME
  ```

- **List services in a stack:**
  ```bash
  docker stack services STACK_NAME
  ```

- **List tasks in a stack:**
  ```bash
  docker stack ps STACK_NAME
  ```

### **Summary**

This list provides a comprehensive set of Docker and Docker Swarm CLI commands for managing containers, images, networks, volumes, and services. It includes basic operations for daily use and advanced commands for more complex tasks and system maintenance.
