# Carbon Desk · Case 01: Veltara Systems (technology)

A choose-your-path learning simulation. The learner is the new Sustainability Manager of Veltara Systems, a fictional French SaaS + IoT hardware group with 640 staff and €92.4M revenue. They work on a simulated laptop with Mail, Files, a Carbon Workbook, an emission factor library, a calculator, Chat and a Report app. The goal is a GHG Protocol inventory for FY2025 and the ESRS E1-6 table for the CSRD sustainability statement, reviewed by a fictional auditor (limited assurance).

Built on the approach of the FRITEO Bilan Carbone training case (one realistic company, a client data pack, calculations by emission source). The case adds three things: stakeholder pressure, decisions with consequences, and an assurance outcome.

`index.html` is self-contained. Open it in a browser. Progress is saved in localStorage.

## Mission flow

| # | Sender | Topic | Learning objective |
| --- | --- | --- | --- |
| 1 | CEO | Kick-off | Inventory plan, principles, audit trail |
| 2 | CFO | Group structure | Consolidation approach (ESRS vs GHG Protocol), 70% sub, leased office, 20% associate |
| 3 | Auditor | Scope 3 screening | Relevance of the 15 categories, justified exclusions |
| 4 | Facilities | Scope 1 + waste | Gas (HHV), generator, F-gas mass balance, fleet (AdBlue trap), EV double-count trap |
| 5 | Energy broker | Scope 2 | Dual reporting, residual mix, GoOs (unbundled vs contract), district heat, Cat. 3 |
| 6 | CTO | Cloud | Supplier-specific vs spend-based data, provider market-based figures |
| 7 | Procurement | Purchases | Spend-based screening without double counting, primary PCF, Cat. 2 with no depreciation, Cat. 15 |
| 8 | Supply chain | Logistics | t·km by mode, air freight hotspot, GLEC carrier data |
| 9 | HR | Travel and commuting | "One-off" exclusion pressure, radiative forcing, teleworking |
| 10 | CMO | Products + claims | Cat. 11 direct vs indirect use phase, Cat. 12, offset-based neutrality claims (Directive 2024/825) |
| 11 | Auditor | ESRS E1-6 | Table build, intensity per net revenue, base year, credits not netted |

## Answer key (best decisions)

Training emission factors are in the file (`F` object), with all data in `D`.

| Line | tCO2e |
| --- | --- |
| Scope 1 (gas 85.74, generator 4.52, F-gas 15.66, fleet 37.50) | 143.42 |
| Scope 2 location-based | 143.21 |
| Scope 2 market-based (no GoOs bought) | 160.19 |
| Cat. 1 kits (verified PCF 15.2 kg; 441.0 with the 18 kg estimate) | 372.40 |
| Cat. 1 cloud (provider location-based) | 312.00 |
| Cat. 1 services (spend-based) | 795.50 |
| Cat. 2 capital goods | 385.70 |
| Cat. 3 fuel and energy | 56.76 |
| Cat. 4 upstream transport | 94.21 |
| Cat. 5 waste | 18.52 |
| Cat. 6 business travel (without RF; 896.45 with RF) | 533.01 |
| Cat. 7 commuting + teleworking (153.79 without teleworking) | 245.64 |
| Cat. 11 use of sold kits | 731.06 |
| Cat. 12 end of life | 14.40 |
| Cat. 15 investments | 28.00 |
| **Total, location-based** | **≈ 3,874** |

Intensity: ≈ 41.9 tCO2e per € million (location-based).

The keys are recomputed from the learner's legitimate choices: GoOs, cloud source, PCF request, RF and teleworking. Lines are accepted within ±10%, and count as exact within ±2%.

## Scoring

- **Accuracy**: the learner's workbook vs the evidence, weighted by tonnes.
- **Audit readiness** and **Stakeholder trust**: moved by each decision.
- **Days to deadline**: 30 working days. Each mission and optional data request uses some.
- **Auditor conclusion**: unqualified, qualified or adverse.

## Next cases (same engine)

Swap the `D`, `FILES` and `MISSIONS` objects. Planned sectors: food manufacturing (FRITEO-like), retail, logistics, construction.

*All companies, people and figures are fictional. Emission factors are rounded training values. Cite the exact database and version in real work.*
