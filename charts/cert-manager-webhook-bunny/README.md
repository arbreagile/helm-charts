# Cert-Manager Webhook Bunny

Deploys the bunny cert-manager webhook.

![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v0.1.0](https://img.shields.io/badge/AppVersion-v0.1.0-informational?style=flat-square) ![ChartVersion: 0.1.0](https://img.shields.io/badge/ChartVersion-0.1.0-informational?style=flat-square)

## Installing the Chart

To install the chart with the release name `cert-manager-webhook-bunny` use the following:

```sh
helm upgrade --install cert-manager-webhook-bunny .
```

## Parameters

### Configuration

Configuration parameters.

| Name                             | Description                                            | Value                |
| -------------------------------- | ------------------------------------------------------ | -------------------- |
| `groupName`                      | Name under which the webhook will be available         | `acme.arbreagile.eu` |
| `certManager.namespace`          | Namespace under which cert-manager is installed        | `cert-manager`       |
| `certManager.serviceAccountName` | Name of the cert-manager service account               | `cert-manager`       |
| `pki.caDuration`                 | Webhook ca duration                                    | `43800h`             |
| `pki.servingCertificateDuration` | Webhook certificate duration                           | `8760h`              |
| `secret.apiKey`                  | Default bunny api key (optional)                       | `""`                 |
| `secret.name`                    | Secret name for the default bunny credentials          | `bunny-secret`       |
| `secret.externalSecretName`      | Existing secret name for the default bunny credentials | `""`                 |


### Common configuration

Common parameters.

| Name                     | Description                                                             | Value                                    |
| ------------------------ | ----------------------------------------------------------------------- | ---------------------------------------- |
| `nameOverride`           | Override charts name                                                    | `""`                                     |
| `fullnameOverride`       | Override charts and release name                                        | `""`                                     |
| `replicaCount`           | Number of replica                                                       | `1`                                      |
| `image.repository`       | Repository for the webhook image                                        | `arbreagile/cert-manager-webhook-bunny`  |
| `image.pullPolicy`       | Image pull policy                                                       | `IfNotPresent`                           |
| `image.imagePullSecrets` | Image pull secrets                                                      | `[]`                                     |
| `image.tag`              | Tag for the webhook image, defaults to AppVersion                       | `""`                                     |
| `extraEnv`               | Additional environment variables to pass to the webhook deployment      | `[]`                                     |
| `listenPort`             | Port the webhook listens on                                             | `443`                                    |
| `service.type`           | Service type exposing the webhook                                       | `ClusterIP`                              |
| `service.port`           | Service port exposing the webhook                                       | `443`                                    |
| `service.ipFamilyPolicy` | Service ipFamilyPolicy set the ip family policy to configure dual-stack | `""`                                     |
| `service.ipFamilies`     | Service ipFamilies. Can be IPv4 and/or IPv6.                            | `[]`                                     |
| `resources`              | Resources definition                                                    | `{}`                                     |
| `podLabels`              | Pod labels                                                              | `{}`                                     |
| `nodeSelector`           | Node selector                                                           | `{}`                                     |
| `tolerations`            | Tolerations                                                             | `[]`                                     |
| `affinity`               | Affinities                                                              | `{}`                                     |
| `securityContext`        | Container security context                                              | `{}`                                     |
| `podSecurityContext`     | Pod security context                                                    | `{}`                                     |
