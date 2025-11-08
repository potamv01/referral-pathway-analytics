# Referral Pathway Analytics
> Reduce admin load & wait times with automated KPIs, breach-risk alerts, and “to-be” workflow design.

**Tech:** SQL Server, Python, Power BI · **Domain:** NHS operations · **Privacy:** synthetic demo data only

## Problem
Referral queues were opaque; breaches rose and admin time was high.

## Approach
- SQL schema + KPI queries (SLA breaches, backlog risk)
- Python ETL to compute risk flags and export to Power BI
- “To-be” workflow + SOP excerpt (see /docs)

## Results (simulated)
- Admin time ↓ **30%**
- Breach alerts delivered daily; backlog visualised by service
- Governance: data catalog + validation checks

## Repository tour
- `/sql` – schema & KPIs
- `/python` – `etl.py` to build KPIs
- `/powerbi` – dashboard export (PNG + optional PBIX)
- `/docs` – case-study.md, workflow diagrams
- `/data` – synthetic data + DATA_NOTES.md

## Quickstart
```bash
python -m venv .venv && source .venv/bin/activate  # win: .venv\Scripts\activate
pip install -r requirements.txt
python python/etl.py --in data/raw --out data/processed



