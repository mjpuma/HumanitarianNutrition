# HumanitarianNutrition (v0.1, research in development)

*Historical evidence for future humanitarian nutrition interventions, 1954–2026.*

A companion to [FamineWatch Datasets](https://github.com/mjpuma/faminewatch-datasets) and [TherapeuticProvisioning](https://github.com/mjpuma/TherapeuticProvisioning).

The study begins with Public Law 480 in 1954 and traces the evolution of specialized nutrition products, procurement costs, quantities and supply chains. Its purpose is to learn from historical interventions to inform future humanitarian nutrition systems.

**429 seed observations · 18 product categories · 16 registered sources**

**Explore in your browser:** [docs/index.html](docs/index.html). Download the HTML and open locally, or enable GitHub Pages from main /docs.

## What's in the repository

| File | Contents |
|---|---|
| [data/observations.csv](data/observations.csv) | Procurement observations, 2003–2026 |
| [data/products.csv](data/products.csv) | Historical and contemporary product registry |
| [data/sources.csv](data/sources.csv) | Source documents and archival leads |
| [data/historical_milestones.csv](data/historical_milestones.csv) | Historical context |
| [data/build.py](data/build.py) | Rebuild CSV tables and SQLite database with Python 3 |
| [METHODOLOGY.md](METHODOLOGY.md) | Methods, data limitations and collection priorities |
| [docs/index.html](docs/index.html) | Standalone searchable data explorer |

## Historical scope

| Period | Research focus |
|---|---|
| 1954–1964 | Milk-based nutrition foods |
| 1965–1994 | Fortified blended foods |
| 1995–2010 | Therapeutic milks and ready-to-use foods |
| 2011–2026 | Specialized nutrition supply chains |

These are analytical periods, not exclusive dates of product use. Quantitative records currently begin in 2003; the historical archive remains a collection priority.

## Reproduce

Run `python data/build.py` from the repository root to generate the database locally. The explorer contains a snapshot of the seed CSV and must be refreshed when the data change.

## Status and limitations

Unpublished research seed. Transcriptions require independent source verification, source-specific redistribution terms require review, and no blanket data licence is asserted. Original currencies and procurement terms are preserved; costs are nominal and not directly comparable across currencies, delivery terms or clinical indications. The 2026 UNICEF records are partial and older USDA Q4 reporting scope is unconfirmed. Not operational or clinical guidance.

## Related research

FamineWatch documents famine events; HumanitarianNutrition documents the history and economics of nutrition interventions; TherapeuticProvisioning explores resource allocation under constraints.
