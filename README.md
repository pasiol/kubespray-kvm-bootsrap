# Kubespray KVM cluster nodes bootstrapping playbook

Ansible playbook generates VM nodes for the Kubespray cluster on the LibVirt hypervisor.  Developers can easily install a cheap local development environment for the HA Kubernetes cluster.

## Hardware requirements

(Old) server/workstation with eight or more cores and 64GB EEC memory. Four disks are recommended, one SSD for OS and three ssd disks for KVM pools. Place one master and worker per KVM storage pool, for performance optimization and distributing disk IO. The UPS is also convenient every power loss is not destroying the cluster.

## Software requirements

- for better performance disable the swap partition
- minimal installation of OS without GUI, system on the run level 3
- KVM and libvirt libraries
- server OS: Debian 11 or RHEL8/9-based distribution
- firewalld on the KVM host
- openssh server for management and opening access to K8S services

## Supported node os

- Debian 11, lightweight and easy to set up (in progress)

## Roadmap

- a playbook for creating pools
- a playbook for removing old cluster
- a playbook for installing required libraries for the KVM host
- creating ssh-keys without community.crypto library
- HAproxy Node
