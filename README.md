# sonarqube-on-kubernetes
Steps and YAML config to deploy SonarQ in Kubernetes.

# Pre-requisites
Install:
- *kubectl* - https://kubernetes.io/docs/tasks/tools/install-kubectl/
- *minikube* - https://github.com/kubernetes/minikube

Check if cluster is up and running - *kubectl get nodes*

# Run manifests

kubectl create -f <manifest.yaml>


# Check pods

 kubectl get pod -n <namespace>

# Check Sonar service

kubectl get svc -n <namespace>