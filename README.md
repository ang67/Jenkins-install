# Jenkins-install

1. Create a Namespace for Jenkins.

```
kubectl create namespace devops-tools
```

2. Create a 'serviceAccount.yaml' file andcopy the following admin service account manifest.

```
kubectl apply -f serviceAccount.yaml
```

3. Create local persistent volume

```
kubectl create -f volume.yaml
```

4. Create a Deployment

```
kubectl apply -f deployment.yaml
```

5. Create a service

```
kubectl apply -f service.yaml
```


Open to outside 
```
kubectl port-forward service/jenkins-service 8080:8080
```

http://localhost:8080/