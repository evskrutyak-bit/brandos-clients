# DEPLOY-NOTES — Loft Hub

Дата: 2026-06-03

## Remote

- Repository: `https://github.com/evskrutyak-bit/brandos-clients.git`
- Branch: `main`
- Deploy commit: commit containing this file. Exact hash is reported in the handoff after push and live QC.

## Scope

### M2 v1.3 wave

Published the M2 client-facing synthesis layer v1.3, then replaced the M2-06 KARTINA apex artifact with its v1.3 HTML. The paired Deep Research originals remain as the source layer. Source MD artifacts were not changed.

Files:

- `loft-prostranstvo/M2/M2-01-RYNOK-RF-GIPOTEZY-v1.3.html`
- `loft-prostranstvo/M2/M2-02-RYNOK-MIR-GIPOTEZY-v1.3.html`
- `loft-prostranstvo/M2/M2-03-TSA-GIPOTEZY-v1.3.html`
- `loft-prostranstvo/M2/M2-04-PRODUKT-GIPOTEZY-v1.3.html`
- `loft-prostranstvo/M2/M2-05-KONKURENTY-GIPOTEZY-v1.3.html`
- `loft-prostranstvo/M2/M2-06-KARTINA.html`
- `loft-prostranstvo/M2/M2-01-RYNOK-RF-DR.html`
- `loft-prostranstvo/M2/M2-02-RYNOK-MIR-DR.html`
- `loft-prostranstvo/M2/M2-03-TSA-DR.html`
- `loft-prostranstvo/M2/M2-04-PRODUKT-DR.html`
- `loft-prostranstvo/M2/M2-05-KONKURENTY-DR.html`
- `loft-prostranstvo/index.html`

The Hub index now points the five M2 synthesis cards to the v1.3 files, keeps the M2-06 KARTINA card on `M2/M2-06-KARTINA.html`, and keeps a separate Deep Research sub-grid for the five paired DR pages.

Because the deployed module files live at `loft-prostranstvo/M2/*.html`, Hub return links in the deployed copies use `../index.html`. DR links are sibling file names.

### M3 wave

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
├── M2/
│   ├── M2-01-RYNOK-RF-GIPOTEZY-v1.3.html
│   ├── M2-01-RYNOK-RF-DR.html
│   ├── M2-02-RYNOK-MIR-GIPOTEZY-v1.3.html
│   ├── M2-02-RYNOK-MIR-DR.html
│   ├── M2-03-TSA-GIPOTEZY-v1.3.html
│   ├── M2-03-TSA-DR.html
│   ├── M2-04-PRODUKT-GIPOTEZY-v1.3.html
│   ├── M2-04-PRODUKT-DR.html
│   ├── M2-05-KONKURENTY-GIPOTEZY-v1.3.html
│   ├── M2-05-KONKURENTY-DR.html
│   └── M2-06-KARTINA.html
└── M3/
    ├── M3-01-YADRO-PRODUKTA.html
    ├── M3-02-ARKHITEKTURA-LINEYKI.html
    ├── M3-03-LESTNITSA-PRODUKTOV.html
    ├── M3-04-TSENY.html
    ├── M3-05-GIPOTEZY.html
    ├── M3-06-TREBOVANIYA.html
    └── M3-07-RISKI.html
```

Because the deployed module files live at `loft-prostranstvo/M2/*.html` and `loft-prostranstvo/M3/*.html`, Hub return links in the deployed copies use `../index.html`.

## Index

The Hub index contains the M3 module block with 7 cards and links to `M3/*.html`.

The public hero slogan `Без хаоса, по уму` was removed from the Hub main page because it is banned as a client-facing slogan. During the M3 wave, M2 was not changed; the later M2 v1.3 waves updated the five synthesis cards and then M2-06 KARTINA.

## Remaining M2 Plan

M2-01..06 client-facing synthesis pages are now v1.3 on the Hub. The paired DR pages intentionally remain on the old research template as source originals.

Remaining M2 work:

1. Optionally migrate DR pages to v1.3 later if the source layer also needs visual unification.
2. Run future M2 v1.1 content calibration after AmoCRM data arrives.
