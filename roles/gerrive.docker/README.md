# Ansible Role: Docker

[![Build Status](https://travis-ci.org/gerrive/ansible-role-docker.svg?branch=master)](https://travis-ci.org/gerrive/ansible-role-docker)

Installs [Docker](https://www.docker.com), Docker is an open platform for developers and sysadmins to build, ship, and run distributed applications, whether on laptops, data center VMs, or the cloud.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values (see defaults/main.yml):

```
docker_keyserver: "hkp://p80.pool.sks-keyservers.net:80"
```
The location where we obtain the package key

```
docker_options: ""
```
[Configuring Docker](https://docs.docker.com/engine/admin/#/configuring-docker) enable debug mode, tls, and listen connections

```
docker_user: "vagrant"
```
User that will be added to the docker group similar to the `sudo usermod -aG docker <user-name>`

```
docker_proxy: false
```
Enable proxy setting configs

```
docker_proxy_http: http://proxy.example.com:8080
```
The proxy variable that will be used to configure docker

## Dependencies

None

## Example Playbook

```
- hosts: servers
  roles:
    - gerrive.docker
```

## License

MIT / BSD
