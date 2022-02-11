# A Kubernetes Stack which Monitors your GitHub Repos
A quick start to stand-up a Kubernetes deployment for [Prometheus](http://prometheus.io/) stack containing Prometheus, Grafana, and  [github-exporter](https://github.com/infinityworksltd/github-exporter) to collect and graph GitHub statistics.

## Pre-requisites
Uses [kustomize](https://kustomize.io/) templates to define deployments. You need the `kubectl` tool to apply them to a Kubernetes cluster

## Installation
1. Clone the project

2. Modify `k8s/docker-secret.yaml`, `k8s/github-token-secret.yaml` and update them with your tokens for GitHub and docker. 

## How to update the list of repositories that are watched.

Update the values of `REPOS` on `k8s/metrics-env-configmap.yaml`