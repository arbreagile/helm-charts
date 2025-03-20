# Arbre Agile Helm repository

The **Arbre Agile Helm repository** contains kubernetes applications packaged by Arbre Agile.

Helm is a tool for managing Kubernetes charts. Charts are packages of pre-configured Kubernetes resources.

## Getting started

### Prerequisites
- Kubernetes 1.16+
- Helm 3

### Installing Helm

To install Helm, refer to the [Helm install guide](https://github.com/helm/helm#install) and ensure that the `helm` binary is in the `PATH` of your shell.

### Add Repository

The following command allows you to download and install all the charts from this repository:

```bash
$ helm repo add arbreagile https://helm.arbreagile.eu/
```

### Using Helm

To install an application: `helm install my-release arbreagile/<package-name>`, package-name can be found with `helm search repo` to view available chart packages.

To list installed applications: `helm list --all-namespaces --all`

And to upgrade an application: `helm upgrade my-release -n namespace`

Helm [Quick Start guide](https://helm.sh/docs/intro/using_helm/) provides detailed instructions on how to use the Helm client to manage packages on your Kubernetes cluster.

## Development

If you are looking for a way to contribute please read [CONTRIBUTING](CONTRIBUTING.md).

### Code of conduct

Participation in the Kubernetes community is governed by the [CNCF Code of Conduct](https://github.com/cncf/foundation/blob/master/code-of-conduct.md).

## Reach us

You can [raise an issue](https://github.com/arbreagile/helm-charts/issues/new) if you think you've found a bug.