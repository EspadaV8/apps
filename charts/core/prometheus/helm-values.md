# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| alertmanager.additionalPeers | list | `[]` |  |
| alertmanager.affinity | object | `{}` |  |
| alertmanager.config.global.resolve_timeout | string | `"5m"` |  |
| alertmanager.config.receivers[0].name | string | `"null"` |  |
| alertmanager.config.route.group_by[0] | string | `"job"` |  |
| alertmanager.config.route.group_interval | string | `"5m"` |  |
| alertmanager.config.route.group_wait | string | `"30s"` |  |
| alertmanager.config.route.receiver | string | `"null"` |  |
| alertmanager.config.route.repeat_interval | string | `"12h"` |  |
| alertmanager.config.route.routes[0].match.alertname | string | `"Watchdog"` |  |
| alertmanager.config.route.routes[0].receiver | string | `"null"` |  |
| alertmanager.configMaps | list | `[]` |  |
| alertmanager.configNamespaceSelector | object | `{}` |  |
| alertmanager.configSelector | object | `{}` |  |
| alertmanager.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| alertmanager.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| alertmanager.containerSecurityContext.enabled | bool | `true` |  |
| alertmanager.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| alertmanager.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| alertmanager.containers | list | `[]` |  |
| alertmanager.enabled | bool | `true` |  |
| alertmanager.externalConfig | bool | `false` |  |
| alertmanager.externalUrl | string | `""` |  |
| alertmanager.listenLocal | bool | `false` |  |
| alertmanager.livenessProbe.enabled | bool | `true` |  |
| alertmanager.livenessProbe.failureThreshold | int | `120` |  |
| alertmanager.livenessProbe.initialDelaySeconds | int | `0` |  |
| alertmanager.livenessProbe.path | string | `"/-/healthy"` |  |
| alertmanager.livenessProbe.periodSeconds | int | `5` |  |
| alertmanager.livenessProbe.successThreshold | int | `1` |  |
| alertmanager.livenessProbe.timeoutSeconds | int | `3` |  |
| alertmanager.logFormat | string | `"logfmt"` |  |
| alertmanager.logLevel | string | `"info"` |  |
| alertmanager.nodeAffinityPreset.key | string | `""` |  |
| alertmanager.nodeAffinityPreset.type | string | `""` |  |
| alertmanager.nodeAffinityPreset.values | list | `[]` |  |
| alertmanager.nodeSelector | object | `{}` |  |
| alertmanager.paused | bool | `false` |  |
| alertmanager.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| alertmanager.persistence.enabled | bool | `true` |  |
| alertmanager.persistence.size | string | `"999Gi"` |  |
| alertmanager.persistence.storageClass | string | `""` |  |
| alertmanager.podAffinityPreset | string | `""` |  |
| alertmanager.podAntiAffinityPreset | string | `"soft"` |  |
| alertmanager.podDisruptionBudget.enabled | bool | `false` |  |
| alertmanager.podDisruptionBudget.maxUnavailable | string | `""` |  |
| alertmanager.podDisruptionBudget.minAvailable | int | `1` |  |
| alertmanager.podMetadata.annotations | object | `{}` |  |
| alertmanager.podMetadata.labels | object | `{}` |  |
| alertmanager.podSecurityContext.enabled | bool | `true` |  |
| alertmanager.podSecurityContext.fsGroup | int | `1001` |  |
| alertmanager.podSecurityContext.runAsUser | int | `1001` |  |
| alertmanager.portName | string | `"alertmanager"` |  |
| alertmanager.priorityClassName | string | `""` |  |
| alertmanager.readinessProbe.enabled | bool | `true` |  |
| alertmanager.readinessProbe.failureThreshold | int | `120` |  |
| alertmanager.readinessProbe.initialDelaySeconds | int | `0` |  |
| alertmanager.readinessProbe.path | string | `"/-/ready"` |  |
| alertmanager.readinessProbe.periodSeconds | int | `5` |  |
| alertmanager.readinessProbe.successThreshold | int | `1` |  |
| alertmanager.readinessProbe.timeoutSeconds | int | `3` |  |
| alertmanager.replicaCount | int | `1` |  |
| alertmanager.resources | object | `{}` |  |
| alertmanager.retention | string | `"240h"` |  |
| alertmanager.routePrefix | string | `"/"` |  |
| alertmanager.secrets | list | `[]` |  |
| alertmanager.serviceAccount.create | bool | `true` |  |
| alertmanager.serviceAccount.name | string | `""` |  |
| alertmanager.serviceMonitor.enabled | bool | `true` |  |
| alertmanager.serviceMonitor.interval | string | `""` |  |
| alertmanager.serviceMonitor.metricRelabelings | list | `[]` |  |
| alertmanager.serviceMonitor.relabelings | list | `[]` |  |
| alertmanager.storageSpec | object | `{}` |  |
| alertmanager.tolerations | list | `[]` |  |
| alertmanager.volumeMounts | list | `[]` |  |
| alertmanager.volumes | list | `[]` |  |
| alertmanagerImage.repository | string | `"bitnami/alertmanager"` |  |
| alertmanagerImage.tag | string | `"0.23.0"` |  |
| coreDns.enabled | bool | `true` |  |
| coreDns.namespace | string | `"kube-system"` |  |
| coreDns.service.enabled | bool | `true` |  |
| coreDns.service.port | int | `9153` |  |
| coreDns.service.selector | object | `{}` |  |
| coreDns.service.targetPort | int | `9153` |  |
| coreDns.serviceMonitor.interval | string | `""` |  |
| coreDns.serviceMonitor.metricRelabelings | list | `[]` |  |
| coreDns.serviceMonitor.relabelings | list | `[]` |  |
| envValueFrom.PROMETHEUS_CONFIG_RELOADER.configMapKeyRef.key | string | `"prometheus-config-reloader"` |  |
| envValueFrom.PROMETHEUS_CONFIG_RELOADER.configMapKeyRef.name | string | `"prometheus-operator-config"` |  |
| exporters.kube-state-metrics.enabled | bool | `true` |  |
| exporters.node-exporter.enabled | bool | `true` |  |
| global.labels | object | `{}` |  |
| image.repository | string | `"bitnami/prometheus-operator"` |  |
| image.tag | string | `"0.52.1"` |  |
| ingress.alertmanager.enabled | bool | `false` |  |
| ingress.main.enabled | bool | `false` |  |
| ingress.thanos.enabled | bool | `false` |  |
| kube-state-metrics.serviceMonitor.enabled | bool | `true` |  |
| kube-state-metrics.serviceMonitor.honorLabels | bool | `true` |  |
| kubeApiServer.enabled | bool | `true` |  |
| kubeApiServer.serviceMonitor.interval | string | `""` |  |
| kubeApiServer.serviceMonitor.metricRelabelings | list | `[]` |  |
| kubeApiServer.serviceMonitor.relabelings | list | `[]` |  |
| kubeControllerManager.enabled | bool | `false` |  |
| kubeControllerManager.endpoints | list | `[]` |  |
| kubeControllerManager.namespace | string | `"kube-system"` |  |
| kubeControllerManager.service.enabled | bool | `true` |  |
| kubeControllerManager.service.port | int | `10252` |  |
| kubeControllerManager.service.selector | object | `{}` |  |
| kubeControllerManager.service.targetPort | int | `10252` |  |
| kubeControllerManager.serviceMonitor.https | bool | `false` |  |
| kubeControllerManager.serviceMonitor.insecureSkipVerify | string | `""` |  |
| kubeControllerManager.serviceMonitor.interval | string | `""` |  |
| kubeControllerManager.serviceMonitor.metricRelabelings | list | `[]` |  |
| kubeControllerManager.serviceMonitor.relabelings | list | `[]` |  |
| kubeControllerManager.serviceMonitor.serverName | string | `""` |  |
| kubeProxy.enabled | bool | `false` |  |
| kubeScheduler.enabled | bool | `false` |  |
| kubeScheduler.endpoints | list | `[]` |  |
| kubeScheduler.namespace | string | `"kube-system"` |  |
| kubeScheduler.service.enabled | bool | `true` |  |
| kubeScheduler.service.port | int | `10251` |  |
| kubeScheduler.service.selector | object | `{}` |  |
| kubeScheduler.service.targetPort | int | `10251` |  |
| kubeScheduler.serviceMonitor.https | bool | `false` |  |
| kubeScheduler.serviceMonitor.insecureSkipVerify | string | `""` |  |
| kubeScheduler.serviceMonitor.interval | string | `""` |  |
| kubeScheduler.serviceMonitor.metricRelabelings | list | `[]` |  |
| kubeScheduler.serviceMonitor.relabelings | list | `[]` |  |
| kubeScheduler.serviceMonitor.serverName | string | `""` |  |
| kubelet.enabled | bool | `true` |  |
| kubelet.namespace | string | `"kube-system"` |  |
| kubelet.serviceMonitor.cAdvisorMetricRelabelings | list | `[]` |  |
| kubelet.serviceMonitor.cAdvisorRelabelings | list | `[]` |  |
| kubelet.serviceMonitor.https | bool | `true` |  |
| kubelet.serviceMonitor.interval | string | `""` |  |
| kubelet.serviceMonitor.metricRelabelings | list | `[]` |  |
| kubelet.serviceMonitor.relabelings | list | `[]` |  |
| node-exporter.extraArgs."collector.filesystem.ignored-fs-types" | string | `"^(autofs|binfmt_misc|cgroup|configfs|debugfs|devpts|devtmpfs|fusectl|hugetlbfs|mqueue|overlay|proc|procfs|pstore|rpc_pipefs|securityfs|sysfs|tracefs)$"` |  |
| node-exporter.extraArgs."collector.filesystem.ignored-mount-points" | string | `"^/(dev|proc|sys|var/lib/docker/.+)($|/)"` |  |
| node-exporter.service.labels.jobLabel | string | `"node-exporter"` |  |
| node-exporter.serviceMonitor.enabled | bool | `true` |  |
| node-exporter.serviceMonitor.jobLabel | string | `"jobLabel"` |  |
| operator.configReloaderResources | object | `{}` |  |
| operator.enabled | bool | `true` |  |
| operator.kubeletService.enabled | bool | `true` |  |
| operator.kubeletService.namespace | string | `"kube-system"` |  |
| operator.logFormat | string | `"logfmt"` |  |
| operator.logLevel | string | `"info"` |  |
| operator.prometheusConfigReloader.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| operator.prometheusConfigReloader.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| operator.prometheusConfigReloader.containerSecurityContext.enabled | bool | `true` |  |
| operator.prometheusConfigReloader.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| operator.prometheusConfigReloader.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| operator.prometheusConfigReloader.livenessProbe.enabled | bool | `true` |  |
| operator.prometheusConfigReloader.livenessProbe.failureThreshold | int | `6` |  |
| operator.prometheusConfigReloader.livenessProbe.initialDelaySeconds | int | `10` |  |
| operator.prometheusConfigReloader.livenessProbe.periodSeconds | int | `10` |  |
| operator.prometheusConfigReloader.livenessProbe.successThreshold | int | `1` |  |
| operator.prometheusConfigReloader.livenessProbe.timeoutSeconds | int | `5` |  |
| operator.prometheusConfigReloader.readinessProbe.enabled | bool | `true` |  |
| operator.prometheusConfigReloader.readinessProbe.failureThreshold | int | `6` |  |
| operator.prometheusConfigReloader.readinessProbe.initialDelaySeconds | int | `15` |  |
| operator.prometheusConfigReloader.readinessProbe.periodSeconds | int | `20` |  |
| operator.prometheusConfigReloader.readinessProbe.successThreshold | int | `1` |  |
| operator.prometheusConfigReloader.readinessProbe.timeoutSeconds | int | `5` |  |
| operator.serviceMonitor.enabled | bool | `true` |  |
| operator.serviceMonitor.interval | string | `""` |  |
| operator.serviceMonitor.metricRelabelings | list | `[]` |  |
| operator.serviceMonitor.relabelings | list | `[]` |  |
| probes.liveness | object | See below | Liveness probe configuration |
| probes.readiness | object | See below | Redainess probe configuration |
| probes.startup | object | See below | Startup probe configuration |
| prometheus.additionalAlertRelabelConfigsExternal.enabled | bool | `false` |  |
| prometheus.additionalAlertRelabelConfigsExternal.key | string | `""` |  |
| prometheus.additionalAlertRelabelConfigsExternal.name | string | `""` |  |
| prometheus.additionalPrometheusRules | list | `[]` |  |
| prometheus.additionalScrapeConfigs.enabled | bool | `false` |  |
| prometheus.additionalScrapeConfigs.external.key | string | `""` |  |
| prometheus.additionalScrapeConfigs.external.name | string | `""` |  |
| prometheus.additionalScrapeConfigs.internal.jobList | list | `[]` |  |
| prometheus.additionalScrapeConfigs.type | string | `"external"` |  |
| prometheus.additionalScrapeConfigsExternal.enabled | bool | `false` |  |
| prometheus.additionalScrapeConfigsExternal.key | string | `""` |  |
| prometheus.additionalScrapeConfigsExternal.name | string | `""` |  |
| prometheus.affinity | object | `{}` |  |
| prometheus.alertingEndpoints | list | `[]` |  |
| prometheus.configMaps | list | `[]` |  |
| prometheus.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| prometheus.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| prometheus.containerSecurityContext.enabled | bool | `true` |  |
| prometheus.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| prometheus.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| prometheus.containers | list | `[]` |  |
| prometheus.disableCompaction | bool | `false` |  |
| prometheus.enableAdminAPI | bool | `false` |  |
| prometheus.enableFeatures | list | `[]` |  |
| prometheus.enabled | bool | `true` |  |
| prometheus.evaluationInterval | string | `""` |  |
| prometheus.externalLabels | object | `{}` |  |
| prometheus.externalUrl | string | `""` |  |
| prometheus.listenLocal | bool | `false` |  |
| prometheus.livenessProbe.enabled | bool | `true` |  |
| prometheus.livenessProbe.failureThreshold | int | `10` |  |
| prometheus.livenessProbe.initialDelaySeconds | int | `0` |  |
| prometheus.livenessProbe.path | string | `"/-/healthy"` |  |
| prometheus.livenessProbe.periodSeconds | int | `10` |  |
| prometheus.livenessProbe.successThreshold | int | `1` |  |
| prometheus.livenessProbe.timeoutSeconds | int | `3` |  |
| prometheus.logFormat | string | `"logfmt"` |  |
| prometheus.logLevel | string | `"info"` |  |
| prometheus.matchLabels | object | `{}` |  |
| prometheus.nodeAffinityPreset.key | string | `""` |  |
| prometheus.nodeAffinityPreset.type | string | `""` |  |
| prometheus.nodeAffinityPreset.values | list | `[]` |  |
| prometheus.nodeSelector | object | `{}` |  |
| prometheus.paused | bool | `false` |  |
| prometheus.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| prometheus.persistence.enabled | bool | `true` |  |
| prometheus.persistence.size | string | `"999Gi"` |  |
| prometheus.persistence.storageClass | string | `""` |  |
| prometheus.podAffinityPreset | string | `""` |  |
| prometheus.podAntiAffinityPreset | string | `"soft"` |  |
| prometheus.podMetadata.annotations | object | `{}` |  |
| prometheus.podMetadata.labels | object | `{}` |  |
| prometheus.podMonitorNamespaceSelector | object | `{}` |  |
| prometheus.podMonitorSelector | object | `{}` |  |
| prometheus.podSecurityContext.enabled | bool | `true` |  |
| prometheus.podSecurityContext.fsGroup | int | `1001` |  |
| prometheus.podSecurityContext.runAsUser | int | `1001` |  |
| prometheus.portName | string | `"main"` |  |
| prometheus.priorityClassName | string | `""` |  |
| prometheus.probeNamespaceSelector | object | `{}` |  |
| prometheus.probeSelector | object | `{}` |  |
| prometheus.prometheusExternalLabelName | string | `""` |  |
| prometheus.prometheusExternalLabelNameClear | bool | `false` |  |
| prometheus.querySpec | object | `{}` |  |
| prometheus.readinessProbe.enabled | bool | `true` |  |
| prometheus.readinessProbe.failureThreshold | int | `10` |  |
| prometheus.readinessProbe.initialDelaySeconds | int | `0` |  |
| prometheus.readinessProbe.path | string | `"/-/ready"` |  |
| prometheus.readinessProbe.periodSeconds | int | `10` |  |
| prometheus.readinessProbe.successThreshold | int | `1` |  |
| prometheus.readinessProbe.timeoutSeconds | int | `3` |  |
| prometheus.remoteRead | list | `[]` |  |
| prometheus.remoteWrite | list | `[]` |  |
| prometheus.replicaCount | int | `1` |  |
| prometheus.replicaExternalLabelName | string | `""` |  |
| prometheus.replicaExternalLabelNameClear | bool | `false` |  |
| prometheus.resources | object | `{}` |  |
| prometheus.retention | string | `"31d"` |  |
| prometheus.retentionSize | string | `""` |  |
| prometheus.routePrefix | string | `"/"` |  |
| prometheus.ruleNamespaceSelector | object | `{}` |  |
| prometheus.ruleSelector | object | `{}` |  |
| prometheus.scrapeInterval | string | `""` |  |
| prometheus.secrets | list | `[]` |  |
| prometheus.serviceAccount.annotations | object | `{}` |  |
| prometheus.serviceAccount.create | bool | `true` |  |
| prometheus.serviceAccount.name | string | `""` |  |
| prometheus.serviceMonitor.enabled | bool | `true` |  |
| prometheus.serviceMonitor.interval | string | `""` |  |
| prometheus.serviceMonitor.metricRelabelings | list | `[]` |  |
| prometheus.serviceMonitor.relabelings | list | `[]` |  |
| prometheus.serviceMonitorNamespaceSelector | object | `{}` |  |
| prometheus.serviceMonitorSelector | object | `{}` |  |
| prometheus.storageSpec | object | `{}` |  |
| prometheus.thanos.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| prometheus.thanos.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| prometheus.thanos.containerSecurityContext.enabled | bool | `true` |  |
| prometheus.thanos.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| prometheus.thanos.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| prometheus.thanos.create | bool | `false` |  |
| prometheus.thanos.extraArgs | list | `[]` |  |
| prometheus.thanos.extraVolumeMounts | list | `[]` |  |
| prometheus.thanos.livenessProbe.enabled | bool | `true` |  |
| prometheus.thanos.livenessProbe.failureThreshold | int | `120` |  |
| prometheus.thanos.livenessProbe.initialDelaySeconds | int | `0` |  |
| prometheus.thanos.livenessProbe.path | string | `"/-/healthy"` |  |
| prometheus.thanos.livenessProbe.periodSeconds | int | `5` |  |
| prometheus.thanos.livenessProbe.successThreshold | int | `1` |  |
| prometheus.thanos.livenessProbe.timeoutSeconds | int | `3` |  |
| prometheus.thanos.objectStorageConfig | object | `{}` |  |
| prometheus.thanos.prometheusUrl | string | `""` |  |
| prometheus.thanos.readinessProbe.enabled | bool | `true` |  |
| prometheus.thanos.readinessProbe.failureThreshold | int | `120` |  |
| prometheus.thanos.readinessProbe.initialDelaySeconds | int | `0` |  |
| prometheus.thanos.readinessProbe.path | string | `"/-/ready"` |  |
| prometheus.thanos.readinessProbe.periodSeconds | int | `5` |  |
| prometheus.thanos.readinessProbe.successThreshold | int | `1` |  |
| prometheus.thanos.readinessProbe.timeoutSeconds | int | `3` |  |
| prometheus.thanos.resources.limits | object | `{}` |  |
| prometheus.thanos.resources.requests | object | `{}` |  |
| prometheus.thanos.service.annotations | object | `{}` |  |
| prometheus.thanos.service.clusterIP | string | `"None"` |  |
| prometheus.thanos.service.extraPorts | list | `[]` |  |
| prometheus.thanos.service.loadBalancerIP | string | `""` |  |
| prometheus.thanos.service.loadBalancerSourceRanges | list | `[]` |  |
| prometheus.thanos.service.nodePort | string | `""` |  |
| prometheus.thanos.service.port | int | `10901` |  |
| prometheus.thanos.service.type | string | `"ClusterIP"` |  |
| prometheus.tolerations | list | `[]` |  |
| prometheus.volumeMounts | list | `[]` |  |
| prometheus.volumes | list | `[]` |  |
| prometheus.walCompression | bool | `false` |  |
| prometheusImage.repository | string | `"bitnami/prometheus"` |  |
| prometheusImage.tag | string | `"2.31.1"` |  |
| rbac | object | `{"enabled":true,"rules":[{"apiGroups":["apiextensions.k8s.io"],"resources":["customresourcedefinitions"],"verbs":["create"]},{"apiGroups":["apiextensions.k8s.io"],"resourceNames":["alertmanagers.monitoring.coreos.com","podmonitors.monitoring.coreos.com","prometheuses.monitoring.coreos.com","prometheusrules.monitoring.coreos.com","servicemonitors.monitoring.coreos.com","thanosrulers.monitoring.coreos.com","probes.monitoring.coreos.com"],"resources":["customresourcedefinitions"],"verbs":["get","update"]},{"apiGroups":["monitoring.coreos.com"],"resources":["alertmanagers","alertmanagers/finalizers","alertmanagerconfigs","prometheuses","prometheuses/finalizers","thanosrulers","thanosrulers/finalizers","servicemonitors","podmonitors","probes","prometheusrules"],"verbs":["*"]},{"apiGroups":["apps"],"resources":["statefulsets"],"verbs":["*"]},{"apiGroups":[""],"resources":["configmaps","secrets"],"verbs":["*"]},{"apiGroups":[""],"resources":["pods"],"verbs":["list","delete"]},{"apiGroups":[""],"resources":["services","services/finalizers","endpoints"],"verbs":["get","create","update","delete"]},{"apiGroups":[""],"resources":["nodes"],"verbs":["list","watch"]},{"apiGroups":[""],"resources":["namespaces"],"verbs":["get","list","watch"]},{"apiGroups":["networking.k8s.io"],"resources":["ingresses"],"verbs":["get","list","watch"]}]}` | Whether Role Based Access Control objects like roles and rolebindings should be created |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| service.alertmanager.enabled | bool | `true` |  |
| service.alertmanager.ports.alertmanager.enabled | bool | `true` |  |
| service.alertmanager.ports.alertmanager.port | int | `10087` |  |
| service.alertmanager.ports.alertmanager.protocol | string | `"HTTP"` |  |
| service.alertmanager.ports.alertmanager.targetPort | int | `9093` |  |
| service.alertmanager.selector."app.kubernetes.io/name" | string | `"alertmanager"` |  |
| service.alertmanager.selector.alertmanager | string | `"{{ template \"kube-prometheus.alertmanager.fullname\" . }}"` |  |
| service.main.ports.main.port | int | `10086` |  |
| service.main.ports.main.protocol | string | `"HTTP"` |  |
| service.main.ports.main.targetPort | int | `9090` |  |
| service.main.selector."app.kubernetes.io/name" | string | `"prometheus"` |  |
| service.main.selector.prometheus | string | `"{{ template \"kube-prometheus.prometheus.fullname\" . }}"` |  |
| service.promop.enabled | bool | `true` |  |
| service.promop.ports.promop.enabled | bool | `true` |  |
| service.promop.ports.promop.port | int | `10089` |  |
| service.promop.ports.promop.protocol | string | `"HTTP"` |  |
| service.promop.ports.promop.targetPort | int | `8080` |  |
| service.thanos.enabled | bool | `true` |  |
| service.thanos.ports.thanos.enabled | bool | `true` |  |
| service.thanos.ports.thanos.port | int | `10901` |  |
| service.thanos.ports.thanos.protocol | string | `"HTTP"` |  |
| service.thanos.ports.thanos.targetPort | int | `10901` |  |
| service.thanos.selector."app.kubernetes.io/name" | string | `"prometheus"` |  |
| service.thanos.selector.prometheus | string | `"{{ template \"kube-prometheus.prometheus.fullname\" . }}"` |  |
| serviceAccount | object | `{"create":true}` | The service account the pods will use to interact with the Kubernetes API |
| thanosImage.repository | string | `"bitnami/thanos"` |  |
| thanosImage.tag | string | `"0.23.1"` |  |

All Rights Reserved - The TrueCharts Project