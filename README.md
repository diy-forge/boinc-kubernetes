# boinc-kubernetes

Deploying a Boinc pod in k3s with 3 tasks

```bash

  # Load Credentials in a secret
  $> KUBECONFIG=/etc/rancher/k3s/k3s.yaml kubectl apply -f ./secrets.yaml

  $ Apply pod
  $> KUBECONFIG=/etc/rancher/k3s/k3s.yaml kubectl apply -f ./boinc_client.yaml

  # We can check that everything went fine with the kubectl commands:

  $> KUBECONFIG=/etc/rancher/k3s/k3s.yaml kubectl describe pod boinc-deployment
  $> KUBECONFIG=/etc/rancher/k3s/k3s.yaml kubectl logs boinc-deployment

```

TODOs

- [x] Add kubernetes support
- [ ] Try to connect with GPU (Jetson Nano)


References:

* https://www.suse.com/c/running-edge-artificial-intelligence-k3s-cluster-with-nvidia-jetson-nano-boards-src/
* https://www.elarraydejota.com/despliegue-de-boinc-en-k8s/
* https://boinc.berkeley.edu/wiki/Boinccmd_tool
* https://scienceunited.org/forum_thread.php?id=82
