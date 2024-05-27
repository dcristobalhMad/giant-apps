# Project Documentation

This repository contains configuration files for various applications and cluster management within a Kubernetes environment. Below is a detailed description of the directory structure and the purpose of each file.

## Directory Structure

```plaintext
├── applications
│   ├── cluster-autoscaler
│   │   ├── servicemonitor.yaml
│   │   └── service.yaml
│   ├── flagger
│   │   └── flagger.yaml
│   ├── podinfo
│   │   └── podinfo.yaml
│   ├── port-scan-exporter
│   │   ├── cilium-network-policy.yaml
│   │   └── port-scan-exporter.yaml
│   ├── prometheus-operator
│   │   ├── disallow-kyverno-node-exporter.yaml
│   │   └── prometheus.yaml
│   └── tf-controller
│       └── tfcontroller.yaml
├── cluster
│   └── diegocristobal
│       ├── apps.yaml
│       ├── flux-system
│       │   ├── gotk-components.yaml
│       │   ├── gotk-sync.yaml
│       │   └── kustomization.yaml
│       └── namespaces.yaml
└── README.md
```

## Applications Directory

The `applications` directory contains the configuration files for various applications deployed in the Kubernetes cluster.

### cluster-autoscaler

- **servicemonitor.yaml**: Configuration for monitoring the cluster-autoscaler service.
- **service.yaml**: Service definition for the cluster-autoscaler.

### flagger

- **flagger.yaml**: Configuration file for deploying Flagger, a progressive delivery tool.

### podinfo

- **podinfo.yaml**: Deployment configuration for Podinfo, a tiny web application for Kubernetes.

### port-scan-exporter

- **cilium-network-policy.yaml**: Cilium network policy for the port-scan-exporter.
- **port-scan-exporter.yaml**: Deployment configuration for the port-scan-exporter.

### prometheus-operator

- **disallow-kyverno-node-exporter.yaml**: Policy to disallow certain operations by Kyverno on the node-exporter.
- **prometheus.yaml**: Configuration file for deploying Prometheus.

### tf-controller

- **tfcontroller.yaml**: Configuration file for the Terraform Controller.

## Cluster Directory

The `cluster` directory contains the configurations for managing the cluster itself.

### diegocristobal

This directory contains cluster-specific configurations managed by the user `diegocristobal`.

- **apps.yaml**: Aggregated application configurations for deployment in the cluster.
- **flux-system**: Directory containing Flux configuration files.
  - **gotk-components.yaml**: Defines the core components of the Flux GitOps toolkit.
  - **gotk-sync.yaml**: Synchronization settings for Flux.
  - **kustomization.yaml**: Kustomize configuration for managing resources.
- **namespaces.yaml**: Namespace definitions for organizing cluster resources.
