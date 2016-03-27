# Kubernetes Setup
This repo is for useful scripts and resources to setup kubernetes environment. 
## Introduction
Kubernetes is a very powerful container management system by Google for large scale systems. 

## Main Components 
Following are the main components for a kubernetes system

### Etcd
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
### Commands 
sudo su - 
sudo mkdir -p /opt/kubernetes/bin 
sudo chown -R core: /opt/kubernetes
cd /opt/kubernetes
wget https://github.com/kelseyhightower/kubernetes-coreos/releases/download/v0.0.1/kubernetes-coreos.tar.gz
tar -C bin/ -xvf kubernetes-coreos.tar.gz
