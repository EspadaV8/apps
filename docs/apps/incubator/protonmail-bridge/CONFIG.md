# protonmail-bridge

![Version: 1.4.3](https://img.shields.io/badge/Version-1.4.3-informational?style=flat-square) ![AppVersion: auto](https://img.shields.io/badge/AppVersion-auto-informational?style=flat-square)

Container for protonmail bridge to work on the network.

**Homepage:** <https://github.com/truechartsapps/tree/master/charts/incubator/protonmail-bridge>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| truecharts | info@truecharts.org | https://truecharts.org |

## Source Code

* <https://github.com/shenxn/protonmail-bridge-docker>
* <https://hub.docker.com/r/shenxn/protonmail-bridge>

## Requirements

Kubernetes: `>=1.16.0-0`

| Repository | Name | Version |
|------------|------|---------|
| https://truecharts.org | common | 6.8.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env | object | See below | environment variables. |
| env.TZ | string | `"UTC"` | Set the container timezone |
| image.pullPolicy | string | `"IfNotPresent"` | image pull policy |
| image.repository | string | `"shenxn/protonmail-bridge"` | image repository |
| image.tag | string | `"1.8.7-1"` | image tag |
| persistence | object | See values.yaml | Configure persistence settings for the chart under this key. |
| service | object | See values.yaml | Configures service settings for the chart. |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)