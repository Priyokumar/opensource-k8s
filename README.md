# opensource-k8s


```
kubectl create namespace opensearch
helm repo add opensearch https://opensearch-project.github.io/helm-charts/
helm repo update
helm install opensearch opensearch/opensearch --namespace opensearch -f values.yaml

helm ls -n opensearch
helm uninstall opensearch -n opensearch


k get all -n opensearch
# For accessing nodeport 
kubectl patch svc opensearch -n opensearch -p '{"spec": {"type": "NodePort"}}'
kubectl get svc -n opensearch
```

### Label agent node
```
 kubectl label node alpha label=opensearch
```
