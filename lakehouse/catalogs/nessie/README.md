# Installing Nessie using Kubernetes

The easiest and recommended way to get started with Nessie on Kubernetes is to use the Helm chart described below.

## Installing the Helm chart

Add the Nessie Helm repo:
```
helm repo add nessie-helm https://charts.projectnessie.org
helm repo update
```
Install the Helm chart in the nessie-ns namespace (create the namespace first if it doesn’t exist), and name the release nessie:
```
helm install -n nessie-ns nessie nessie-helm/nessie --set replicaCount=2
```