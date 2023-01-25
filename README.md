# prometheus-grafana
This is a simple prometheus and grafana application stack

# Usage
First clone the repo.

Change the target of prometheus to your metrics endpoint. in ./prometheus/prometheus.yml
```yaml
  - job_name: *job-name
    static_configs:
      - targets: [*'host.docker.internal:4100']
```

Navigate to the directory and run
```shell
docker compose up
```

http://localhost:9090/ will show prometheus running on you machine

http://localhost:3000/ will show graphana running on you machine
