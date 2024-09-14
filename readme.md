
# docker.io installations commands
```
sudo apt-get update
sudo apt-get install docker.io -y
sudo usermod -aG docker $USER
sudo systemctl start docker
sudo systemctl enable docker
```

- Permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/json": dial unix /var/run/docker.sock: connect: permission denied

### If you have face these types of issues, then use the below commands 
``` 
sudo chmod 777 /var/run/docker.sock 
```


### install Aws cli
```
#!/bin/bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
sudo apt-get install unzip -y
unzip awscliv2.zip
sudo ./aws/install
aws --version
```


# List of basic Docker commands that you can use to manage Docker images and containers, using an Nginx image as an example:


### **Docker Commands for Managing Images**

1. **Pull an Image**
   ```bash
   docker pull nginx
   ```
   *Downloads the latest Nginx image from Docker Hub.*

2. **List Images**
   ```bash
   docker images
   ```
   *Shows a list of all images on your local machine.*

3. **Remove an Image**
   ```bash
   docker rmi nginx
   ```
   *Removes the Nginx image from your local machine.*

4. **Build an Image**
   ```bash
   docker build -t my-nginx-image .
   ```
   *Builds a Docker image from a Dockerfile in the current directory, tagging it as `my-nginx-image`.*

5. **Tag an Image**
   ```bash
   docker tag my-nginx-image myrepo/my-nginx-image:latest
   ```
   *Tags `my-nginx-image` with `myrepo/my-nginx-image:latest` for pushing to a repository.*

6. **Push an Image**
   ```bash
   docker push myrepo/my-nginx-image:latest
   ```
   *Pushes the tagged image to a Docker repository (e.g., Docker Hub, AWS ECR).*

### **Docker Commands for Managing Containers**

1. **Run a Container**
   ```bash
   docker run -d -p 8080:80 --name my-nginx-container nginx
   ```
   *Starts a new container from the Nginx image, mapping port 80 in the container to port 8080 on the host, and names the container `my-nginx-container`.*

2. **List Running Containers**
   ```bash
   docker ps
   ```
   *Shows a list of currently running containers.*

3. **List All Containers**
   ```bash
   docker ps -a
   ```
   *Shows a list of all containers, including stopped ones.*

4. **Stop a Container**
   ```bash
   docker stop my-nginx-container
   ```
   *Stops the running container named `my-nginx-container`.*

5. **Remove a Container**
   ```bash
   docker rm my-nginx-container
   ```
   *Removes the stopped container named `my-nginx-container`.*

6. **Restart a Container**
   ```bash
   docker restart my-nginx-container
   ```
   *Restarts the container named `my-nginx-container`.*

7. **View Container Logs**
   ```bash
   docker logs my-nginx-container
   ```
   *Displays logs from the container named `my-nginx-container`.*

8. **Execute a Command in a Running Container**
   ```bash
   docker exec -it my-nginx-container /bin/bash
   ```
   *Executes a bash shell in the running container named `my-nginx-container`. You can also use `/bin/sh` for simpler containers.*

9. **Inspect a Container**
   ```bash
   docker inspect my-nginx-container
   ```
   *Displays detailed information about the container named `my-nginx-container`.*

10. **Remove All Stopped Containers**
    ```bash
    docker container prune
    ```
    *Removes all stopped containers.*

### **General Docker Commands**

1. **System Information**
   ```bash
   docker info
   ```
   *Shows system-wide information about Docker.*

2. **Clean Up Unused Data**
   ```bash
   docker system prune
   ```
   *Removes unused data, including stopped containers, unused networks, and dangling images.*

3. **Search for Images**
   ```bash
   docker search nginx
   ```
   *Searches Docker Hub for images related to `nginx`.*

4. **Login to Docker Hub**
   ```bash
   docker login
   ```
   *Logs into Docker Hub or other Docker registries.*

5. **Logout from Docker Hub**
   ```bash
   docker logout
   ```
   *Logs out from Docker Hub or other Docker registries.*

6. **Show Docker Version**
   ```bash
   docker --version
   ```
   *Displays the Docker version installed on your system.*

These commands cover the essentials for working with Docker images and containers, managing Docker resources, and interacting with Docker registries.