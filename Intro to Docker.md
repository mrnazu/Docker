# Intro to Docker
Learn to create, build and deploy Docker containers!

In this room, you’ll get your first hands-on experience deploying and interacting with Docker containers.
Namely, by the end of the room, you will be familiar with the following:

- The basic syntax to get you started with Docker
- Running and deploying your first container
- Understanding how Docker containers are distributed using images
- Creating your own image using a Dockerfile
- How Dockerfiles are used to build containers, using Docker Compose to orchestrate multiple containers
- Applying the knowledge gained from the room into the practical element at the end.



## Docker 
It is a platform for creating containerized environments for applications. containers are self-contained environments that allow applications to run without interference from the host operating system. docker is a tool that makes it easy to build and deploy containers, and it provides many features and capabilities that help make containerization easier and more efficient. docker is a powerful technology that can greatly improve the performance and usability of applications.

lets say you have an application which relies on a database. with docker, you can easily create a containerized environment for your application, including the database. you can then deploy this containerized environment to any cloud service provider, or even into your own private cloud. this gives your application a highly scalable, portable, and highly available environment, which can be deployed into any cloud provider with ease. docker offers many benefits for developers and administrators alike, and it is a great tool to understand and use if you want to take your applications to the next level.



## Basic Docker Syntax 
The syntax for Docker can be categorised into four main groups:
- Running a container
- Managing & Inspecting containers
- Managing Docker images
- Docker daemon stats and information

### Managing Docker Images
docker image is essentially a standalone package which contains everything required to run a container environment, including base operating system, application and code, dependencies, libraries, and any required configuration settings. this makes it easy to create and deploy containers without having to piece together all of the necessary components manually. the docker image library contains a variety of pre-built images which come with a wide range of packages and configurations to make containers easy to develop and deploy.

imagine you have a service which you want to deploy in a container environment. you could start from scratch and piece together all of the necessary components manually, or you could use a pre-built image from the docker images library which contains everything you need. the purpose of images is to save you time and provide a quick and easy way to create and deploy a container environment without having to do all of the work yourself, which can be time consuming and tedious. in short, images are standalone packages which contain everything required to run a container environment, including base operating system, application and code, dependencies, and any required configuration settings.

so Managing Docker Images would consist of the process of creating, updating, tagging, and removing images in the docker images library. this can be done manually or using tools like docker compose, which can help automate and simplify the process. as previously mentioned, these images are pre-built and typically built from popular open source projects. the best example would be something like a LAMP stack image, which would contain all of the necessary components to run a LAMP stack application in a container environment, without the need to piece together all of the necessary components manually. this makes creating and deploying containers easy and straightforward.
#### Docker Pull
The docker pull command is used to pull down pre-built images from the docker images library. This is a quick and easy way to create and deploy containers, without having to build your own images from scratch. this command will download the image from the docker images library and store it locally on your machine. in addition, this command will also check if a newer image is available, and will update the local image if this is the case. the docker pull command allows you to utilize pre-built images to create and deploy containers, without having to build them yourself. so in short word or in other word The docker pull command downloads Docker images from the internet.

So, if you execute `docker pull nginx` that will download the nginx image from the docker images library, and store it locally on your machine. this command will also check if there is a newer version of the image available, and will update the local image if this is the case.

`docker pull ubuntu` - IS THE SAME AS - `docker pull ubuntu:latest` - it will download the latest version of the ubuntu image from the docker images library.
`docker pull ubuntu:22.04` - This command will pull version "22.04 (Jammy)" of the "ubuntu" image.
**When specifying a tag, you must include a colon : between the image name and tag, for example, ubuntu:22.04 (image:tag).**

`docker image` - is a command which allows you to view the list of images that you have downloaded locally on your machine. This command can be helpful to get a snapshot of your local docker images library, and to see if any new or updated images are available. The command also allows to inspect information about a specific image, such as its age, size, name, and tag, which can help you track and manage your docker images. You can also use "docker image" to delete images from your local images library, which is helpful when you need to remove unused or no longer needed images.

```┌──(nazu㉿Nazu)-[~]
└─$ docker image

Usage:  docker image COMMAND

Manage images

Commands:
  build       Build an image from a Dockerfile
  history     Show the history of an image
  import      Import the contents from a tarball to create a filesystem image
  inspect     Display detailed information on one or more images
  load        Load an image from a tar archive or STDIN
  ls          List images
  prune       Remove unused images
  pull        Pull an image or a repository from a registry
  push        Push an image or a repository to a registry
  rm          Remove one or more images
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE

Run 'docker image COMMAND --help' for more information on a command.
```
If we want to remove an image from the system, we can use docker image rm along with the name (or Image ID). In the following example, I will remove the "ubuntu" image with the tag "22.04". My command will be `docker image rm ubuntu:22.04`                                                                                   



## Running Your First Container 
