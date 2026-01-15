# 🛠️ Maintenance Data Platform  
### A complete end-to-end data engineering + application system simulating a real maintenance workflow for electric vehicles

This project is a full learning environment designed to simulate how a modern company would build an end-to-end maintenance platform for electric vehicles (motorcycles or cars), including:

- A **transactional operational system** (Postgres)
- A **workflow + mechanics app** (Retool)
- A **data orchestrator** (Dagster)
- A **real-time analytical database** (ClickHouse)
- A **BI/analytics layer** (Metabase)
- A **local Docker environment** to run everything easily

This project is built to learn:
- Data modeling
- Orchestration pipelines
- Simulating real operational data
- Analytics with event-driven architecture
- Integration between app → database → pipelines → dashboards

---

# 🚀 Features

### ✔ Complete operational database (25+ tables)
Models include:
- Vehicles, mechanics, parts, suppliers  
- Maintenance workflow (OS, events, assignments)  
- Inventory + purchase orders  
- Diagnostic codes & vehicle alerts  
- Billing & audit logs  
- Telemetry simulation  

### ✔ Realistic maintenance workflow
- Create a vehicle
- Register conditions
- Create Orders of Service (OS)
- Track status changes
- Assign mechanics
- Log work events (start, pause, finish)
- Consume parts
- Log inventory movements

### ✔ Analytics-ready architecture
- Status history  
- Labor time tracking  
- Inventory movements  
- Telemetry (usage, battery cycles, alerts)  
- Billing + cost center  

---

# 🧱 Architecture Overview

                ┌───────────────────────────┐
                │         Retool App        │
                │ (operational UI: OS, pcs) │
                └──────────────┬────────────┘
                               │ CRUD / actions
                               ▼
                      ┌─────────────────┐
                      │   Postgres OLTP │
                      │  (source of truth)
                      └───────┬─────────┘
                              │ ingestion
                              ▼
                 ┌─────────────────────────┐
                 │         Dagster          │
                 │  jobs, assets, pipelines │
                 └───────────┬──────────────┘
                             │ analytics
                             ▼
                     ┌─────────────────┐
                     │ ClickHouse OLAP │
                     │ (historical data)
                     └──────┬──────────┘
                            │ queries
                            ├─────────► Retool dashboards
                            ▼
                       ┌──────────┐
                       │ Metabase │
                       └──────────┘


---

# 📦 Tech Stack

| Component | Tool | Purpose |
|----------|------|----------|
| Database (OLTP) | **Postgres** | Operational system (app data) |
| Database (OLAP) | **ClickHouse** | Historical + analytics |
| App Layer | **Retool** | CRUD, UI, mechanics workflow |
| Orchestration | **Dagster** | Pipelines, transformations, metrics |
| Business Intelligence | **Metabase** | Dashboards + SQL |
| Environment | **Docker** | Local development |

---

# 📁 Recommended Repository Structure
maintenance-data-platform/
│
├── docker/
│ └── docker-compose.yml
│
├── sql/
│ ├── postgres/
│ │ └── full_schema.sql
│ └── clickhouse/
│ ├── analytics_tables.sql
│ └── materialized_views.sql
│
├── dagster/
│ ├── maintenance_dagster/
│ │ ├── assets/
│ │ ├── jobs/
│ │ ├── resources/
│ │ └── definitions.py
│ └── pyproject.toml
│
├── retool/
│ └── app_screenshots/

