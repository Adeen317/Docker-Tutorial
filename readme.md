# Docker Environment Setup

This repository provides a simple guide and commands for setting up and managing Ubuntu environments using Docker.

## Getting Started

To run Ubuntu in your system using Docker, follow the command below:

```bash
docker run -it ubuntu
```

This command connects the container to your terminal and keeps it attached (`-it`), allowing you to interact with it.

## Docker Basics

### Docker Hub

Docker Hub is a repository similar to GitHub but for containers. It hosts a vast collection of Docker images that you can use to build your applications.

### Images vs Containers

- **Images**: Images are similar to operating systems and serve as blueprints for creating containers.
- **Containers**: Containers are instances of images running as isolated processes on the host operating system.

### Common Commands

Here are some common Docker commands to manage your containers and images:

1. **List Running Containers**: To view currently running containers, use the following command:
    ```bash
    docker container ls
    ```
    To include stopped containers, use:
    ```bash
    docker container ls -a
    ```

2. **Start Container**: To start a stopped container, execute:
    ```bash
    docker start 'container_file name'
    ```

3. **Stop Container**: To stop a running container, use:
    ```bash
    docker stop 'container_file name'
    ```

4. **Enter Container**: To enter an existing container, run:
    ```bash
    docker exec -it 'container_file_name' bash
    ```

5. **List Images**: To find the number of images on your system, run:
    ```bash
    docker images
    ```

### Port Mapping

Port mapping allows you to map ports between your local machine and the Docker container. For example:
```bash
docker run -it -p 1025:1025 image_name
```
This command maps port 1025 in the container to port 1025 on your local machine.

### Environment Variables

You can define environment variables for your Docker containers. For example:
```bash
docker run -it -e PORT=4000 -p 4000:4000 image_name
```
This command sets the `PORT` environment variable to `4000` and maps port `4000` in the container to port `4000` on your local machine.

## Creating Your Own Image and Container

To create your own Docker image and container, use the following command:

```bash
docker build -t python-world .
```

This command builds an image named `python-world` based on the `Dockerfile` in the current directory (`.`).

## Docker Compose

To build and run your Docker services defined in a `docker-compose.yml` file, use the following command:

```bash
docker-compose up --build
```

This command builds the Docker services specified in the `docker-compose.yml` file and starts them up.



## Conclusion

This repository aims to provide a basic understanding of setting up and managing Ubuntu environments using Docker. For more advanced usage and customization, please refer to the Docker documentation and community resources.
