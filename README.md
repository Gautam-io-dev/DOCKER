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

STEP 1 - INSTALLING DOCKER

The Docker installation package available in the official Ubuntu repository may not be the latest version. To ensure we get the latest version, we’ll install Docker from the official Docker repository. To do that, we’ll add a new package source, add the GPG key from Docker to ensure the downloads are valid, and then install the package.

First, update your existing list of packages:

    sudo apt update

Next, install a few prerequisite packages which let apt use packages over HTTPS:

    sudo apt install apt-transport-https ca-certificates curl software-properties-common

Then add the GPG key for the official Docker repository to your system:

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

Add the Docker repository to APT sources:

    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"

This will also update our package database with the Docker packages from the newly added repo.

Make sure you are about to install from the Docker repo instead of the default Ubuntu repo:

    apt-cache policy docker-ce

You’ll see output like this, although the version number for Docker may be different:


    


    
    

    


    
    



    
