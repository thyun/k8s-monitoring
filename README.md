# Kubernetes Monitoring
This project is based on https://github.com/Thakurvaibhav/k8s/tree/master/monitoring

# Monitoring
## Setup container
- kubectl apply -f namespace.yaml
- kubectl apply -f dashboard; kubectl apply -f prometheus; kubectl apply -f alertmanager; kubectl apply -f grafana
- kubectl apply -f kube-state-metrics
 	
## Setup access
- kubectl apply -f ingress
- Modify OS hosts file
  - Location of hosts file: MacOS - /etc/hosts, Windows - C:\Windows\System32\drivers\etc\hosts
  - ex) 192.168.99.100 mini-plab.com

## Setup grafana
    - Access grafana at grafana.yourdomain.com
    - Add DataSource: 
 	  - Name: DS_PROMETHEUS
 	  - Type: Prometheus 
 	  - URL: http://prometheus:8080 
 	- Import dashboards from grafana/dashboards-k8s, grafana/dashboards-elasticsearch-metrics

## How to access
- http://prometheus.mini-plab.com
- http://alertmanager.mini-plab.com
- http://grafana.mini-plab.com

# Tool
- http://kibana.mini-plab.com
- http://kafka-manager.mini-plab.com

# Old
- Node-Exporter: kubectl apply -f k8s/monitoring/node-exporter

