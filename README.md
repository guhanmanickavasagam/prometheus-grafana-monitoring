# prometheus-grafana-monitoring

Prometheus is configured to scrape metrics every 15 seconds.

Configuration file: /etc/prometheus/prometheus.yml

global:
  scrape_interval: 15s

scrape_configs:
  - job_name: prometheus
    static_configs:
      - targets: [localhost:9090]

  - job_name: node-exporter
    static_configs:
      - targets: [localhost:9100]

Scrape Targets

Prometheus: localhost:9090

Node Exporter: localhost:9100


