# kube-monitoring-stack

## Overview

The purpose of this document is to install (deploy) a customized version of [kube-prometheus-stack](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack) to a desired Kubernetes cluster for monitoring the Kubernetes resources and the underlying infrastructure.

## Prerequisites

The following software is required to perform the installation:

- [git](https://git-scm.com/downloads)
- [Helm](https://helm.sh/docs/intro/install/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

**Warning:** kubectl must be configured to access the desired Kubernetes cluster before the installation.

## Installation

1. Clone the git repository of the monitoring stack:

```console
git clone git@github.com:yedaysal/kube-monitoring-stack.git
```

2. cd into the local repository directory:

```console
cd kube-monitoring-stack
```

3. Install the stack:

```console
helm install -n monitoring kube-monitoring-stack .
```

4. Run below `kubectl` command to verify the installation:

```console
kubectl get all -n monitoring ; kubectl get ingress -n monitoring
```

<br>

For more, please visit base repository [README](https://github.com/prometheus-community/helm-charts/blob/main/charts/kube-prometheus-stack/README.md).
