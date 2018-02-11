# Gerrit in Kubernetes

**Proceed with caution! This is a work in progress.**

## Running

You must first initialize the Gerrit volumes before this will work. Alternatively, you may copy the git, cache, index, and db directories from an existing Gerrit installation.

```
kubectl apply -f gerrit-k8s.yml
```
