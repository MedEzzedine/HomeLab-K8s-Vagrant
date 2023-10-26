
# Kubernetes Home Lab
This project allows you to setup a K8s cluster with 1 master node and as many worker nodes as you wish with ONE command:
```bash
vagrant up
```

## Requirements
You need the following packages installed in your local Linux machine:
- **Vagrant**: Infrastructure as Code tool that allows you automatically spin and manage VMs.
- **VirtualBox**: Software responsible for the lifecycle of Virtual Machines from creation until deletion (Can alternatively use any other type 2 hypervisor)
- **Ansible**: A configuration management tool that installs dependencies needed for the cluster nodes.

## Connecting to the K8s cluster
After running "vagrant up" and making sure all the nodes are running correctly, follow these steps to connect to the cluster via Kubectl:
1. Install kubectl on your local machine ([instructions](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/))
2. Connect to the master node using SSH:
	```bash
	vagrant ssh k8s-master
	```
3. Once there, open **~/.kube/config.yml** and copy its contents to your local machine under the same path: **~/.kube/config.yml**
4. That's all, to check that everything works correctly, run:
	```bash
	kubectl get nodes
	```
