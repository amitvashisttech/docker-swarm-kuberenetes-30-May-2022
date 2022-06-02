# Docker login
```
docker login
ls /root/.docker/config.json
```

# Create a Secret in K8s for Docker Registry
```
kubectl create secret generic regcred --from-file=.dockerconfigjson=/root/.docker/config.json --type=kubernetes.io/dockerconfigjson 
kubectl get secrets  
```

# Apply the Nginx POD Config: 
```
kubectl apply -f nginx.yaml
```

# Check the POD Status 
```
kubectl get pods
kubectl get pods -o wide 
```
