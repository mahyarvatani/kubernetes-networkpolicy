# kubernetes-networkpolicy
# Kubernetes Network Policy Project

## Overview

This Kubernetes project demonstrates the use of Network Policies to control communication between two deployments (`nginx1` and `nginx2`) deployed in separate namespaces (`namespace1` and `namespace2`). The project aims to achieve the following:

1. Allow `nginx1` to curl `nginx2`.
2. Prevent `nginx2` from curling `nginx1`.
3. Block ping access from `nginx1` to `nginx2`.
4. Create services (`sns1` and `sns2`) for `nginx1` and `nginx2` respectively.
5. `nginx1` is located in `ns1` and `nginx2` is located in `ns2`

## Prerequisites

Before running this Kubernetes project, make sure you have the following prerequisites:

1. A running Kubernetes cluster.
2. `kubectl` installed and configured to communicate with your Kubernetes cluster.

## Project Structure

```plaintext
.
├── k8s/
│   ├── namespaces/
│   │   ├── ns1.yaml
│   │   └── ns2.yaml
│   ├── deployments/
│   │   ├── nginx1.yaml
│   │   └── nginx2.yaml
│   ├── services/
│   │   ├── sns1.yaml
│   │   └── sns2.yaml
│   └── network-policies/
│       ├── networkpolicy-allow80.yaml
│       └── networkpolicy-denyall.yaml
├── README.md
└── .gitignore
