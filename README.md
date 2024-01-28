Kubernetes Clusters

Installed Docker
Installed kubectl 
Installed minikube for local development 
Opened a terminal and ran the following command to start a local Kubernetes cluster:
    minikube start
Verified that Minikube is running and kubectl is configured
    kubectl cluster-info
On each worker node, joined the cluster by running the command provided by the kubeadm init output on the master:
On the machine where kubectl is configured 
    kubectl get nodes
   Verified that all nodes are in the `Ready` state.
    kubectl get pods --all-namespaces
  Verified that the cluster is running essential Kubernetes components.
Created a deployment
    kubectl create deployment nginx-deployment --image=nginx
Exposed the deployment:
    kubectl expose deployment nginx-deployment --type=NodePort --port=80
Accessed the application:
    minikube service nginx-deployment
Opened the provided URL to access the deployed application.

 Successfully set up and verified a Kubernetes cluster. Customized the cluster configuration and application deployments.
