# OpenTelemetry Observability Project

## Overview
This project explores end-to-end observability using the OpenTelemetry Demo application, with Prometheus for metrics, Grafana for visualization, and Jaeger for distributed tracing.

## Tools & Technologies
- **OpenTelemetry** – Telemetry collection and instrumentation
- **Prometheus** – Metrics querying and monitoring
- **Grafana** – Dashboards and metrics visualization
- **Jaeger** – Distributed tracing
- **Docker Compose** – Running the demo and observability services
- **AWS EC2** – Cloud-based practice environment

## What I Worked On
- Deployed the OpenTelemetry Demo using Docker Compose on an AWS EC2 instance.
- Ran the observability stack alongside the demo application.
- Connected Prometheus to Grafana and verified the data source.
- Queried service metrics in Prometheus and Grafana.
- Explored service-level metrics and observability dashboards.

## Observability Components
| Component | Purpose |
|---|---|
| OpenTelemetry | Telemetry instrumentation and collection |
| Prometheus | Metrics storage and querying |
| Grafana | Metrics visualization and dashboards |
| Jaeger | Distributed trace exploration |
| Docker Compose | Service orchestration |

## Reference
This project uses the official [OpenTelemetry Demo](https://github.com/open-telemetry/opentelemetry-demo) as its application foundation.

## Learning Outcome
Hands-on practice with deploying a multi-service application and exploring metrics, dashboards, and distributed observability in a cloud environment.

## Architecture

The project runs the OpenTelemetry Demo application alongside an observability stack.

```text
OpenTelemetry Demo
        |
        v
  Telemetry Data
        |
        v
OpenTelemetry Collector
        |
        v
   Prometheus
        |
        v
     Grafana
  (Dashboards)

Demo services
        |
        v
Distributed Traces
        |
        v
      Jaeger
```

## Setup and Execution

The project was deployed on an AWS EC2 Ubuntu instance using Docker Compose.

1. Clone the official demo repository.
2. Start the demo services using Docker Compose.
3. Start the observability configuration alongside the demo.
4. Access the application and observability interfaces.
5. Verify metrics in Prometheus and visualize them in Grafana.

Example commands:

```bash
git clone https://github.com/open-telemetry/opentelemetry-demo.git
cd opentelemetry-demo

docker compose up -d

docker compose -f compose.yaml \
  -f compose.observability.yaml up -d
```

**Note:** These commands assume the observability Compose file is available in the cloned repository. Follow the repository's current instructions if its configuration changes.

## Services Used

- **Demo application:** Port 8080
- **Prometheus:** Port 9090
- **Grafana:** Port 32795
- **Jaeger:** Port 32793

Ports may vary depending on the Compose configuration.

## Future Improvements

- Add more Grafana dashboard panels.
- Explore distributed traces in Jaeger.
- Add alerting and service-health monitoring.
