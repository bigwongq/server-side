# Development for Docker Apps

> ### Docker
*  Docker is an open-source platform for building, deploying, and 
managing containerized applications.

>### After installation ~ Commonly Used Docker Commands

| Docker Command                                | Description                                             |
|-----------------------------------------------|---------------------------------------------------------|
| `docker --version`                            | Find the installed docker version                       |
| `docker pull <image>`                         | Pull the docker image from dockerhub (docker repository)|
| `docker build -t "<your-docker-id>/<image>" .`| Create your image                                       |
| `docker images`                               | List all the docker images on the system                |
| `docker run --env <image>`                    | Run the docker image and create a docker container      |
| `docker ps -a`                                | List all the docker containers running/exited/stopped   |
| `docker stop <container_id/name>`             | Stop a container                                        |
| `docker restart <container_id/name>`          | Restart the docker container                            |
| `docker rm -f <container_id/name>`            | Remove the docker container by force                    |
| `docker rmi <image_id/name>`                  | Remove the docker image                                 |
| `docker login`                                | Login into docker hub                                   |
| `docker push your-docker-id/<image>`          | Upload a docker image on the dockerhub                  |
| `docker logout`                               | Logging out from dockerhub                              |

>### 1 and 2. DockerFile Commands

| **Command**           | **Description**                                           |
|-----------------------|-----------------------------------------------------------|
| `FROM`                | Specify the base image for your container.                |
|                       | E.g., using the node base image with the desired version:  |
|                       | `FROM node:<version>-alpine`                              |
| `COPY`                | Copy files and directories from the host system into the container image. |
|                       | E.g., copying `server.js` into the container:             |
|                       | `COPY server.js /`                                        |
| `RUN`                 | Execute shell commands during the image build process.    |
|                       | E.g., using npm to install the express module:            |
|                       | `RUN npm install express`                                 |
| `EXPOSE`              | Declare the ports on which the container listens for incoming connections (for documentation purposes). |
|                       | E.g., `EXPOSE 8099`                                       |
| `ENTRYPOINT`          | Define an executable that always runs, making it harder to override. |
|                       | E.g., `ENTRYPOINT ["node"]`                               |
| `CMD`                 | Specify the default command to run when a container is started. Override it by providing a command when running the container. |
|                       | E.g., `CMD ["server.js"]`                                 |

>### 3. Build the image
  `docker build -t <your-image-name> .`
 * <your-image-name> is the name you want to give the image.

 * `.` denotes the current directory.


>### 4. Run the container
`docker run -d -p 8080:80 nginx` 
- **`docker run`**: Start and run a new container.
- **`-d`**: Run the container in the background (detached mode).
- **`-p 8080:80`**: Map port 8080 on the host to port 80 in the container.
  - **Host Port**: 8080
  - **Container Port**: 80
- **`nginx`**: Use the Docker image named `nginx` to create the container.

>### 5. Testing

>### 6. Push the image to Docker Hub


>### 7. Clear the local image and container
`docker ps -a`

`docker rm -f <your container ID>`

`docker ps -a`

`docker images`

`docker rmi <your image ID>`

`docker images`

>### Appendix I: Useful Commands

1.  ### Clean Ubuntu
 `df-h`  
 
 `sudo apt autoremove--purge snapd`

2.  ### Docker Install
 `sudo apt install docker-compose`  

 `sudo docker images`  

 `sudo docker ps-a`  

 `docker stop container_name`


 3. ### Docker Images remove
 `docker system prune -a`