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

