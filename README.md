# CentOS Stream 9 QEMU Virtual Machine in Docker Container

![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=for-the-badge&logo=qemu&logoColor=white)
![CentOS](https://img.shields.io/badge/CentOS-002260?style=for-the-badge&logo=centos&logoColor=white)

A lightweight **CentOS Stream 9** virtual machine running inside a Docker container using QEMU/KVM for optimal performance.

## Features

- 🐳 Containerized CentOS Stream 9 VM  
- ⚡ KVM-accelerated for near-native performance  
- 🌐 Web-based VNC access (port **6080**)  
- 🔑 SSH access (port **2221**)  
- 💾 Persistent storage volume  

## Prerequisites

- Docker installed  
- KVM support on host machine  
- `sudo` privileges (for KVM device access)  

## VM User and Password

- **Username:** `root`  
- **Password:** `root`  

## Installation

```bash
# Clone the repository
git clone https://github.com/ParaNoob123/CentOS-Stream-9
cd CentOS-Stream-9

# Build the Docker image
docker build -t centos-vm .

# Run the container
docker run --privileged -p 6080:6080 -p 2221:2221 -v $PWD/vmdata:/data centos-vm
