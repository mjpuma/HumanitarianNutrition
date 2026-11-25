# HumanitarianNutrition — v0.1 (2026-11-25)
Study window: 1954–2026. Historical evidence to inform future humanitarian nutrition procurement and preparedness. This is a seed dataset, not a complete global census or clinical guidance.

## Contents
- observations.csv: 429 observations (410 UNICEF supplier/channel/year prices and 19 USDA product/packaging/report-period purchases).
- sources.csv: source register with URLs and document descriptions.
- products.csv: provisional product taxonomy, including products not yet observed.
- nutrition.sqlite: SQLite copies of the three tables plus historical milestones.
- build.py: reproducible construction of the seed tables from manually transcribed primary-source figures.
- historical_milestones.csv: contextual evidence kept separate from procurement measurements.

## Methods and caveats
UNICEF: use September 2025 edition for 2003–2018 and August 2026 edition for 2019–2026. The earlier PDF actually has both tables on one page; the latest has offshore on page 1 and country-office on page 3. Values are manually transcribed against displayed tables. A second independent transcription and revision comparison are still needed before publication. Carton mass is 13.8 kg as stated in both editions; independently check historical packaging changes. Currency is retained as published; price_per_kg is in that currency, NOT necessarily USD. Country-office figures are UNICEF's USD conversions. Offshore FCA excludes onward transportation; country-office terms can be EXW or DAP. 2026 UNICEF is partial year. Missing entries are not zero. Do not average suppliers as a volume-weighted global price without weights.

USDA: 2019–2024 observations are Q4-labelled reports; whether these are cumulative fiscal-year figures is not independently confirmed, so do not aggregate with other quarters or interpret as annual totals until checked. 2025–2026 are annual reports. PO value / metric tons / 1000 yields nominal USD/kg; freight scope needs confirmation. Broader AMS summaries have different values and are not combined. Unlisted products are not recorded as zero.

Fields: source_id joins sources; page is one-based; year and period distinguish calendar, partial calendar, fiscal year, and Q4 with unresolved coverage; buyer/channel/product/supplier/packaging describe reporting strata; currency applies to prices and values; price_per_pack and pack_kg retain original UNICEF units; quantity_mt and purchase_value retain USDA published totals; price_per_kg is derived; cost_basis records reporting terms. Empty cells mean unavailable. No inflation adjustment or FX conversion beyond what the source itself provides.

## Next extraction priorities
1. PL480 annual reports (1954 onward), especially nutrition commodities, tonnage, valuation and destinations; locate original tables for CSM, WSM, DSM, CSB, WSB.
2. WFP and UNICEF historical annual reports, and WFP food aid shipment archives; keep purchases, deliveries and distributions distinct.
3. Older USAID Food for Peace contract awards for RUSF and fortified blends; verify Q4 reporting conventions, collect supplier and freight records.
4. Versioned product specifications: ingredients, energy, target population, water/fuel and preparation. Do not assume equal clinical outcomes per kg.
5. Add FX, inflation, agricultural input prices, logistics and validated program outcomes; retain raw and harmonized tables separately.
