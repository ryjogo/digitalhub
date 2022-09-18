# phpipam

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.5x](https://img.shields.io/badge/AppVersion-1.5x-informational?style=flat-square)

A Helm chart for phpIpam - Open source IP address management

**Homepage:** <https://phpipam.net/>

## Source Code

* <https://github.com/phpipam/phpipam>

## Usage

[Helm](https://helm.sh) must be installed to use the charts. Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

    helm repo add digitalhub https://ryjogo.github.io/digitalhub

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages. You can then run `helm search repo digitalhub` to see the charts.

To install the phpipam chart:

    helm install my-phpipam digitalhub/phpipam

To uninstall the chart:

    helm delete my-phpipam

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| database.database | string | `"phpipam"` |  |
| database.existingSecret | string | `""` |  |
| database.hostname | string | `"localhost"` |  |
| database.password | string | `"pass"` |  |
| database.port | string | `"3306"` |  |
| database.username | string | `"user"` |  |
| extraEnv[0].name | string | `"IPAM_DEBUG"` |  |
| extraEnv[0].value | string | `"true"` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"phpipam/phpipam-www"` |  |
| image.tag | string | `"latest"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| phpipamCron.extraEnv[0].name | string | `"SCAN_INTERVAL"` |  |
| phpipamCron.extraEnv[0].value | string | `"1h"` |  |
| phpipamCron.image.pullPolicy | string | `"IfNotPresent"` |  |
| phpipamCron.image.repository | string | `"phpipam/phpipam-cron"` |  |
| phpipamCron.image.tag | string | `"latest"` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `2` |  |
| resources | object | `{}` |  |
| securityContext.allowPrivilegeEscalation | bool | `true` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |