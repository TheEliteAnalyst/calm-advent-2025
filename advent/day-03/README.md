# 📅 Day 3: Connect Nodes with Relationships

## Overview

Today’s challenge expanded our ransomware defense model by creating multiple relationship types between nodes:
- **connects** (technical link service → database)
- **interacts** (actor → service)
- **composed-of** (system contains components)

These help model how the architecture *behaves* and *is composed*.  Use of CALM Agent was greatly helpful is debugging and provideing insights.

---

## 🗂 Files Updated
📁 architectures/
└── ransomware-defense-architecture.architecture.json

---
🔗 Relationships Added
✅ Connects

Server Collector → Telemetry Message Bus
Captures how server‑side telemetry is ingested into the event stream for processing.

Endpoint Collector → Telemetry Message Bus
Captures endpoint telemetry ingestion from workstations and user devices.

Analytics Engine → Telemetry Store
Stores detection artifacts and evidence for forensic analysis and long‑term retention.

✅ Interacts

Security Analyst → Reporting Dashboard
Represents how a human SOC analyst reviews alerts, incidents, and system metrics through the dashboard interface.

✅ Composed-of

Ransomware Defense Architecture → {Telemetry, Analytics, Response, Reporting Subsystems}
Shows how the overall ransomware defense platform is composed of telemetry collection, detection, alerting, response orchestration, and reporting components.

✅ Validation Executed 

![Architecture Validation Completed](advent\day-03\architecture-validation.png)

Experimented with the oneOf Constraint