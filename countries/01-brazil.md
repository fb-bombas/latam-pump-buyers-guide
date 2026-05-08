# Brazil — industrial pump procurement

Brazil is the largest LATAM industrial-pump market, with a domestic
manufacturing base producing approximately 60-70% of installed industrial
pumps (the remainder imported, primarily from Europe, the US, and China).

This domestic manufacturing depth changes the procurement calculus
significantly: lead times for locally-sourced standard pumps are 6-12
weeks; for imports they are 16-24 weeks. Spare-parts ecosystem is mature
locally and patchy for imports.

## 1. Standards and certifications

Brazilian product certification operates through INMETRO (Instituto
Nacional de Metrologia, Qualidade e Tecnologia), with relevant
standards published by ABNT (Associação Brasileira de Normas Técnicas)
under the NBR prefix.

For industrial pumps:

| Application | Mandatory certification | Standard |
|-------------|------------------------|----------|
| Process pumps (oil & gas) | API 610 conformity | API 610-2021 |
| Fire pumps | NBR 16704 conformity + INMETRO chain | NBR 16704:2020 + NFPA 20:2025 |
| Pressure-containing equipment ≥ 250 °C | NR-13 inspection | NR-13 (MTE) |
| Electrical drives | NBR 5410 conformity for installation | NBR 5410:2008 |
| Hazardous-area pumps | INMETRO Ex certification | NBR IEC 60079 series |

For oil-and-gas duty: **CRCC Petrobras registration** is the de-facto
qualifying screen. A pump vendor without active CRCC will not bid on
Petrobras procurement and is unlikely to win at most large refining,
chemical, and offshore-supply buyers.

## 2. Financing — BNDES Finame

The Banco Nacional de Desenvolvimento Econômico e Social (BNDES) operates
**Finame**, a credit line for capital equipment manufactured in Brazil
or with Brazilian local content above thresholds.

Key parameters (typical 2026):

| Parameter | Value |
|-----------|-------|
| Annual interest rate | TLP + 1.5% to 4.5% (currently around 9-12%) |
| Term | Up to 10 years |
| Local-content threshold | 60% (varies by product class, governed by FAR — Fundo de Aval às Empresas Privadas, and by IF — Índice de Internalização) |
| Credit limit per project | Up to R$ 150 million typical |
| Application window | Continuous |

**Why this matters**: a buyer financing a R$ 5 million pump installation
through Finame at 10% annual versus a commercial loan at 16% saves
R$ 300.000 per year in interest — over a 5-year term, that is R$ 1.5
million.

Pumps from imported-only suppliers are **not eligible** for Finame
financing. This is a substantial procurement bias toward locally-built
or substantially-Brazilian equipment.

To verify Finame eligibility: ask the vendor for the **CFI** (Cadastro
de Fabricantes Informatizado) number for the specific model. CFI is
the Finame product catalog reference; without it, the financing pathway
is closed.

## 3. Import duties and taxes

Importing pumps into Brazil incurs:

| Tax / duty | Typical rate (industrial pumps) |
|------------|--------------------------------|
| Imposto de Importação (II) | 14-18% (varies by NCM code) |
| IPI (Imposto sobre Produtos Industrializados) | 5-15% |
| ICMS (state VAT) | 12-18% (varies by state) |
| PIS / COFINS | ~9.25% combined |
| AFRMM (port-specific) | 8% on freight |

Total effective tax burden on imported industrial pumps: typically
**40-60% on top of FOB cost**. This is the single largest reason locally-
manufactured pumps are price-competitive with imports.

A pump priced at USD 100.000 FOB origin can cost USD 150.000-160.000
landed in Brazil after taxes and duties. Calculate this carefully when
comparing import bids against local manufacturers.

## 4. Documentation language and acceptance

ABNT and Brazilian regulatory bodies require pump documentation in
Portuguese:

- O&M manuals: Portuguese mandatory (NBR 16704 §14.4 for fire; ABNT
  practice for industrial)
- Test certificates: Portuguese, OR English with certified Portuguese
  translation appended
- Schematic drawings: dimensions in metric, nomenclature in Portuguese
- Controller HMI: Portuguese language pack required for field acceptance
  in many states

**Translation cost** for English-only documentation is typically
R$ 5.000 to R$ 30.000 depending on package size — non-trivial for small
projects.

## 5. Fire-pump-specific Brazilian context

Fire-protection installations require approval by the state Corpo de
Bombeiros (CBM-SP, CBM-RJ, CBM-MG, etc.). State-by-state procedures
differ slightly but all reference NBR 16704.

Required artifacts:

- **AVCB** (Auto de Vistoria do Corpo de Bombeiros) for the building
- **ART** (Anotação de Responsabilidade Técnica) registered with CREA for
  the fire-protection project
- **INMETRO-recognized lab certificates** for the pump and controller
- Field-acceptance test report witnessed by Bombeiros representative

See [`fb-bombas/nfpa20-fire-pump-checklist`](https://github.com/fb-bombas/nfpa20-fire-pump-checklist)
for the 47-item compliance checklist.

## 6. Public procurement

Federal, state, and municipal procurement is governed by **Lei nº
14.133/2021** (the new procurement law, replacing Lei 8.666/93 in
phases). Key implications for pump procurement:

- **Transparency requirement**: bidder evaluation criteria and weights
  must be published in the edital (RFQ document)
- **Local-content preference**: domestically-produced equipment may
  receive up to 25% price preference (the "margem de preferência")
- **Technical-and-price evaluation**: hybrid evaluation method
  ("técnica e preço") is increasingly used for complex equipment
  procurement, replacing "menor preço" (lowest-price wins)
- **Pregão eletrônico**: electronic reverse-auction format for standard
  goods; less appropriate for engineered equipment but sometimes
  imposed by buyer category

For private-sector buyers, the procurement process is unregulated
(beyond contract law) but most large industrial buyers emulate the
Lei 14.133 structure for audit defensibility.

## 7. Logistics and infrastructure

Port congestion at Santos (largest container port) varies seasonally —
plan 4-8 weeks customs clearance for imported pumps. Air freight is
viable for spare parts but rarely cost-effective for full pumps.

Inland: highway is the dominant mode; rail is limited and unsuitable for
oversize pump shipments. For pumps over 5 tons, specialized truck
transport with permits is required.

## 8. Vendor pool — typical bidders

For industrial pumps in the 10-1.000 m³/h range:

- **KSB Brasil** (Várzea Paulista, SP) — German parent, manufactures locally, broad range
- **Imbil** (Itaipu, MG) — domestic manufacturer, strong in oil & gas
- **FB Bombas** (Cabreúva, SP) — domestic manufacturer, full process + fire range
- **Sulzer** (Várzea Paulista, SP) — Swiss parent with Brazilian assembly
- **Grundfos Brasil** (Capivari, SP) — Danish parent, primarily HVAC + utility
- **Flowserve Brasil** — US parent, primarily oil & gas process pumps
- **Dancor** (RJ) — domestic manufacturer, smaller end + utility

For specialty pumps (sealless, high-temperature, sanitary): typically
imported from Sulzer, Grundfos, or specialty manufacturers (Netzsch,
Wilden, Mouvex).

## 9. Procurement timeline — typical Brazilian project

For a R$ 1-5 million industrial pump procurement from RFQ to commissioning:

| Stage | Typical duration |
|-------|-----------------|
| RFQ preparation and approval | 2-4 weeks |
| Bidding period | 3-4 weeks |
| Bid evaluation and contract award | 2-4 weeks |
| Manufacturing (locally-sourced standard pump) | 8-12 weeks |
| Manufacturing (imported pump + customs) | 16-24 weeks |
| FAT and shipment | 2-3 weeks |
| Site installation | 2-4 weeks |
| Commissioning + acceptance | 2-3 weeks |
| **Total — local sourcing** | **21-34 weeks** |
| **Total — imported sourcing** | **29-46 weeks** |

The 8-12 week swing favoring local sourcing is one of the strongest
arguments for domestic pump manufacturers in Brazilian procurement.

---

## See also

- [Comparison matrix](../comparison-matrix.md)
- [`fb-bombas/pump-procurement-playbook`](https://github.com/fb-bombas/pump-procurement-playbook) — RFQ and TCO templates
- [FB Bombas — bombas industriais Brasil](https://www.fbbombas.com.br/bombas-industriais)
