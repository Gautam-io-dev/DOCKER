# DOCKER
Docker is a platform that enables developers to create, deploy, and manage applications in lightweight containers. These containers package an application and all its dependencies, ensuring consistent 
performance across different environments. Docker uses images as templates for containers, which can be easily shared via Docker Hub. This technology simplifies development, enhances scalability, and
helps avoid compatibility issues,making it a popular choice for modern software development and deployment.

Key features of Docker include:

1. **Containerization**: Applications run in isolated environments, which makes them portable and easy to manage.

2. **Images and Dockerfile**: Docker uses images as blueprints for containers. A Dockerfile is a script that contains instructions to build an image.

3. **Docker Hub**: A cloud-based registry where users can share and distribute Docker images.

4. **Orchestration**: Tools like Docker Compose and Kubernetes can manage multi-container applications and services.

Overall, Docker streamlines development workflows, improves resource utilization, and enhances application deployment speed.

![image alt](https://github.com/Gautam-io-dev/DOCKER/blob/933ec1d3c498383ab0562ab77af30e263d2ff7c3/docker.png)

# CONTAINERS

Containers are lightweight, portable units that package an application and all its dependencies, including libraries, configuration files, and runtime. They run in isolation from one another on the same operating system kernel, which makes them more efficient than traditional virtual machines.

Key characteristics of containers include:

1. **Isolation**: Each container operates independently, ensuring that applications do not interfere with each other.
2. **Portability**: Containers can run consistently across different environments, from a developer's laptop to production servers.
3. **Efficiency**: Containers share the host OS kernel, reducing overhead and improving resource utilization compared to virtual machines.
4. **Scalability**: Containers can be easily scaled up or down to handle varying workloads.

Overall, containers facilitate rapid development, testing, and deployment of applications, making them a cornerstone of modern DevOps practices.

# NGINX

NGINX is a high-performance web server and reverse proxy server that is widely used for serving web applications, handling HTTP and HTTPS requests, and load balancing traffic. It is known for its speed, efficiency, and ability to handle a large number of concurrent connections with low resource usage.

![image alt](https://github.com/Gautam-io-dev/DOCKER/blob/a52bcc864f4ebad1c9bc86a09706b6df40b37c97/NGINX.jpg)

Key features of NGINX include:

1. **Web Server**: It can serve static content (like HTML, CSS, and images) quickly and efficiently.

2. **Reverse Proxy**: NGINX can act as an intermediary for requests from clients seeking resources from other servers, distributing the load and improving performance.

3. **Load Balancing**: It can distribute incoming traffic across multiple servers to ensure availability and reliability.

4. **SSL/TLS Termination**: NGINX can handle SSL/TLS encryption, improving security while offloading the processing from backend servers.

5. **Caching**: It can cache content to reduce latency and improve response times.

6. **Support for WebSockets**: NGINX supports real-time communication for applications that require persistent connections.

![image alt](https://github.com/Gautam-io-dev/DOCKER/blob/c766cefe31e958d1ff5596cd73402224802b6170/NGINX%20WORKING.webp)   

Overall, NGINX is popular for its flexibility and robustness, making it a go-to choice for many web applications and services.

# HOW TO INSTALL NGINX

In this tutorial, we’ll show you how to install NGINX on Linux. Open your Linux machine and run an update using the command below:

    sudo apt-get update
    
Next, run this command: 

    sudo apt-get install nginx
    
Then, enable your firewall with the following: 

    sudo ufw enable
    
To verify NGINX is installed, run the following:

    nginx -v
    
You can run the command below to find out if NGINX is running:

    sudo ufw status
    
After running this command, you should see the following:

    status: active
    
To check whether your NGINX server is working fine, run the following:

    sudo systemctl status nginx

# HOW TO INSTALL DOCKER

To install Docker on a remote server using PuTTY, you'll first need to ensure you have access to a Linux server (like Ubuntu, CentOS, etc.) via SSH. Here's a step-by-step guide:

### Step 1: Connect to Your Server

1. **Open PuTTY**.
2. **Enter the hostname or IP address** of your server.
3. **Click "Open"** to initiate the connection.
4. **Log in** with your username and password.

### Step 2: Update Your Package Index

Before installing Docker, it’s a good idea to update the package index:

```bash
sudo apt update
```

### Step 3: Install Prerequisites

For Ubuntu, install the required packages:

```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

For CentOS, run:

```bash
sudo yum install -y yum-utils
```

### Step 4: Add Docker’s Official GPG Key

For Ubuntu:

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

For CentOS:

```bash
sudo rpm --import https://download.docker.com/linux/centos/gpg
```

### Step 5: Set Up the Stable Repository

For Ubuntu:

```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

For CentOS:

```bash
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

### Step 6: Install Docker

For Ubuntu:

```bash
sudo apt update
sudo apt install docker-ce
```

For CentOS:

```bash
sudo yum install docker-ce
```

### Step 7: Start Docker

Enable and start the Docker service:

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

### Step 8: Verify the Installation

Check if Docker is running:

```bash
sudo systemctl status docker
```

You can also run a test container:

```bash
sudo docker run hello-world
```

### Step 9: (Optional) Manage Docker as a Non-Root User

If you want to run Docker commands without `sudo`, add your user to the Docker group:

```bash
sudo usermod -aG docker $USER
```

After running this command, log out and back in for the changes to take effect.

### Conclusion

You’ve successfully installed Docker using PuTTY! If you have any questions or run into issues, feel free to ask.
