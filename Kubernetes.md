Certainly! Here are detailed notes on Kubernetes, covering the topics you mentioned.

### What is Kubernetes and its Function?
Kubernetes, also known as K8s, is an open-source platform designed to automate deploying, scaling, and operating application containers. Developed by Google, it aims to provide a framework for running distributed systems resiliently, allowing for scaling and failover for your application, provisioning of deployment patterns, and more. Essentially, Kubernetes manages various aspects of containerized applications to ensure they run efficiently across a cluster of machines.

### Primary Advantages of Using Kubernetes
1. **Scalability**: Kubernetes can scale applications automatically based on their resource usage or other metrics. It supports both horizontal and vertical scaling.
2. **Load Balancing**: Kubernetes provides built-in load balancing and traffic distribution, which helps distribute incoming network traffic efficiently.
3. **High Availability**: It ensures that applications have higher availability by maintaining the desired state of applications and automatically replacing or restarting failed containers.
4. **Automated Rollouts and Rollbacks**: Kubernetes can manage application updates and rollbacks seamlessly, thus allowing for continuous integration and continuous deployment.
5. **Environment Consistency and Version Control**: Helps maintain consistency across development, testing, and production environments, which simplifies the development cycle.
6. **Resource Utilization**: Allows efficient usage of underlying resources, reducing costs.

### Architecture of Kubernetes
Kubernetes follows a client-server architecture. The main components include:
- **Master Node**: The control plane of Kubernetes, managing the state of the cluster.
- **Worker Nodes**: Nodes that run the applications using containers.

### Components of Master Nodes and Worker Nodes
- **Master Node Components**:
  1. **API Server**: Acts as the front end to the cluster, through which all internal and external communications pass.
  2. **etcd**: A highly available key-value store used as Kubernetes' backing store for all cluster data.
  3. **Scheduler**: Responsible for scheduling pods on nodes based on resource availability.
  4. **Controller Manager**: Manages controllers that regulate the state of the cluster, handle node failures, and ensure correctness.
  5. **Cloud Controller Manager**: Manages components that interact with underlying cloud services.

- **Worker Node Components**:
  1. **Kubelet**: An agent running on each node, ensuring containers are running in a pod.
  2. **Kube-Proxy**: Maintains network rules that allow network communication to your pods from network sessions inside or outside of your cluster.
  3. **Container Runtime**: The software responsible for running containers (e.g., Docker).

### Three Pod Container Design Patterns
1. **Sidecar Pattern**: Uses a secondary container as a helper to the main application container, enhancing or extending its functionality.
2. **Ambassador Pattern**: Abstracts network connectivity, allowing the main container to be oblivious of the network aspects.
3. **Adapter Pattern**: Standardizes and normalizes the output of the main container to suit other components or services.

### Building Blocks of Kubernetes
- **Nodes**: Physical or virtual machines that run the applications.
- **Pods**: The smallest deployable units that can be created, scheduled, and managed. A pod usually represents one running process in your cluster.
- **Labels and Selectors**: Used to organize and select groups of objects based on key-value pairs.
- **Controllers**: Ensure the desired state of the cluster matches the observed state, and act when needed.

### What is Kubernetes Service and What Does it Do?
A Kubernetes Service is an abstraction which defines a logical set of Pods and a policy by which to access them. This is often used to handle load balancing configurations and to ensure that the networking environment remains consistent and predictable despite dynamic changes in the pod configurations.

### Kubernetes Service Proxy
Kube-proxy is a network proxy that runs on each node in the cluster, maintaining network rules on nodes. These rules allow network communication to your Pods from network sessions inside or outside of your cluster.

### Kubernetes Comparison with Docker Swarm
- **Ease of Use**: Docker Swarm is easier to configure compared to Kubernetes.
- **Scalability**: Kubernetes is highly scalable and maintains strong guarantees about the cluster state which makes it suitable for larger deployments.
- **Features**: Kubernetes offers a richer feature set particularly around deployments, scaling, networking, and storage.
- **Community and Adoption**: Kubernetes has a larger community and more widespread adoption in the industry compared to Docker Swarm.

These notes should provide a robust foundation for your studies on Kubernetes. If you need more details on any specific part, feel free to ask!