# DockerContainersSetup

This project simplifies the process of setting up various development and service containers using Docker. It saves time, minimizes errors, and ensures a repeatable environment configuration.

## Usage

### Starting Containers

To start all configured containers in detached mode:

  docker-compose up -d

To view container logs:

  docker-compose logs -f

### Stopping Containers

Stop the running containers:

  docker-compose down

### Rebuilding Containers

If you make changes to Dockerfiles or configuration files:

  docker-compose up --build
