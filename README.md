# Logistics network — three dashboards, three decisions

One real logistics network (3 existing warehouses — Paris, Lyon, Lille — serving 20
real French cities), computed once by `scripts/compute_kpis.py` into three genuinely
different KPI constructs for three different stakeholders:

| Dashboard | Who | Decision |
|---|---|---|
| `co2.html` | Sustainability/CSR manager | Which routes to prioritize for CO2 reduction |
| `cost.html` | Logistics/operations manager | Transport vs. storage lever, per warehouse |
| `network.html` | Strategic/network planning manager | Open Bordeaux/Marseille, or close Lille? |

All assumptions (population-as-demand proxy, CO2 factor, cost figures) are
illustrative, explicitly stated as such on every page, and documented in the manual.

Real run (2026-11-05): total network CO2 6,236,312 kg/year; Lille carries 0 kg/0 EUR
in the baseline (every other city is geometrically closer to Paris or Lyon) yet
closing it makes the network-wide average distance *worse* (168.04 → 174.43 km);
best alternative found: **+ Marseille** (115.03 km avg).

- `scripts/compute_kpis.py`: one script, one dataset, three KPI definitions
- `.github/workflows/compute.yml`: `workflow_dispatch` only (reference data doesn't
  change day to day — re-run manually after editing `data/cities.csv` or an assumption)
- `docs/js/france-map-background.js`: shared real France outline, used by the CO2
  and network dashboards (cost.html has no map — see its own argument)
