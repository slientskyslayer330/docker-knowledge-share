# Docker Basics

## Common Docker Commands

- `docker pull <image>`: Download an image from Docker Hub
- `docker images`: List all local Docker images
- `docker ps`: List running containers
- `docker ps -a`: List all containers (including stopped ones)
- `docker run <image>`: Create and start a container from an image
- `docker stop <container>`: Stop a running container
- `docker rm <container>`: Remove a stopped container
- `docker rmi <image>`: Remove a Docker image

Example usage:

# Pull the official Nginx image
`docker pull nginx`

# Run an Nginx container
`docker run -d -p 8080:80 --name my-nginx nginx`

# Stop the container
`docker stop my-nginx`

# Remove the container
`docker rm my-nginx`


## Building a Docker Image

1. Create a Dockerfile (see example in this repo)
2. Build the image:

`docker build -t my-node-app .`

3. Run the container


`docker run -d -p 3000:3000 --name my-node-container my-node-app`

4. Stop the container

`docker stop my-node-container`

5. Remove the container

`docker rm my-node-container`

## Running with Custom port

1. Run the container

`docker run -d -e PORT=8080 -p 8080:8080 --name my-node-container my-node-app`

2. Stop the container

`docker stop my-node-container`

3. Remove the container

`docker rm my-node-container`

## Using Docker Compose

Docker Compose makes it easy to define and run multi-container Docker applications.

1. Create a docker-compose.yml file (see example in this repo)
2. Start the application:

   `docker-compose up -d`

3. Stop the application:

    `docker-compose down`

