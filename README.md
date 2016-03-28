# Kubernetes Setup
This repo is for useful scripts and resources to setup kubernetes environment. 
## Introduction
Kubernetes is a very powerful container management system by Google for large scale systems. 

## Main Components 
Following are the main components for a kubernetes system

### Etcd2
The etcd project, was developed by the CoreOS team, is a lightweight, distributed key-value store that can be distributed across multiple nodes. Kubernetes uses this service to store and retreive configuration data for each node in the cluster.
### Apiserver
### Controller-manager
### kubecfg
### kubelet
### proxy
### Pods
### Services
### Replication Controllers
## Installation 

### CoreOS VM
Create a virtual machine with CoreOS installed in VirtualBox. You can use any other virtualisation software to acheive this, as long as the OS is CoreOS.
The version of CoreOS I used for this setup is:
```

```
Install CoreOS
Set password for core user on the server
passwd centos

Login remotely into the machine via ssh with core users and password you specified.
By default coreos installation doesn't have the password. 

So for this setup we will construct cloud-config file and setup a user on installation. 
sudo coreos-install -d /dev/sda -C stable
Discovery service: https://discovery.etcd.io

By default in CoreOS instance all ports are open. If you are planning to use this cluster in production you will need to lock the ports down.

### Commands 
sudo su - 
sudo mkdir -p /opt/kubernetes/bin 
sudo chown -R core: /opt/kubernetes
cd /opt/kubernetes

https://coreos.com/kubernetes/docs/latest/getting-started.html

wget https://github.com/kelseyhightower/kubernetes-coreos/releases/download/v0.0.1/kubernetes-coreos.tar.gz
tar -C bin/ -xvf kubernetes-coreos.tar.gz


## Reference
http://www.liberidu.com/blog/2015/04/11/basic-newbie-install-coreos-on-virtualbox-getting-started-with-docker/
