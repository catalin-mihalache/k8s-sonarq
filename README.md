# sonarqube-on-kubernetes
Steps and YAML config to deploy SonarQ in Kubernetes.

# Pre-requisites
Install:
- *kubectl* - https://kubernetes.io/docs/tasks/tools/install-kubectl/
- *minikube* - https://github.com/kubernetes/minikube

Check if cluster is up and running - *kubectl get nodes*

# Run manifests
### Create the namespace
```kubectl create -f sonar-namespace.yaml```
### Create the persistent volume for PostgresDB
```kubectl create -f postgres-pvc.yaml```
### Deploy and config the PostgresDB
```kubectl create -f postgres-app.yaml```
### Create the persistent volume for SonarQ
```kubectl create -f sonar-pvc.yaml```
### Deploy and config the SonarQ
```kubectl create -f sonar-app.yaml```
### Create the Ingress rule
```kubectl create -f sonar-ingress.yaml```




# Check pods

 kubectl get pod -n "namespace"

# Check Sonar service

kubectl get svc -n "namespace"
