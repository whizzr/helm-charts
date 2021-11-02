# Helm chart usage
## Pre-requisites
Helm 3.4 CLI tool installed.
Ingress is supported but requires nginx-ingress to be installed and also cert-manager (if TLS is required)

## Installation
To enable Ingress edit the gke-values.yaml and ensure frontend.ingress.enabled = true.

```
kc create ns ob-demo
helm upgrade ob-demo . --values ./gke-values.yaml -i -n ob-demo
```
If Ingress is not enabled only a ClusterIP type service is created, so use kubefwd to port-forward:
`sudo -E kubefwd svc -n ob-demo`