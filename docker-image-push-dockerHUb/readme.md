
---- 
# Docker image, tagging, and pushing it to Docker Hub.

```markdown
# Flask Todo App

This is a simple Flask-based Todo application. This guide provides instructions for building the Docker image, tagging, and pushing it to Docker Hub.

## Prerequisites

Make sure you have the following installed:

- Docker
- Docker Hub account

## Getting Started

### 1. Clone the Repository

First, clone the Flask Todo App repository from GitHub:

```bash 
git clone https://github.com/nahidkishore/flask-todo-app.git
```
Navigate to the project directory:

```bash
cd flask-todo-app/
```

### 2. Build the Docker Image

To build the Docker image, use the following command. This will create a Docker image locally using the `Dockerfile` in the repository:

```bash
docker build -t flask-test-app .
```

### 3. Tag the Docker Image

After building the image, tag it with your Docker Hub username and repository name. Replace `nahid0002` with your Docker Hub username if different:

```bash
docker tag flask-test-app nahid0002/flask-test-app:latest
```

This will create a new tag for your Docker image.

### 4. Login to Docker Hub

If you're not logged in already, use the `docker login` command to log into Docker Hub. Enter your Docker Hub credentials when prompted:

```bash
docker login
```

### 5. Push the Docker Image to Docker Hub

After successfully tagging and logging in, push the Docker image to Docker Hub using the following command:

```bash
docker image push nahid0002/flask-test-app:latest
```

### 6. Verify the Image on Docker Hub

Once the push is complete, go to [Docker Hub](https://hub.docker.com/) and check your repository to verify that the image was successfully pushed.

## Additional Commands

Here is the history of the commands used:

```bash
git clone https://github.com/nahidkishore/flask-todo-app.git
cd flask-todo-app/
docker build -t flask-test-app .
docker tag flask-test-app nahid0002/flask-test-app:latest
docker login
docker image push nahid0002/flask-test-app:latest
```

## Conclusion

You now have your Flask Todo app containerized and pushed to Docker Hub. You can use this image to run containers locally or deploy it to any container platform.
```

### Additional Notes:

- Make sure to replace `nahid0002` with your actual Docker Hub username if different.
- You may want to add more sections for running the container locally or using it in a Kubernetes or Docker Compose environment.
