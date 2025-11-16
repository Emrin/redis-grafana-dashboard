# Redis Grafana Dashboard Helm Chart

This Helm chart automates provisioning the Opstree Redis Dashboard (Grafana ID 16056) as a ConfigMap, so it auto-imports via the kube-prometheus-stack sidecar. I built this for my Kubernetes monitoring stack with Redis Operator—saves manual Grafana UI steps!

## Installation
helm install redis-dashboard oci://ghcr.io/emrin/charts/redis-grafana-dashboard --version 0.1.0

## Prerequisites
- kube-prometheus-stack with sidecar enabled.
- Redis exporter metrics scraped.

## Customization
Override values like namespace or datasource in your values file.

Download the latest JSON from https://grafana.com/grafana/dashboards/16056 and place in `dashboards/` if needed.
