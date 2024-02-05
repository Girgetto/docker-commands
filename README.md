# Useful Docker Commands

This README provides a collection of useful Docker commands for managing containers, images, volumes, and networks. These commands are essential for Docker users of all levels.

## Container Management

- **List all running containers**
  ```
  docker ps
  ```

- **List all containers (running and stopped)**
  ```
  docker ps -a
  ```

- **Start a container**
  ```
  docker start <container_id_or_name>
  ```

- **Stop a container**
  ```
  docker stop <container_id_or_name>
  ```

- **Remove a container**
  ```
  docker rm <container_id_or_name>
  ```
  Use `-f` to force removal of running containers.

- **Execute a command in a running container**
  ```
  docker exec -it <container_id_or_name> <command>
  ```
  For example, to open a bash shell: `docker exec -it <container_id_or_name> bash`

## Image Management

- **List all images**
  ```
  docker images
  ```

- **Pull an image from a registry**
  ```
  docker pull <image_name>
  ```

- **Build an image from a Dockerfile**
  ```
  docker build -t <tag_name> .
  ```
  `-t` allows you to tag your image with a name and optionally a tag in the 'name:tag' format.

- **Remove an image**
  ```
  docker rmi <image_id_or_name>
  ```

## Volume Management

- **List all volumes**
  ```
  docker volume ls
  ```

- **Create a volume**
  ```
  docker volume create <volume_name>
  ```

- **Remove a volume**
  ```
  docker volume rm <volume_name>
  ```

## Network Management

- **List all networks**
  ```
  docker network ls
  ```

- **Create a network**
  ```
  docker network create <network_name>
  ```

- **Remove a network**
  ```
  docker network rm <network_name>
  ```

## Docker Compose

- **Start services defined in a docker-compose.yml**
  ```
  docker-compose up
  ```
  Use `-d` to run in detached mode.

- **Stop services started with docker-compose**
  ```
  docker-compose down
  ```

## Cleaning Up

- **Remove all stopped containers, all dangling images, and all unused networks**
  ```
  docker system prune
  ```
  Add `-a` to also remove all unused images, not just dangling ones.

- **Remove all unused volumes**
  ```
  docker volume prune
  ```

Feel free to modify and expand this README as per your project requirements.
