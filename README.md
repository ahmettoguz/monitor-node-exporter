<h1 id="top" align="center">Monitor Node-Exporter <br/> 🚢 v1.0.0 🚢</h1>

<br>

## 🔍 Table of Contents

- [Features](#features)
- [System Startup](#system-startup)

<br/>

<h2 id="features">🔥 Features</h2>

- **Docker Compose Deployment:** Simplifies deployment with Docker Compose configuration, enabling easy setup and service orchestration without complex commands.
- **Network Setup:** Integrates Node-Exporter with other metric tools with other networks.

<br/>

<h2 id="system-startup">🚀 System Startup</h2>

- Create a new directory named `monitor`.

```
mkdir monitor
cd monitor
```

- Clone project.

```
git clone https://github.com/ahmettoguz/monitor-node-exporter
```

- Create `network-monitor` network if not exists.

```
docker network create network-monitor
```

- Run container.

```
docker stop                              monitor-node-exporter-c
docker rm                                monitor-node-exporter-c
docker compose -p monitor up --build -d  node-exporter
docker compose -p monitor up -d          node-exporter
docker logs -f                           monitor-node-exporter-c
```

- Refer to [`prometheus`](https://github.com/ahmettoguz/monitor-prometheus) repository to integrate prometheus to scrap data.

- Refer to [`grafana`](https://github.com/ahmettoguz/monitor-grafana) repository to integrate grafana to visualize node exporter data.

<br/>

### [🔝](#top)
