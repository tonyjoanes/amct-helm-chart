# Helm Chart Repository

## Chart Repo for Asset Manager Compliance Tool

### Setup

- Install Heml 3* (use chocolately or [helm install](https://helm.sh/docs/intro/install/))
- Add repo `helm repo add amctrepo https://tonyjoanes.github.io/amct-helm-chart`

### Add Charts

- Clone this repo
- Add charts to dir `./helm-chart-sources`
### Example create a test chart called db-test
```
cd helm-chart-sources
helm create db-test
```
Now package up the chart source
```
helm package helm-chart-sources/*
```
Now merge this into the [index.yaml](index.yaml) file using

```
heml repo index --url https://tonyjoanes.github.io/amct-helm-chart --merge index.yaml
```
