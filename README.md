# kubecost


Step 1: Install Kubecost

Running the following command will also install Prometheus and Grafana in the namespace supplied. View install configuration options here.

```bash
helm install kubecost cost-analyzer \
--repo https://kubecost.github.io/cost-analyzer/ \
--namespace kubecost --create-namespace
```

Step 2: Enable port-forward

```bash
kubectl port-forward --namespace kubecost deployment/kubecost-cost-analyzer 9090
```

Step 3: See the data!

You can now view the deployed frontend by visiting the following link. Publish :9090 as a secure endpoint on your cluster to remove the need to port forward.

http://localhost:9090
