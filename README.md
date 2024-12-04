# Argo CD Autopilot Design

This configuration design is an output from the [Argo CD Labs Autopilot project](https://github.com/argoproj-labs/argocd-autopilot).

Advantages of this configuration include:

- Argo CD managing itself
- Argo CD managing namespaces, Application Sets (apps and environments)
- After the initial `kubectl apply``, no further manual configuration is normally required

## Installing Argo

Assumes a single Argo CD managing one or more clusters.

```shell
kubectl apply -f ./boostrap/argo-cd.yaml
kubectl apply -f ./boostrap/cluster-resources.yaml
kubectl apply -f ./boostrap/root.yaml
```
