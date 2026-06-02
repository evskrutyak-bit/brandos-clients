# DEPLOY-NOTES — Loft M3 Hub

Дата: 2026-06-03

## Remote

- Repository: `https://github.com/evskrutyak-bit/brandos-clients.git`
- Branch: `main`
- Deploy commit: commit containing this file. Exact hash is reported in the handoff after push and live QC.

## Scope

Published only the HTML layer for M3. Source MD artifacts were not changed.

Files:

- `loft-prostranstvo/M3/M3-01-YADRO-PRODUKTA.html`
- `loft-prostranstvo/M3/M3-02-ARKHITEKTURA-LINEYKI.html`
- `loft-prostranstvo/M3/M3-03-LESTNITSA-PRODUKTOV.html`
- `loft-prostranstvo/M3/M3-04-TSENY.html`
- `loft-prostranstvo/M3/M3-05-GIPOTEZY.html`
- `loft-prostranstvo/M3/M3-06-TREBOVANIYA.html`
- `loft-prostranstvo/M3/M3-07-RISKI.html`
- `loft-prostranstvo/index.html`

## Structure

The Hub uses a flat module directory:

```text
loft-prostranstvo/
├── index.html
└── M3/
    ├── M3-01-YADRO-PRODUKTA.html
    ├── M3-02-ARKHITEKTURA-LINEYKI.html
    ├── M3-03-LESTNITSA-PRODUKTOV.html
    ├── M3-04-TSENY.html
    ├── M3-05-GIPOTEZY.html
    ├── M3-06-TREBOVANIYA.html
    └── M3-07-RISKI.html
```

Because the deployed files live at `loft-prostranstvo/M3/*.html`, Hub return links in the deployed copies use `../index.html`.

## Index

The Hub index contains the M3 module block with 7 cards and links to `M3/*.html`.

The public hero slogan `Без хаоса, по уму` was removed from the Hub main page because it is banned as a client-facing slogan. M2 was not changed.

## M2 Migration Plan

M2 remains on the old HTML generation. This deploy intentionally allows a temporary mixed Hub: old M0-M2 plus new M3 v1.3.

Separate M2 migration wave:

1. Inventory live M2 HTML and source files.
2. Rebuild only the HTML shell to v1.3, without changing artifact content.
3. Normalize Hub paths for `loft-prostranstvo/M2/*.html`.
4. Run the same live QC: 200 responses, Hub navigation, artifact navigation, `hero-loft`, print smoke.
5. Deploy M2 as a separate commit and record notes.
