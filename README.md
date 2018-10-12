# Docker Openstack Ansible Client
[![Build Status](https://travis-ci.org/snieking/docker-openstack-ansible-client.svg?branch=master)](https://travis-ci.org/snieking/docker-openstack-ansible-client)
[![Docker Pulls](https://img.shields.io/docker/pulls/mashape/kong.svg)](https://hub.docker.com/r/snieking/docker-openstack-ansible-client/builds/)
[![Docker Automated build](https://img.shields.io/docker/automated/snieking/docker-openstack-ansible-client.svg)](https://hub.docker.com/r/snieking/docker-openstack-ansible-client/builds/)

Image that can be used for Openstack deployments with Ansible.

It is suggested and adviced to map in either your openstack.rc file or clouds.yaml, .ssh folder, ansible roles and playbook directories.

```
docker run -it \
  -v ${HOME}/.config/openstack:/etc/openstack \
  -v ${HOME}/.ssh:/home/docker/.ssh \
  -v ${HOME}/ansible:/home/docker/ansible \
  snieking/docker-openstack-ansible-client
```

## Tips

Create an alias for running the container so that you can start the container with one command.

*~/.bashrc* 
```
alias os-ansible-cli='docker run -it \
  -v ${HOME}/.config/openstack:/etc/openstack \
  -v ${HOME}/.ssh:/home/docker/.ssh \
  -v ${HOME}/ansible:/home/docker/ansible \
  snieking/docker-openstack-ansible-client'
```
