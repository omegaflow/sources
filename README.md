# omegaflow/sources

Static source catalogs for the **omegaflow** spatial field system: pre-built, machine-readable
assets that the system loads into its ICRS/J2000 frame.

## Layout

- `data/` — a small set of frequently used catalogs (orbits, masses, NDBC buoys, …) as JSON/CSV.
- **Releases** — the bulk: one release per upstream netloc (e.g. `psl.noaa.gov`,
  `geomag.usgs.gov`), each holding that source's assets. Measured 2026-10-09: **339 releases,
  12,333 asset files, ~1.76 TB**.
- `NOTICE` — the licence position.

## Licences

The data are **not** under a single licence: each source keeps its own. The per-source licence is
recorded in the parent repository (`omegaflow/omegaflow`) in the register `phi/sources.φ` — every
source block carries `terms <SPDX-token> <licence-url>` (e.g. `terms CC-BY-4.0 https://…`).

Reuse must follow the upstream source's licence and acknowledgement terms. If you are a rights
holder and believe a mirrored asset exceeds your terms, write to `code@omegaflow.space` naming the
asset — we remove it from the CDN and from the manifest. Sources whose terms state that
redistribution is restricted (`ohne-lizenz`) are not mirrored.

## Refresh

The catalog refresh is **pending a Rust port**. This repository carries no Python: the former
Python scripts (`refresh_all.py`, `tap_downloader.py`, `gaia_downloader.py`) and the workflow that
called them were removed. Until the port lands, the release assets are the durable record.

The omegaflow project's own source code is licensed separately — PolyForm NonCommercial +
ShareAlike for `src/`, CC BY-NC-SA elsewhere — in [`omegaflow/omegaflow`](https://github.com/omegaflow/omegaflow).
