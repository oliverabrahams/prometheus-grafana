# prometheus-grafana
This is a simple prometheus and grafana application stack

# Setup
First clone the repo.

Change the target of prometheus to your metrics endpoint. in ./prometheus/prometheus.yml
```yaml
scrape_configs:
  - job_name: *job-name
    static_configs:
      - targets: [*'host.docker.internal:4100']
```

ou need to have Docker Engine and Docker Compose on your machine.

You can either:

Install Docker Engine and Docker Compose as standalone binaries.

Install Docker Desktop which includes both Docker Engine and Docker Compose
https://docs.docker.com/compose/gettingstarted/

# Usage
To start navigate to the directory and run
```shell
docker compose up
```

To stop navigate to the directory and run
```shell
docker compose down
```


http://localhost:9090/ will show prometheus running on you machine

http://localhost:3000/ will show graphana running on you machine
