## Monitoring Setup (Classwork 1)

### New Branch
This task was completed on the `monitoring` branch.

### Services Added
The `docker-compose.yml` was updated to include the following monitoring services:

- **Prometheus** (port 9090) — scrapes and stores metrics from the app and blackbox
- **Blackbox Exporter** (port 9115) — probes the Hello World app endpoint to check availability
- **Grafana** (port 3001) — visualizes metrics from Prometheus via dashboards

### Running Containers
All five containers running together:

| Container | Port | Purpose |
|---|---|---|
| app | 3000 | Hello World Express app |
| prometheus | 9090 | Metrics collection |
| blackbox | 9115 | Endpoint health probing |
| grafana | 3001 | Metrics visualization |

### How to Run
```bash
docker-compose up --build
```

### Screenshots
![Running Containers](./screenshots/containers.png)
![Prometheus](./screenshots/prometheus.png)
![Grafana](./screenshots/grafana.png)