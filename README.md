# boinc-kubernetes

Deploying a Boinc pod in k3s with 3 tasks

```bash

  $> export KUBECONFIG=/etc/rancher/k3s/k3s.yaml (particular requirement for k3s)

  # Load Credentials in a secret
  $> kubectl apply -f ./secrets.yaml

  $ Apply pod
  $> kubectl apply -f ./boinc_client.yaml

  # We can check that everything went fine with the kubectl commands:

  $> kubectl describe pod boinc-deployment
  $> kubectl logs boinc-deployment
  
  $> kubectl logs <POD_ID> -n default
  
```

TODOs

- [x] Add kubernetes support
- [ ] Using secrets template to avoid to push credentials
- [ ] Try to connect with GPU (Jetson Nano)


References:

* https://www.suse.com/c/running-edge-artificial-intelligence-k3s-cluster-with-nvidia-jetson-nano-boards-src/
* https://www.elarraydejota.com/despliegue-de-boinc-en-k8s/
* https://boinc.berkeley.edu/wiki/Boinccmd_tool
* https://scienceunited.org/forum_thread.php?id=82
