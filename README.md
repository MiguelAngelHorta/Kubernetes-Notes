# Kubernetes-Notes
Kubernetes &amp; Cloud Native Notes

![image](https://github.com/MiguelAngelHorta/Kubernetes-Notes/assets/106134627/5b3efaa3-5d08-4be2-99d7-eeedf28e689e)


# Kubernetes Commands Cheat Sheet

## Pods

- **Create a Pod:**  
  ```yaml
  kubectl create -f <pod-definition.yaml>
  ```

- **List Pods:**  
  ```yaml
  kubectl get pods
  ```

- **Describe a Pod:**  
  ```yaml
  kubectl describe pod <pod-name>
  ```

- **Get logs from a Pod:**  
  ```yaml
  kubectl logs <pod-name>
  ```

- **Execute a command in a Pod:**  
  ```yaml
  kubectl exec -it <pod-name> -- <command>
  ```

## Deployments

- **Create a Deployment:**  
  ```yaml
  kubectl create -f <deployment-definition.yaml>
  ```

- **List Deployments:**  
  ```yaml
  kubectl get deployments
  ```

- **Scale a Deployment:**  
  ```yaml
  kubectl scale --replicas=<number-of-replicas> deployment/<deployment-name>
  ```

- **Update a Deployment:**  
  ```yaml
  kubectl apply -f <updated-deployment-definition.yaml>
  ```

- **Rollout status of a Deployment:**  
  ```yaml
  kubectl rollout status deployment/<deployment-name>
  ```

## Services

- **Create a Service:**  
  ```yaml
  kubectl create -f <service-definition.yaml>
  ```

- **List Services:**  
  ```yaml
  kubectl get services
  ```

- **Expose a Deployment as a Service:**  
  ```yaml
  kubectl expose deployment <deployment-name> --type=LoadBalancer --port=<port> --target-port=<target-port>
  ```

- **Delete a Service:**  
  ```yaml
  kubectl delete service <service-name>
  ```

## Configuration

- **View Cluster Information:**  
  ```yaml
  kubectl cluster-info
  ```

- **View Nodes:**  
  ```yaml
  kubectl get nodes
  ```

- **View Pods on a Node:**  
  ```yaml
  kubectl describe node <node-name>
  ```

- **Edit a resource:**  
  ```yaml
  kubectl edit <resource-type> <resource-name>
  ```

- **Apply changes to a resource:**  
  ```yaml
  kubectl apply -f <resource-definition.yaml>
  ```

- **Delete a resource:**  
  ```yaml
  kubectl delete <resource-type> <resource-name>
  ```

- **Get all resources with labels:**  
  ```yaml
  kubectl get all --show-labels
  ```

- **Get events across all namespaces:**  
  ```yaml
  kubectl get events --all-namespaces
  ```

- **Get YAML output for resources:**  
  ```yaml
  kubectl get <resource-type> <resource-name> -o yaml
  ```

- **Get a resource by label selector:**  
  ```yaml
  kubectl get <resource-type> -l <label-selector>
  ```
