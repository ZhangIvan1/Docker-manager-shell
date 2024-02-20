# Docker Management Script

[English](#docker-management-script) | [中文](#docker-管理脚本)

## Introduction

This script aims to simplify Docker management operations, especially for students in the laboratory who are not familiar with Docker. With this script, you can easily manage Docker images, containers, networks, and volumes without having to delve into Docker command-line operations.

## Prerequisites

Before using the script, make sure to complete the following prerequisites:

1. **Install Docker:** Make sure Docker is installed on your system. If not, refer to the Docker official documentation for installation instructions.

2. **Create User File:** Create a file named `docker_user` in the `~/docker_user` path and add usernames and passwords in the following format:

    ```
    username1:password1
    username2:password2
    ...
    ```

    Ensure that each line contains only one username and password, separated by a colon `:`, without spaces. This file is used for user login to ensure that only authorized users can perform operations.

## Usage

### Running the Script

In the terminal, execute the following command, ensuring you are in the directory where the script is located and have sudo privileges:

```bash
sudo ./docker_manage
```

### Functionality

- **Login Functionality:** Log in with a username and password to ensure only authorized users can execute operations.
- **Image Management:** Support pulling, building, deleting, and updating images to facilitate image resource acquisition and maintenance.
- **Container Management:** Provide container operations such as creating, deleting, starting, stopping, restarting, viewing details, and logs to simplify container management.
- **Network Management:** View network details, create, and delete networks to assist in configuring network connections between containers.
- **Volume Management:** Support creating and deleting volumes and easily mounting volumes into containers for persistent data storage.

## Tenant Management

The script includes a simple tenant management system that implements permission control by recognizing prefixes in container, image, and volume names. Each user can only operate containers, images, and volumes with their username prefix, thus enforcing user permissions.

## Disclaimer

- Using this script requires sudo privileges. Please ensure you have been authorized to execute Docker-related operations.
- Exercise caution when performing operations to avoid data loss or system instability.
- This script is still in the experimental stage. Please do not use it in a production environment. It is recommended to validate its functionality before use.
- For any questions or concerns, please consult the laboratory's Docker management personnel, who will be happy to assist you.
- This project is for learning and research purposes only. Commercial use is discouraged, and no responsibility is taken for any losses incurred due to the use of this project.
