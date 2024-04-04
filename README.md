K8s cluster has two major components
1.	Master node
2.	Worker node
Node: physical machine or virtual worker machine where containers will be deployed by k8s.
Cluster: set of nodes grouped together.
Master or control panel manages the cluster


Components of K8s:
API server, scheduler, control manager etcd, kubelet, container runtime and kube-proxy.
Kubernetes Basics
we will learn some important Basics of Kubernetes:
Cluster:
It is a collection of hosts(servers) that helps you to aggregate their available resources. That includes ram, CPU,  disk, and their devices into a usable pool.
Master:
The master is a collection of components which make up the control panel of Kubernetes. These components are used for all cluster decisions. It includes both scheduling and responding to cluster events.
Node:
It is a single host which is capable of running on a physical or virtual machine. A node should run both kube-proxy, minikube, and kubelet which are considered as a part of the cluster.
Namespace:
It is a logical cluster or environment. It is a widely used method which is used for scoping access or dividing a cluster.
Kubernetes Architecture:
Kubernetes has two nodes – master node and worker/slave node.
Master node:
The master node is the first and most vital component which is responsible for the management of Kubernetes cluster. it is the entry point of all kind of administrative tasks. there might be more than one master node in the cluster to check for fault tolerance.
The master node has various components like API server, Controller manager, kubectl, scheduler and ETCD.
ETCD: 
•	This component stores the configuration details and essential values in key value form 
{
“name”: “xyz”,
“part”: “ght”
}
•	It communicates with all other components to receive the commands to perform an action.
•	It is also called as meta data storage.

Controller Manager:
•	A daemon (server) that runs in continuous loop and is responsible for gathering information and sending it to the API server.
•	Works to get the shared set of clusters and change them to the desired state of the server.
•	The key controllers are the replication controllers, endpoint controllers, namespace controllers and service account controllers.
•	The controller manager runs controllers to administer nodes and endpoints.

Scheduler
•	The Schedular assigns the tasks to the slave nodes.
•	It is responsible for distributing the workload and stores resource usage information on every node.

API Server
•	Kubernetes uses the API server to perform all operations on the cluster.
•	It is central management entity that receives all REST requests for modifications, serving as frontend to the cluster.
Kubectl
•	Kubectl controls the Kubernetes cluster manager.

Worker/Slave nodes
Worker nodes are another essential component which contains all the required services to manage the networking between the containers, communicate with the master node, which allows you to assign resources to the scheduled containers.
•	Kubelet: gets the configuration of a Pod from the API server and ensures that the described containers are up and running.
•	Docker Container: Docker container runs on each of the worker nodes, which runs the configured pods.
•	Kube-proxy: Kube-proxy acts as a load balancer and network proxy to perform service on a single worker node.
•	Pods: A pod is a combination of single or multiple containers that logically runs together on nodes.
![image](https://github.com/Roopa2487/Kubernets_yaml_files_roopa2487/assets/154946002/9f20c5cc-c791-4286-b5b9-bfaaa25bc3b8)
![image](https://github.com/Roopa2487/Kubernets_yaml_files_roopa2487/assets/154946002/ccc5924e-bedd-4710-9170-4b874108e545)
