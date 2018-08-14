# Installing Python on Ubuntu image for a Dockerfile

## Getting Started

These instructions will let you to install the latest version of Python on Ubuntu 18.04 image for Dockerfile. 

### Prerequisites

What things you need to install the software and how to install them

- I created a virtual machine on VirtualBox and installed Ubuntu OS 18.04.
- Installed Docker

### Installing

A step by step series of examples that tell you how to install Python on Ubuntu 18.04

First of all, open the terminal window on your local machine and create a file called "Dockerfile".
For example, I will create my Dockerfile in to my Documents directory.

```
cd Documents
```
Now, create a file called "Dockerfile" under Documents directory (or which directory you have chosen)
```
touch Dockerfile
```

After that, open the Dockerfile with your favorite text editor, I prefer nano editor
```
nano Dockerfile
```
Paste the code below
```
#Pull base image
FROM ubuntu:18.04

# Install Python.
RUN \
  apt-get update && \
  apt-get install -y python python-dev python-pip python-virtualenv && \
  rm -rf /var/lib/apt/lists/*
```
Now you can build your Dockerfile and it's done!
```
docker build -t example1 .
```
!!! Please don't forget to put a dot at the end of your tag name otherwise it won't work.

