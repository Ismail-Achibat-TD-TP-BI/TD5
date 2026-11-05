# REFLECTIONS (TD5)

## 1. Which stakeholder disagrees most?
Prediction: the **network/strategic manager** vs. the other two — CO2 and cost both point toward optimizing the existing 3 warehouses, while network planning is the one asking "add or remove a warehouse entirely," a bigger, different kind of decision.

## 2. Least defensible assumption?
**Population-as-demand** (50 tonnes/year per 1,000 residents). The CO2 factor at least sits in a real ADEME/government-cited range; this number isn't sourced at all — it's an illustrative stand-in with no real shipment data behind it.

## 3. Two KPIs, different actions, same warehouse
**Lille**: CO2/cost say it contributes 0 kg and 0 EUR (looks idle, maybe ripe to close). The network scenarios say closing it makes the average distance *worse* (168.04 → 174.43 km), because its own local population would then travel to Paris instead. CO2 says "cut it," network says "keep it."

## 4. Trust the #1 CO2 route as-is?
No — it's **Marseille ← Lyon**. Marseille is a `candidate_warehouse`, not just a customer, so before recommending consolidation on that route I'd check whether opening Marseille itself (Step 10's scenario) makes the route irrelevant rather than optimizing it.

## 5. Highest-cost warehouse, which lever?
**Lyon**, 13,476,013 EUR total. Storage (7,788,952 EUR) edges out transport (5,687,061 EUR) — but both are large, so I'd pull **storage** first since it's the bigger single number.

## 6. The big one — network recommendation
I'd **open Marseille** (115.03 km avg, best of the four). The caveat (no capex/lease-exit cost) doesn't change my answer, just my confidence — I'd present it as "best option on distance alone, pending a capex check," not a final call. Reflection 1 check: right in spirit (network manager is the odd one out) but I predicted disagreement over *closing/opening*, and the real surprise was Lille's counter-intuitive case, which I hadn't anticipated.

## 7. Fourth chart
Added to `cost.html`: a ranked bar of **cost per tonne (EUR), by warehouse** — a normalized view, not a copy of the existing stacked bar. The stacked bar shows *total* cost, which mostly tracks warehouse size (more tonnes = more total cost even if run well); it can't answer "independent of size, which warehouse is structurally the most expensive to run per tonne?" A ranked bar chart is the right type because warehouses are a small set of discrete categories being compared on one number — same logic as the CO2 dashboard's top-routes ranking, applied to warehouses instead of routes. Real result: Lyon (69.21 EUR/tonne) is worst, then Paris (50.91), then Lille (40.0) — the same order as the stacked bar's totals here, which is itself worth noting: in this particular network, "biggest total cost" and "least efficient per tonne" happen to agree, but they're still answering different questions, and wouldn't necessarily agree in a different network.
