# Helm Chart

This Helm chart is a lightweight way to configure and run the following stack:
- Elasticsearch
- Kibana
- APM Server
- Logstash
- Metricbeat
- App Demo microservices
    - Adapter
    - Composite 
    - Core

### Deploying
```
helm install demoapp demoapp-0.2.0-ITX.tgz
```

### Requirements

- [Helm](https://helm.sh/docs/intro/install/) 
- [kubectl](https://kubernetes.io/es/docs/tasks/tools/install-kubectl/) 

By default Helm runs the chart against your local .kube/config. Your config should be pointing the kubernetes cluster
