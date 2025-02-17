
# blobscan

![Version: 0.2.5](https://img.shields.io/badge/Version-0.2.5-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

Blobscan is the first blockchain explorer that helps to navigate and visualize those EIP-4844 blobs

**Homepage:** <https://blobscan.com>

## Source Code

* <https://github.com/blobscan/blobscan/>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | blobscandb(postgresql) | 12.5.1 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | Affinity configuration for pods |
| annotations | object | `{}` | Annotations for the Deployment |
| args | list | `[]` | Command arguments |
| blobscandb.auth.database | string | `"blobscan"` |  |
| blobscandb.auth.password | string | `"postgres"` |  |
| blobscandb.auth.postgresPassword | string | `"postgres"` |  |
| blobscandb.auth.username | string | `"postgres"` |  |
| blobscandb.enabled | bool | `true` | If enabled a postgres chart will be deployed as a dependency |
| blobscandb.image.registry | string | `"docker.io"` |  |
| blobscandb.image.repository | string | `"bitnami/postgresql"` |  |
| blobscandb.image.tag | string | `"14.8.0"` |  |
| blobscandb.initdbScripts | object | See `values.yaml` | How to init the PSQL DB |
| blobscandb.persistence.enabled | bool | `true` |  |
| blobscandb.persistence.size | string | `"8Gi"` |  |
| blobscandb.pullPolicy | string | `"IfNotPresent"` |  |
| containerSecurityContext | object | See `values.yaml` | The security context for containers |
| customArgs | list | `["web"]` | Custom args for the blobscan container |
| customCommand | list | `[]` | Command replacement for the blobscan container |
| extraContainers | list | `[]` | Additional containers |
| extraEnv | list | `[{"name":"DATABASE_URL","value":"postgresql://postgres:postgres@blobscan-blobscandb:5432/blobscan?schema=public"},{"name":"SECRET_KEY","value":"supersecret"},{"name":"NEXT_PUBLIC_BEACON_BASE_URL","value":"http://134.209.87.158:8080/"},{"name":"NEXT_PUBLIC_EXPLORER_BASE_URL","value":"https://explorer.4844-devnet-6.ethpandaops.io/"}]` | Additional env variables |
| extraPodPorts | list | `[]` | Extra Pod ports |
| extraPorts | list | `[]` | Additional ports. Useful when using extraContainers |
| extraVolumeMounts | list | `[]` | Additional volume mounts |
| extraVolumes | list | `[]` | Additional volumes |
| fullnameOverride | string | `""` | Overrides the chart's computed fullname |
| httpPort | int | `3000` | Ports |
| image.pullPolicy | string | `"IfNotPresent"` | blobscan container pull policy |
| image.repository | string | `"blossomlabs/blobscan"` | blobscan container image repository |
| image.tag | string | `"next"` | blobscan container image tag |
| imagePullSecrets | list | `[]` | Image pull secrets for Docker images |
| ingress.annotations | object | `{}` | Annotations for Ingress |
| ingress.enabled | bool | `false` | Ingress resource for the HTTP API |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths | list | `[]` |  |
| ingress.tls | list | `[]` | Ingress TLS |
| initContainers | list | `[]` | Additional init containers |
| livenessProbe | object | See `values.yaml` | Liveness probe |
| nameOverride | string | `""` | Overrides the chart's name |
| nodeSelector | object | `{}` | Node selector for pods |
| podAnnotations | object | `{}` | Pod annotations |
| podDisruptionBudget | object | `{}` | Define the PodDisruptionBudget spec If not set then a PodDisruptionBudget will not be created |
| podLabels | object | `{}` | Pod labels |
| priorityClassName | string | `nil` | Pod priority class |
| readinessProbe | object | See `values.yaml` | Readiness probe |
| replicas | int | `1` | Number of replicas |
| resources | object | `{}` | Resource requests and limits |
| secretEnv | object | `{}` | Secret env variables injected via a created secret |
| securityContext | object | See `values.yaml` | The security context for pods |
| service.type | string | `"ClusterIP"` | Service type |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.create | bool | `false` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | The name of the service account to use. If not set and create is true, a name is generated using the fullname template |
| serviceMonitor.annotations | object | `{}` | Additional ServiceMonitor annotations |
| serviceMonitor.enabled | bool | `false` | If true, a ServiceMonitor CRD is created for a prometheus operator https://github.com/coreos/prometheus-operator |
| serviceMonitor.interval | string | `"15s"` | ServiceMonitor scrape interval |
| serviceMonitor.labels | object | `{}` | Additional ServiceMonitor labels |
| serviceMonitor.namespace | string | `nil` | Alternative namespace for ServiceMonitor |
| serviceMonitor.path | string | `"/metrics"` | Path to scrape |
| serviceMonitor.relabelings | list | `[]` | ServiceMonitor relabelings |
| serviceMonitor.scheme | string | `"http"` | ServiceMonitor scheme |
| serviceMonitor.scrapeTimeout | string | `"30s"` | ServiceMonitor scrape timeout |
| serviceMonitor.tlsConfig | object | `{}` | ServiceMonitor TLS configuration |
| terminationGracePeriodSeconds | int | `30` | How long to wait until the pod is forcefully terminated |
| tolerations | list | `[]` | Tolerations for pods |
| topologySpreadConstraints | list | `[]` | Topology Spread Constraints for pods |
