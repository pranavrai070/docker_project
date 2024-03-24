# Docker Container Deployment with Ansible

This project demonstrates how to deploy a Docker container using Ansible. The Docker container runs an Apache service with a static web page and is deployed on a host machine with a specified IP address.

## Requirements

- Ansible installed on the control machine.
- Docker installed on the target machine(s).
- Control machine with SSH access to the target machine(s).
- Host machine with the IP address `172.168.10.1`.
- Docker container with the IP address `172.168.10.2`.

## Ansible Inventory

Ensure that the Ansible inventory file (`hosts`) is properly configured with the IP addresses of the host machine and the Docker container. Example:


[my_subnet]
172.168.10.1 ansible_user=username

[my_docker_container]
172.168.10.2 ansible_user=username

## To deploy the Docker container, run the Ansible playbook as follows:

`ansible-playbook playbook.yml -i hosts`


### Managing the Docker Container

## Starting the Container: 
`docker start my_apache_container`

## Stopping the Container:: 
`docker stop my_apache_container`

## Restarting the Container: 
`docker restart my_apache_container`


## Deleting the Container: 
`docker rm my_apache_container`

