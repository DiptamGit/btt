Certainly! Let's dive into the details of Docker and related technologies, covering each subtopic comprehensively.

### 1. What is Dockerfile and How to Use It?
**Dockerfile** is a text document that contains all the commands a user could call on the command line to assemble an image. Using `docker build` users can create an automated build that executes several command-line instructions in succession.

#### How to Use Dockerfile:
1. **Specify a Base Image**: Use the `FROM` command to define the base image you're starting from.
2. **Set Environment Variables**: The `ENV` command allows you to set environment variables.
3. **Run Commands**: The `RUN` command lets you execute commands needed for your application setup.
4. **Copy Files**: The `COPY` or `ADD` commands are used to copy files and directories into the container.
5. **Set Working Directory**: The `WORKDIR` command sets the working directory for any `RUN`, `CMD`, `ENTRYPOINT`, `COPY`, and `ADD` commands.
6. **Expose Ports**: Use the `EXPOSE` command to inform Docker that the container listens on specific network ports.
7. **Command on Start**: The `CMD` command provides defaults for executing a container.

### 2. What is Docker Swarm?
**Docker Swarm** is a container orchestration tool, meaning it allows the user to manage multiple containers deployed across multiple host machines. It's built into Docker as part of the standard Docker application and uses the Docker API as its primary user interface.

### 3. Swarm Services and States
In Docker Swarm, a **service** is the definition of the tasks to execute on the nodes. A service defines the container image, ports, and commands among other settings. Services are declared in a `docker-compose.yml` file or via Docker CLI.

#### Common Service States:
- **Running**: Service is active and running as expected.
- **Paused**: Service is temporarily stopped; can be resumed.
- **Stopped**: Service has been halted and needs to be restarted or removed.

### 4. Different Types of Docker Network and Their Usages
Docker provides several networking options:
- **Bridge Network**: Default network type for containers. Good for communicating between containers on the same host.
- **Host Network**: Removes network isolation between container and Docker host, and uses the host's networking directly.
- **Overlay Network**: Connects multiple Docker daemons together and enables swarm services to communicate with each other.
- **Macvlan Network**: Allows you to assign a MAC address to a container, making it appear as a physical device on your network.

### 5. Service Discovery in Docker Swarm
**Service discovery** in Docker Swarm involves the automatic assignment of addresses to the services in a cluster so that they can communicate with each other:
- **Embedded DNS**: Docker Daemon has an embedded DNS server which provides service discovery for containers.
- **Routing Mesh**: Enables containers to communicate across a cluster via internal load balancing.

### 6. External Load Balancing in Docker Swarm
In Docker Swarm, **external load balancing** can be handled by:
- **Publishing Ports**: Configuring specific ports in services that external load balancers can access.
- **Using External Load Balancers**: Placing a third-party load balancer like HAProxy or Nginx in front of the swarm cluster.

### 7. Three Ways to Map Host to Container
1. **Port Mapping**: Using the `-p` or `--publish` option to map a host port to a container port.
2. **Volume Mapping**: Using the `-v` or `--volume` option to map a host directory to a container directory.
3. **Network Mapping**: Connecting a container to a host network with `--network host`.

### 8. Docker Compose and Its Usage
**Docker Compose** is a tool for defining and running multi-container Docker applications. You use a YAML file to configure your application's services, networks, and volumes, then use a single command (`docker-compose up`) to create and start all the services from your configuration.

#### Usage:
- **Development environments**: Easily setup and replicate complex applications.
- **Automated testing environments**: Quickly deploy and scale applications for testing.
- **Production deployments**: Manage the lifecycle of an entire stack efficiently.

This comprehensive coverage should give you a robust foundation in understanding and utilizing Docker's capabilities and functionalities.