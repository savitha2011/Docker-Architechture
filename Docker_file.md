## 📌 Docker Architecture Diagram

../Docker-Architecture/docker_archi.png.png)

---

## 🔹 Overview

Docker is a platform that enables developers to build, ship, and run applications inside lightweight containers. The image above illustrates the interaction between the **Client**, **Docker Host**, and **Registry**.

---

## 🔸 Components

### 1. **Client**
The Docker client is the interface used to interact with Docker. You typically run commands from your terminal like:

- `docker run` – Runs a container from an image.
- `docker build` – Builds a new image from a Dockerfile.
- `docker pull` – Downloads images from a registry.

These commands are sent to the **Docker Daemon**.

---

### 2. **Docker Host**
This is the environment where Docker is installed. It contains:

#### 🛠 Docker Daemon
- The background service that does all the heavy lifting.
- It listens to Docker client requests and manages containers, images, networks, and storage.

#### 🖼 Images
- These are read-only templates used to create containers.
- Examples shown: Python, Redis, and Alpine-based custom image.

#### 📦 Containers
- Containers are running instances of images.
- They are isolated environments that package application code and dependencies.

---

### 3. **Registry**
A Docker registry is a storage and content delivery system for Docker images.

#### 🔹 Images
- Examples shown: NGINX, Ubuntu, PostgreSQL, and a custom app.
- You can pull these images using `docker pull`.

#### 🔹 Extensions
- Third-party integrations such as JFrog, Docker Desktop GUI, etc.

#### 🔹 Plugins
- Additional tools like Grafana, Portainer, etc. for monitoring and management.

---

## 🔄 Workflow Summary

1. **Build**: Use `docker build` to create a custom image → stored in local image cache.
2. **Pull**: Use `docker pull` to download images from the registry to the host.
3. **Run**: Use `docker run` to start a container from an image → container runs on Docker Host.
4. **Image Source**: If the image isn’t on the host, it is pulled from the Registry.

---
