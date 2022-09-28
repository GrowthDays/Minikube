# Minikube

## Addons

```bash
$ minikube addons list
```
Output:

```
|-----------------------------|----------|--------------|--------------------------------|
| ADDON NAME                    | PROFILE    | STATUS         | MAINTAINER                       |
| ----------------------------- | ---------- | -------------- | -------------------------------- |
| ambassador                    | minikube   | disabled       | 3rd party (Ambassador)           |
| auto-pause                    | minikube   | disabled       | Google                           |
| csi-hostpath-driver           | minikube   | disabled       | Kubernetes                       |
| dashboard                     | minikube   | enabled ✅      | Kubernetes                       |
| default-storageclass          | minikube   | enabled ✅      | Kubernetes                       |
| efk                           | minikube   | disabled       | 3rd party (Elastic)              |
| freshpod                      | minikube   | disabled       | Google                           |
| gcp-auth                      | minikube   | disabled       | Google                           |
| gvisor                        | minikube   | disabled       | Google                           |
| headlamp                      | minikube   | disabled       | 3rd party (kinvolk.io)           |
| helm-tiller                   | minikube   | disabled       | 3rd party (Helm)                 |
| inaccel                       | minikube   | disabled       | 3rd party (InAccel               |
|                               |            |                | [info@inaccel.com])              |
| ingress                       | minikube   | disabled       | Kubernetes                       |
| ingress-dns                   | minikube   | disabled       | Google                           |
| istio                         | minikube   | disabled       | 3rd party (Istio)                |
| istio-provisioner             | minikube   | disabled       | 3rd party (Istio)                |
| kong                          | minikube   | disabled       | 3rd party (Kong HQ)              |
| kubevirt                      | minikube   | disabled       | 3rd party (KubeVirt)             |
| logviewer                     | minikube   | disabled       | 3rd party (unknown)              |
| metallb                       | minikube   | disabled       | 3rd party (MetalLB)              |
| metrics-server                | minikube   | disabled       | Kubernetes                       |
| nvidia-driver-installer       | minikube   | disabled       | Google                           |
| nvidia-gpu-device-plugin      | minikube   | disabled       | 3rd party (Nvidia)               |
| olm                           | minikube   | disabled       | 3rd party (Operator Framework)   |
| pod-security-policy           | minikube   | disabled       | 3rd party (unknown)              |
| portainer                     | minikube   | disabled       | 3rd party (Portainer.io)         |
| registry                      | minikube   | disabled       | Google                           |
| registry-aliases              | minikube   | disabled       | 3rd party (unknown)              |
| registry-creds                | minikube   | disabled       | 3rd party (UPMC Enterprises)     |
| storage-provisioner           | minikube   | enabled ✅      | Google                           |
| storage-provisioner-gluster   | minikube   | disabled       | 3rd party (Gluster)              |
| volumesnapshots               | minikube   | disabled       | Kubernetes                       |
| ----------------------------- | ---------- | -------------- | -------------------------------- |

```

## Dashboard

```
$ minikube dashboard --port 20000
```

Output:

```
🤔  Verifying dashboard health ...
🚀  Launching proxy ...
🤔  Verifying proxy health ...
🎉  Opening http://127.0.0.1:20000/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/ in your default browser...
👉  http://127.0.0.1:20000/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/

```

### Remote access

```bash
$ kubectl proxy --address='0.0.0.0' --disable-filter=true
```

---
