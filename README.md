# Homelab

## Машини
| Име | IP | Роля |
|---|---|---|
| pve | 192.168.100.241 | Proxmox node (Shuttle), pfSense |
| pve2 | 192.168.100.242 | Proxmox node (HP EliteBook 840 G5) |
| qdev | 192.168.100.243 | QDevice witness (Acer, Debian 13) |
| docker01 | 192.168.100.244 | Docker VM на pve2: мониторинг |
| Synology | 192.168.100.2 | NAS (DS120j): backup-и |

Клъстер: `HomePVECluster`, 2 node-а + QDevice.

## Мониторинг (`monitoring/`)
Prometheus, Grafana, pve-exporter, blackbox, speedtest.

Вдигане:
1. `cp monitoring/pve.yml.example monitoring/pve.yml` и сложи token-а
2. `cd monitoring && docker compose up -d`

- Grafana: http://192.168.100.244:3000
- Prometheus: http://192.168.100.244:9090

