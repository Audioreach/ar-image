# ar-image
Docker image for building the Audioreach projects

This project contains the recipe for a Docker image containing necessary tools
for building the Audioreach projects.

## Installing docker

If Docker isn't installed on your system yet, you can follow the instructions
provided at Docker's official documentation.

https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository

### Add user to the docker group
```
sudo usermod -aG docker $USER
newgrp docker
```

Restart your terminal, or log out and log in again, to ensure your user is
added to the **docker** group (the output of `id` should contain *docker*).

## Generating Docker image

With docker installed, you can generate the docker image that will be used to
operate on the kernel tree. Do this by running *docker build* in the directory
where you cloned this project:

```
docker build -t ar-image .
```
