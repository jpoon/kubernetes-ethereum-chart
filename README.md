# kubernetes-ethereum-chart

Private Ethereum Network

## TL;DR;

```console
$ git clone git@github.com:jpoon/kubernetes-ethereum-chart.git
$ helm install --name ethereum kubernetes-ethereum-chart
```

## Introduction

This chart bootstraps a private [Ethereum](https://www.ethereum.org/) network on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager. This chart will provide DNS Services and can be deployed in multiple configuration to support various scenarios listed below:

## Prerequisites

* Kubernetes 1.8

## Installing the Chart

The chart can be installed as follows:

```console
$ git clone git@github.com:jpoon/kubernetes-ethereum-chart.git
$ helm install --name ethereum kubernetes-ethereum-chart
```

The command deploys a private Ethereum network on the Kubernetes cluster in the default configuration. The [configuration](#configuration) section lists various ways to override default configuration during deployment.

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
$ helm delete ethereum
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

See `values.yaml` for configuration notes. Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. For example,

```console
$ helm install --name ethereum \
  --set geth.networkid=98052 \
    kubernetes-ethereum-chart
```

The above command sets the networkId to 98052

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart. For example,

```console
$ helm install --name ethereum -f values.yaml kubernetes-ethereum-chart
```

> **Tip**: You can use the default [values.yaml](values.yaml)
