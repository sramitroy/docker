
# Docker Commands and Explanations

This document contains useful Docker commands along with explanations to help you manage your Docker environment.

## 1. List Docker Images (Builds)

To view all Docker images on your system:
```bash
docker images
```
This will display the images along with their repository, tag, image ID, creation date, and size.

## 2. List Running Docker Containers

To list all currently running Docker containers:
```bash
docker ps
```
This will show the containers' ID, names, image, status, and ports.

## 3. List All Docker Containers (Running and Stopped)

To see all containers, including stopped ones:
```bash
docker ps -a
```
This shows all containers with their statuses and other details.

## 4. List Docker Volumes

To list all Docker volumes:
```bash
docker volume ls
```
This shows all volumes used by Docker containers.

## 5. List Docker Networks

To list all Docker networks:
```bash
docker network ls
```
This shows all networks created by Docker.

## 6. List Docker System Information

To get information about your Docker installation (e.g., version, containers, and more):
```bash
docker info
```
This will display general information about your Docker setup.

## 7. Remove Stopped Containers

To remove all stopped containers from your system:
```bash
docker container prune
```
This will remove any containers that are not running.

## 8. Remove Unused Images (Old Builds)

To remove all unused Docker images (images not associated with any containers):
```bash
docker image prune -a
```
This will remove all images that are not in use.

## 9. Remove Unused Volumes

To remove unused volumes:
```bash
docker volume prune
```
This will clean up volumes not used by any containers.

## 10. Remove Unused Networks

To remove unused Docker networks:
```bash
docker network prune
```
This removes networks that are not used by any containers.

## 11. Remove All Unused Docker Objects (Images, Containers, Volumes, Networks)

To remove all unused objects in your Docker setup:
```bash
docker system prune -a
```
This will clean up all unused containers, images, volumes, and networks.

## 12. Remove Specific Docker Container

To remove a specific container by its name or ID:
```bash
docker rm <container_id_or_name>
```
Replace `<container_id_or_name>` with the actual ID or name of the container.

## 13. Remove Specific Docker Image

To remove a specific Docker image:
```bash
docker rmi <image_id_or_name>
```
Replace `<image_id_or_name>` with the ID or name of the image you want to remove.

## 14. Remove Docker Network

To remove a specific Docker network:
```bash
docker network rm <network_name>
```
Replace `<network_name>` with the name of the network you want to remove.

## 15. Build Docker Image from Dockerfile

To build a Docker image from a `Dockerfile` in the current directory:
```bash
docker build -t <image_name>:<tag> .
```
Replace `<image_name>` with your preferred image name and `<tag>` with the version tag.

## 16. Run Docker Container from Image

To run a new container from a specific image:
```bash
docker run -d -p <host_port>:<container_port> --name <container_name> <image_name>:<tag>
```
- Replace `<host_port>` with the port you want to expose on your host.
- Replace `<container_port>` with the port the container exposes.
- Replace `<container_name>` with your container name.
- Replace `<image_name>:<tag>` with the image name and tag you want to run.

## 17. View Docker Container Logs

To view the logs of a specific container:
```bash
docker logs <container_name_or_id>
```
Replace `<container_name_or_id>` with the name or ID of the container whose logs you want to view.

## 18. Access Running Docker Container

To access a running Docker container and open an interactive shell:
```bash
docker exec -it <container_name_or_id> /bin/bash
```
This will give you access to the container's shell.

## 19. Stop a Running Docker Container

To stop a running container:
```bash
docker stop <container_name_or_id>
```
Replace `<container_name_or_id>` with the container name or ID.

## 20. Start a Stopped Docker Container

To start a previously stopped container:
```bash
docker start <container_name_or_id>
```
Replace `<container_name_or_id>` with the container name or ID.

## 21. Restart a Docker Container

To restart a running or stopped container:
```bash
docker restart <container_name_or_id>
```
This will restart the specified container.

## 22. Remove Docker Volume

To remove a specific Docker volume:
```bash
docker volume rm <volume_name>
```
Replace `<volume_name>` with the name of the volume you want to delete.

## 23. Remove Docker Image

To remove a specific Docker image:
```bash
docker rmi <image_id_or_name>
```
Replace `<image_id_or_name>` with the image ID or name of the image you wish to delete.

## 24. Remove All Docker Containers and Volumes

To remove all containers (running and stopped) and volumes:
```bash
docker system prune --volumes
```
This will remove all unused containers, images, networks, and volumes.

## 25. Clean Up Docker System (Remove Unused Containers, Images, and Networks)

To clean up the Docker system and remove unused objects:
```bash
docker system prune
```
This will remove all stopped containers, unused networks, and dangling images.

## 26. Run Docker Container with Specific Environment Variables

To run a container with environment variables:
```bash
docker run -d -p <host_port>:<container_port> -e VAR_NAME=value --name <container_name> <image_name>:<tag>
```
Replace `VAR_NAME=value` with the environment variables you want to set in the container.

---

### Note:
- Be cautious when using `docker system prune` and `docker system prune -a`, as these commands can remove many objects that are not in use.
- Always verify that containers, volumes, or networks are not in use before removing them.

---

By following these commands, you can efficiently manage Docker containers, images, volumes, and networks within your environment.
