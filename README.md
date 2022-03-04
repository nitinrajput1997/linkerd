# linkerd

### Install the CLI
```bash
curl --proto '=https' --tlsv1.2 -sSfL https://run.linkerd.io/install | sh
export PATH=$PATH:/home/ubuntu/.linkerd2/bin
linkerd version
```

### Validate your Kubernetes cluster

```bash
linkerd check --pre
```

### Install the control plane onto your cluster
```bash
linkerd install | kubectl apply -f -
linkerd check
linkerd viz install | kubectl apply -f - # install the on-cluster metrics stack
```
