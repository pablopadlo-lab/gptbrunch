---
layout: post
title: "The Real Price of S3-Compatible Storage: 13 Providers Compared (Sep 2026)"
date: 2026-09-07
canonical_url: https://aggregation.marketplace/storage
---

# The Real Price of S3-Compatible Storage: 13 Providers Compared (Sep 2026)

Object storage pricing looks simple until you line up 13 providers on one screen. The same S3 API sells for **$4.36/TB/mo** at one end and **$29.74/TB/mo** at the other. And the list price is only half the story — egress policy, retention minimums, API fees, and object-lock support decide the actual bill.

This is a live snapshot from the aggregation.marketplace storage tracker: **13 providers, 26 configurations, updated hourly**, with prices in their native units (no fake normalization) and egress shown as the real policy.

![Storage listings overview](https://pablopadlo-lab.github.io/gptbrunch/assets/storage-hero-2026-09-07.png)

## What the tracker covers

- **13 providers**: Backblaze, Wasabi, Storj, Cloudflare R2, OVHcloud, Hetzner, IDrive e2, Rabata, Alibaba OSS, Huawei OBS, Yandex, Selectel, Cloud.ru.
- **26 configurations** across hot, cold/IA, and archive classes.
- Prices kept in their native unit: $/TB/mo, $/TB-yr contracts, $49/10TB blocks.
- Egress as the real policy — unconditional free, fair-use ratio, or paid per-TB.
- Badges for annual/hourly billing, retention windows, minimums, and per-operation API fees.

## Class floors right now

The cheapest live plan per provider and class (green = cheaper within class; dashed cells = block/annual tariffs, not ranked):

![Storage price heatmap: provider × class](https://pablopadlo-lab.github.io/gptbrunch/assets/storage-heatmap-2026-09-07.png)

- **Hot from $5.00/TB/mo** — IDrive e2 (Veeam/MSP/reseller tier)
- **Cold / IA from $4.36/TB/mo** — OVHcloud Infrequent Access
- **Archive from $4.91/TB/mo** — Alibaba OSS Archive (LRS, CN)

The spread inside a single class is enormous: hot storage runs from **$5.00 (IDrive)** to **$29.74 (Selectel S3 standard)** — a 6× gap between S3-compatible vendors. Among global options with solid guarantees, Backblaze B2 at **$6.95** and Storj at **$7.00** stay the cheapest hot plans.

## Cheapest live plans, sorted by price

| Provider | Plan | Class | Price | Region |
|---|---|---|---|---|
| OVHcloud | Object Storage Infrequent Access (30-day retention) | cold | $4.36/TB/mo | us |
| Alibaba Cloud OSS | OSS Archive (LRS, CN) | archive | $4.91/TB/mo | cn |
| IDrive e2 | e2 Veeam/MSP/Reseller (monthly) | hot | $5.00/TB/mo | global |
| IDrive e2 | e2 Standard (pay-as-you-go) | hot | $6.00/TB/mo | global |
| Backblaze | B2 Cloud Storage | hot | $6.95/TB/mo | global |
| Storj | Object Storage Standard | hot | $7.00/TB/mo | global |
| Yandex | Object Storage ICE (RU, min 12 mo) | archive | $7.35/TB/mo | ru |
| Wasabi | Hot Cloud Storage (90-day retention) | hot | $7.99/TB/mo | global |
| Hetzner | Object Storage (1 TB incl.) | hot | $7.99/TB/mo | eu |
| OVHcloud | Object Storage Standard (30-day retention) | hot | $8.11/TB/mo | us |
| Rabata | S3 Hot Storage | hot | $10.00/TB/mo | global |
| Cloudflare R2 | R2 Infrequent Access | cold | $10.00/TB/mo | global |
| Storj | Object Storage Advanced (US SOC2) | hot | $10.00/TB/mo | us |

![Live listings table sorted by price](https://pablopadlo-lab.github.io/gptbrunch/assets/storage-listings-2026-09-07.png)

## The fine print that changes the bill

**"Free egress" is three different products.** Unconditional free (OVHcloud, Cloudflare R2). Free up to a stored-volume ratio — Backblaze 3×, IDrive 3×, Wasabi 1:1 fair-use. Or paid per-TB — Storj at $7/TB, Rabata at $10/TB, and most RU/CN providers bill egress outright.

**Retention minimums are a hidden price.** Wasabi holds objects for 90 days, OVHcloud and Storj for 30, Yandex ICE for 365. Delete early and you still pay the full window. On churn-heavy workloads this doubles the effective per-TB cost.

**API fees invert "cheap" math.** Cloudflare R2 looks aggressive at $15/TB hot with zero egress — until you count per-operation charges (Class A $4.50/1M, Class B $0.36/1M) and notice R2 has no versioning and no object lock. Backblaze and Wasabi ship both features at lower storage prices.

**"—" means not disclosed, not supported.** Several CN and RU providers (Alibaba, Huawei, Cloud.ru) leave versioning and object lock undisclosed; the tracker marks them honestly instead of assuming.

![Provider constraints matrix: versioning, object lock, API fees, retention, egress](https://pablopadlo-lab.github.io/gptbrunch/assets/storage-constraints-2026-09-07.png)

## Bottom line

- **Cheapest hot S3-compatible, global, no gotchas**: Backblaze B2 at $6.95, Storj at $7.00.
- **Cheapest cold/IA**: OVHcloud Infrequent Access at $4.36 (30-day retention, free egress).
- **Cheapest archive**: Alibaba OSS Archive at $4.91 (CN region).
- **Zero-egress hot serving**: Cloudflare R2 at $15/TB — but budget the API operations and check whether you need object lock.
- **Backup/DR with heavy restores**: Rabata S3 Backup flat $49/10TB with no egress fees on restores — roughly $4.9/TB effective.

Prices refresh continuously. The full interactive view — heatmap, class floors, presets for S3-compatible / no-egress-fees / cold-archive filtering, and live listings — is at [aggregation.marketplace/storage](https://aggregation.marketplace/storage).
