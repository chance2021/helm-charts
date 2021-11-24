# helm-charts
Helm Charts Repository for VRE

## Usage

### Creating a new chart
```bash
helm create mychart
```

### Publishing a chart
```bash
helm package mychart # will use version defined in chart
mv mychart-x.y.z.tgz docs # move it to the github pages folder
helm repo index docs --url https://virtualresearchenvironment.github.io/helm-charts/ # build index file for helm repository
```

### Using a chart from the git repo repo
```bash
helm install deployment-name ./mychart
```

### Using a chart from the helm repository
```bash
helm repo add vre https://virtualresearchenvironment.github.io/helm-charts/
helm install deployment-name vre/mychart
```