
Below is the GitHub-flavored Markdown content you can use to document the Docker commands for content management in a README file.

---

# Docker Commands for Content Management

Docker is a containerization platform that simplifies application deployment. This document covers the essential Docker commands for managing containers and images.\


## **1. Docker Pull**
Pull an image or a repository from a registry.

```bash
docker pull ubuntu:latest
```

```
docker images
```

- Downloads the `ubuntu:16.04` image from Docker Hub.


---

## **2. Docker Run**
Run a command in a new container.

```bash
docker run --name mycontainer -it ubuntu:latest /bin/bash
```
## if want see running containers

```
docker ps
```

### if want to see stoped container and ruuning container 

```
docker ps -a
```

- **`--name mycontainer`**: Names the container `mycontainer`.
- **`-it`**: Runs the container interactively.
- **`ubuntu:latest`**: Specifies the base image.
- **`/bin/bash`**: Starts a bash shell.

---

## **3. Docker Start**
Start one or more stopped containers.

```bash
docker start mycontainer
```

- Restarts the container named `mycontainer`.

---

## **4. Docker Stop**
Stop one or more running containers.

```bash
docker stop mycontainer
```

- Stops the container `mycontainer`.

---

## **5. Docker RM**
Remove one or more stopped containers.

```bash
docker rm mycontainer
```

- Deletes the container `mycontainer`.

---

## **6. Docker Images**
List all available images.

```bash
docker images
```

- Displays a list of images stored locally.

---

---

## **8. Docker Push**
Push an image or a repository to a registry.

```bash
docker push <username>/<image_name>:<tag>
```

### Steps:
1. **Tag the image**:

   docker tag image_name:version  username/image_name


   ```
   docker tag ubuntu:latest muraliburugu507/sampleapp
   ```
2. **Login to Docker Hub**:
   ```bash
   docker login
   ```
3. **Push the image**:

    ```
    docker push muraliburugu507/sampleapp
    ```


   
   docker push username/image_name


---



 Clean Everything (Optional)
To clean up everything (containers, images, volumes, and networks), use:

```bash
docker system prune -a
```

## **9. Additional Commands**

### **List Running Containers**
```bash
docker ps
```

### **List All Containers**
```bash
docker ps -a
```

### **Remove an Image**
```bash
docker rmi <image_name>
```

### **View Container Logs**
```bash
docker logs mycontainer
```

### **Run a Command in a Running Container**
```bash
docker exec -it mycontainer /bin/bash
```
