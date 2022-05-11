# oxidized

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

oxidized helm package

**This chart is not maintained by the upstream project and any issues with the chart should be raised [here](https://github.com/nicko170/charts/issues/new/choose)**

## Source Code

* <https://github.com/ytti/oxidized>

## Requirements

Kubernetes: `>=1.16.0-0`

## Dependencies

| Repository | Name | Version |
|------------|------|---------|
| https://library-charts.k8s-at-home.com | common | 4.3.0   |

## TL;DR

```console
helm repo add nicko170 https://charts.nicko170.au/
helm repo update
helm install oxidized nicko170/oxidized
```

## Installing the Chart

To install the chart with the release name `oxidized`

```console
helm install oxidized nicko170/oxidized
```

## Uninstalling the Chart

To uninstall the `oxidized` deployment

```console
helm uninstall oxidized
```

The command removes all the Kubernetes components associated with the chart **including persistent volumes** and deletes the release.

## Configuration

Read through the [values.yaml](./values.yaml) file. It has several commented out suggested values.
Other values may be used from the [values.yaml](https://github.com/k8s-at-home/library-charts/tree/main/charts/stable/common/values.yaml) from the [common library](https://github.com/k8s-at-home/library-charts/tree/main/charts/stable/common).

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

```console
helm install oxidized \
  --set env.TZ="America/New York" \
    nicko170/oxidized
```

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart.

```console
helm install oxidized k8s-at-home/oxidized -f values.yaml
```

## Custom configuration

N/A

## Values

**Important**: When deploying an application Helm chart you can add more values from our common library chart [here](https://github.com/k8s-at-home/library-charts/tree/main/charts/stable/common)

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env | object | See below | environment variables. See more environment variables in the [oxidized documentation](https://oxidized.org/docs). |
| env.TZ | string | `"UTC"` | Set the container timezone |
| image.pullPolicy | string | `"IfNotPresent"` | image pull policy |
| image.repository | string | `"oxidized/oxidized"` | image repository |
| image.tag | string | `"1.0.0"` | image tag |
| ingress.main | object | See values.yaml | Enable and configure ingress settings for the chart under this key. |
| persistence | object | See values.yaml | Configure persistence settings for the chart under this key. |
| service | object | See values.yaml | Configures service settings for the chart. |

## Changelog

### Version 1.0.0

#### Added

- Initial version

#### Changed

N/A

#### Fixed

N/A

## Support

- See the [Docs](https://docs.k8s-at-home.com/our-helm-charts/getting-started/)
- Open an [issue](https://github.com/k8s-at-home/charts/issues/new/choose)
- Ask a [question](https://github.com/k8s-at-home/organization/discussions)
- Join our [Discord](https://discord.gg/sTMX7Vh) community
