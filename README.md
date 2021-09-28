# helm-charts

This repo serves as a Helm chart registry - uses a Git action to generate the tar.gz and Git pages to serve them.

## Usage
### Consuming charts

The following will add this repo as a new chart registry and list all the charts available in it
```
helm repo add whizzr https://whizzr.github.io/helm-charts/
helm repo update
helm search repo whizzr
```

### Adding updating charts
1. Add new charts into their own sub-dir under `charts`
1. Push/merge into main - a Github Action will take care of the rest

Hint: use this to only download the Helm chart in a repo containing other stuff: https://download-directory.github.io/