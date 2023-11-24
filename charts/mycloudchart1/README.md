# StackSimplify Simple Helm Chart

## Step-00: Introduction
- This Helm Chart will deploy the following Resources
  1. Kubernetes Load Balancer 
  2. Kubernetes Deployment 

## Step-01: Add Custom Helm Repo
```t
# List Helm Repositories
helm repo list

# Add Helm Repository
helm repo add <DESIRED-NAME> <HELM-REPO-URL>
helm repo add stacksimplify https://stacksimplify.github.io/cloud-helm-charts/

# List Helm Repositories
helm repo list

# Search Helm Repository
helm search repo <KEY-WORD>
helm search repo mycloudchart1
```

## Step-02: Install Helm Chart from our Custom Helm Repository
```t
# Install myapp1 Helm Chart
helm install <RELEASE-NAME> <repo_name_in_your_local_desktop/chart_name>
helm install myapp1 stacksimplify/mycloudchart1
```
## Step-03: List Resources and Access Application in Browser
```t
# List Helm Release
helm ls 
or 
helm list

# helm status
helm status myapp1 --show-resources

# List Pods
kubectl get pods

# List Services 
kubectl get svc

# Access Application
http://localhost
```