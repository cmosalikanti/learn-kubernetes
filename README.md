## Kubernetes Cluster

-   Top-level entity that encompasses all of the infrastructure components needed to run and manage containerized applications.

-   It has multiple nodes

-   Cluster includes:
        Master node(s) - Responsible for the overall management and control of the cluster like scheduling, load-balancing etc., 
        Worker nodes   - Run the applications in containers.

**Kubernetes Node**

- Single machine (either physical or virtual) within a Kubernetes cluster that runs one or more containers.

**Pod**

-    A Node contains multiple pods

**Container**

-   A pod can run one or more containers, but typically, each pod runs one container to maintain simplicity and scalability.

-   runtime instance of a Docker image. It is the active version of an image that is running.

**Docker Image**

An executable piece of software that contains the application code, libraries, environment variables, and configurations needed to run a program.

**minikube

quickly sets up a local Kubernetes cluster on macOS, Linux, and Windows. On Cloud, we can have clusters from cloud providers like Google, Amazon etc.,

**kubectl**
    
helps to manage the cluster e.g., kubectl get nodes

**busybox**

like an app to see if the containers in the pod are running

**Cluster**
    
An instance of Kubernetes.

**Kubernetes Control Plane**

This is like an air-traffic control tower in an airport. It has different components to support the control:

1.  Kube API:   Exposes the Kubernetes API and handles requests to interact with the cluster. 
2.  Kube Scheduler: watches for newly created pods that don’t have a node assigned and selects a suitable node for them to run on.
3.  Kube Control Manager: runs a set of controllers that manage the state of the cluster. Controllers continuously monitor the cluster state and ensure that the desired state is maintained.
4.  etcd :  key-value store. stores the state of the Kubernetes' cluster data.
5.  Cloud Controller Manager: enables Kubernetes to interact with various cloud providers’ APIs (e.g., AWS, GCP, Azure). It is responsible for managing cloud-specific resources and services, like load balancers, storage volumes, and network configurations.

**Components of a node**
1.  Container Runtime: Pulls container images, creates and manages containers, and ensures they run properly and securely as directed by the Kubernetes control plane
2.  kube-proxy: A network proxy that runs on each node in a Kubernetes cluster, maintaining network rules and enabling communication between pods and services within the node and the control plane, while also communicating directly with the kube-apiserver
3.  kubelet: An agent that runs on each node in a Kubernetes cluster, ensuring containers in a pod are running and healthy while communicating with the API server in the control plane to maintain the desired state of the node.    

**Three ways to ensure security of the Kubernetes cluster**
1. Add the "securiy context" in the YAML file.
2. Use Synk - Pronouced as Sneak. Scan for any securities issues in the *.yml. More info at: https://snyk.io/        
3. Update the Kubernetes software to the latest version, following the updates.
