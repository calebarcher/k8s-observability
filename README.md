# KubeSimplify: Kubernetes Observability Workshop

## Resources

- [Slides with exercises](https://docs.google.com/presentation/d/1uuYIPwQjckNiPPJQcN8tauZ8KSIdHASbyoAxJ0fc6uQ/edit?usp=sharing)


## Repository

In order to use the local [kube-prometheus](kube-prometheus/) project, initialize the submodules.

```
git submodule init && git submodule update
```

Or clone the project with `git clone --recursive ...`. 

## Preparations

The workshop requires a bare Kubernetes cluster with `kubectl` available on the terminal.

- EKS, AKS, etc.
- k3s in Civo Cloud
- minikube

This workshop needs a running Kubernetes cluster with all exercises building on top of each other. You can apply the knowledge to production clusters later when re-visiting the workshop. To access web interfaces, we will be using port-forwarding on the CLI. For production, it is recommended to look into ingress controllers (Nginx, Traefik, etc.).

To use a learning platform like Killercoda (https://killercoda.com/creators), exposed service ports can require more work with exposing NodePort to access Prometheus, Grafana, AlertManager, etc. as web interfaces. This is out of the scope of this workshop.


### Example with Civo

https://www.civo.com/learn/kubernetes-cluster-administration-using-civo-cli 

```
$ civo kubernetes create ks-k8s-o11y 

$ civo kubernetes ls
$ civo kubernetes show ks-k8s-o11y 

$ civo kubernetes config ks-k8s-o11y --save --merge

$ kubectl config use-context ks-k8s-o11y

$ kubectl get node
```

Development - https://www.civo.com/api/kubernetes#list-available-versions 

```
civo kubernetes create ks-k8s-o11y --version=1.23.10-k3s1
```


