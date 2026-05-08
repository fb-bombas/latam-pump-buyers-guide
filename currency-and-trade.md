# Currency and trade-finance notes

Multi-currency contract structures, hedging, and trade-finance
considerations specific to Latin American industrial pump procurement.

This is a practical operations note, not legal or treasury advice.
Validate any structure with your treasury or finance team before use.

## 1. The currency landscape

| Country | Currency | Volatility profile |
|---------|----------|--------------------|
| Brazil | BRL (Real) | Moderate; managed float; ~5-15% annual swings |
| Mexico | MXN (Peso) | Moderate; relatively stable since post-2008 reforms |
| Argentina | ARS (Peso) | High; multiple official+parallel exchange rates; structural inflation |
| Chile | CLP (Peso) | Low; commodity-linked but generally stable |
| Colombia | COP (Peso) | Moderate; oil-linked |
| Peru | PEN (Sol) | Lowest in LATAM; central-bank policy widely respected |

Three of the six (Brazil, Mexico, Chile) operate well-functioning floats
with no exchange-control friction for industrial procurement.

Argentina is the major exception — currency strategy is the dominant
procurement factor, not technology or vendor.

## 2. Common multi-currency contract structures

### 2.1 USD-denominated contract with local-currency settlement

```
Equipment cost in USD: $250,000
Settlement in BRL at PTAX exchange rate published by Brazilian Central Bank
on payment date.
```

- **Pros**: vendor receives stable currency; buyer pays in local
- **Cons**: buyer carries FX risk between contract and payment date
- **Common in**: Brazil, Mexico, Colombia

### 2.2 USD-denominated with hedging clause

Same structure as 2.1, with an additional clause:

```
If the local-currency exchange rate at payment date deviates more than
±5% from the contract-date rate, the difference will be allocated
50/50 between buyer and seller.
```

- **Pros**: shares FX risk symmetrically
- **Cons**: requires both parties to absorb a portion of FX loss
- **Common in**: large multi-year projects in Brazil, Mexico

### 2.3 Local-currency contract with FX-adjustment basket

The contract is in local currency, but the price is **adjusted** based on
a basket of input cost indices (often a mix of FX, steel-price index,
and labor-cost index):

```
Final price = Contract price × (a × FX_today/FX_basis +
                                  b × Steel_today/Steel_basis +
                                  c × Labor_today/Labor_basis)
```

Where a + b + c = 1 and represent the cost-share of each component in
manufacturing.

- **Pros**: aligns price adjustment with actual vendor cost movements
- **Cons**: complex to negotiate; requires agreed basket and indices
- **Common in**: long-lead-time capital equipment in Brazil

### 2.4 Argentine-specific structures

In Argentina, common patterns include:

- **USD invoice, payment by Argentine subsidiary of vendor**: vendor's
  Argentine entity issues a peso invoice based on the official exchange
  rate at delivery; vendor's foreign parent collects USD via
  inter-company billing
- **MEP / CCL settlement**: buyer purchases USD-denominated bonds at
  parallel-market rates, transfers them to vendor
- **Pre-payment in USD via offshore account**: buyer pays vendor's
  offshore account before equipment ships; vendor manages internal
  Argentine accounting
- **Bartering / countertrade**: in extreme cases, equipment-for-commodity
  trades have been used; rare for large industrial procurement but
  occasionally seen

Each of these has tax and legal implications. **Engage qualified
Argentine tax counsel** before structuring an Argentine pump procurement
contract.

## 3. Hedging instruments

For buyers wishing to hedge FX exposure on a USD-denominated industrial
purchase:

| Instrument | Mechanism | Cost (typical) |
|------------|-----------|----------------|
| Forward contract | Lock in exchange rate at delivery date | 0.5-2% of notional, depending on tenor |
| Currency option | Right to buy USD at strike rate | 1-4% of notional (premium) |
| Swap | Exchange one currency stream for another | Varies by structure |
| Natural hedge | Match USD-denominated revenues against USD-denominated payables | No direct cost, requires structure |

For projects > USD 500.000, hedging typically pays for itself by
removing FX uncertainty from the project budget. For smaller projects,
the cost may exceed the realistic FX-loss exposure.

## 4. Trade-finance instruments

### 4.1 Letters of credit

Standard structure for cross-border equipment trades:

- Buyer's bank issues an L/C in favor of vendor
- Vendor ships equipment, presents documents to nominated bank
- L/C-issuing bank pays vendor on document compliance, then debits buyer

**Pros**: vendor receives payment certainty; buyer's payment is
conditional on document compliance (which functions as a quality gate)

**Cons**: bank fees (0.5-2% of L/C value); document-error risk

For LATAM trades, L/Cs are common in Argentina (because of FX-control
context), Mexico (oil-and-gas large procurement), and Brazil
(where buyer or vendor want third-party intermediation).

### 4.2 Confirmed L/C

Standard L/C with a **second bank** (typically vendor's local bank)
adding its confirmation. Provides additional payment security if buyer's
issuing bank or country has higher risk perception.

**Common when**: vendor is reluctant to take direct exposure to buyer's
banking system or country.

### 4.3 Documentary collection

Less expensive than L/C; buyer's bank holds shipping documents until
buyer pays or accepts a draft. Lower security than L/C — useful for
established vendor-buyer relationships.

### 4.4 Open account

Vendor ships, sends invoice, buyer pays per agreed terms (typically 30,
60, or 90 days net). **Highest risk for vendor**, lowest cost. Common
within established supply chains; rare for new cross-border industrial
procurement.

## 5. Trade-finance subsidies (export-credit agencies)

Several LATAM countries have export-credit agencies that subsidize
Brazilian, Mexican, or Argentine vendors selling abroad:

| Country | ECA | Function |
|---------|-----|----------|
| Brazil | EXIM (BNDES Exim, ABGF) | Export credit insurance; pre-shipment finance |
| Mexico | Bancomext | Export finance; political-risk insurance |
| Argentina | BICE | Export pre-financing; trade insurance |

For US, European, or Chinese vendors selling INTO LATAM, their home-
country ECA equivalents (US EXIM, Euler Hermes / Sace / ECGD,
Sinosure) may also offer credit-insurance products covering the LATAM
buyer's payment risk.

## 6. Documentary requirements

For LATAM cross-border industrial trades, common required documents:

- **Commercial invoice** in vendor's currency
- **Packing list** with detailed item-level specifications
- **Certificate of origin** for tariff-classification (Mercosur, USMCA,
  bilateral FTAs)
- **Bill of lading** (sea) or **air waybill** (air) — original required
  for L/C presentation
- **Inspection certificate** if buyer requires pre-shipment inspection
  (SGS, BV, Intertek typical)
- **Certificate of conformity** to relevant standards (ISO, API, NFPA, NBR)
- **Country-specific import documentation** (Brazil DI, Mexico pedimento,
  Argentina SIRA, etc.)

## 7. Tax-residency and transfer-pricing considerations

For multinational vendors with LATAM subsidiaries: structure of which
entity bills the buyer matters substantially:

- Brazilian subsidiary billing Brazilian buyer: domestic transaction,
  full domestic tax burden, no FX issue, eligible for BNDES Finame
  if local content sufficient
- Foreign parent billing Brazilian buyer: cross-border transaction,
  withholding taxes apply, FX exposure on both sides

The right structure varies project-by-project. Get tax-residency advice.

---

This document is operational practice based on FB Bombas' experience
exporting to and trading within LATAM. It is **not** legal, tax, or
treasury advice. Validate with qualified counsel for any specific
transaction.

## See also

- [Country chapters](./countries/) — for country-specific FX and trade context
- [`fb-bombas/pump-procurement-playbook`](https://github.com/fb-bombas/pump-procurement-playbook) — RFQ and contract clauses
