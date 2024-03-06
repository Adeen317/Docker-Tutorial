# Docker Environment Setup

This repository provides a simple guide and commands for setting up and managing Ubuntu environments using Docker.

## Getting Started

To run Ubuntu in your system using Docker, follow the steps below:

1. Ensure Docker is installed on your system. If not, please refer to the official Docker documentation for installation instructions.

2. Run the following command in your terminal:

```bash
docker run -it ubuntu
```

Explanation of options used:
- `-it`: Connects the container to your terminal and keeps it attached, allowing you to interact with it.

## Docker Basics

### Docker Hub

Docker Hub is a repository similar to GitHub but for containers. It hosts a vast collection of Docker images that you can use to build your applications.

### Images vs Containers

- **Images**: Similar to an operating system, images are the blueprints used to create containers. They contain all the necessary files and configurations.
- **Containers**: Instances of images running as isolated processes on the host operating system.

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

## Conclusion

This repository aims to provide a basic understanding of setting up and managing Ubuntu environments using Docker. For more advanced usage and customization, please refer to the Docker documentation and community resources.