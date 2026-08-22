# SmartData

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

SmartData is a hosted drone-data workspace built and operated by **National Drones**, a CASA
ReOC holder and Registered Training Organisation headquartered at Level 34, 1 Eagle Street,
Brisbane, Australia. Teams bring processed, viewer-ready outputs from DJI Terra, Agisoft
Metashape or their own photogrammetry workflow into SmartData and share one secure browser
workspace where clients and asset owners can inspect, measure, compare and sign off on the
data instead of passing files around.

> **Correction, 2026-08-14.** Until this date this repository described a fictional company —
> "Smart Data", a data enrichment / integration / data quality API vendor with three invented
> APIs whose documentation URLs (`www.smart-data.com/docs/*`) have never existed and return
> 404. That scaffold, and the plans / rate-limits / FinOps artifacts derived from it, have been
> removed and rebuilt from the real company's own public pages. See `x-provenance-note` in
> `apis.yml`.

## Overview

- **BYO data hosting** — host processed packages: orthomosaic hosted views, Cesium 3D Tiles,
  tiled point clouds, packaged Gaussian Splat views. Raw project folders, raw photos and loose
  GeoTIFF / LAS / LAZ / OBJ / FBX files are not direct uploads and are quoted separately.
- **Inspection AI** — AI-assisted review for towers, poles, solar, roofs, structures and linear
  assets, with detections, confidence, crops, annotations, status and evidence exports.
- **Multi-view asset context** — move between 2D maps, 3D models, point clouds, Gaussian Splat,
  thermal and source photos without losing asset context.
- **Measurements and change** — distance, area, volume, stockpiles, terrain, vegetation
  proximity, and change between repeat captures.
- **Teams and governance** — shared workspaces, roles, review status, notifications and secure
  access controls.
- **Emerging workflows** — DJI L3 processing (early access), Elios confined-space data
  (operational), photogrammetry engine (in development), Gaussian splatting (preview),
  powerline analytics (scoped pilots), forestry intelligence (active buildout).

Industries served: power and utilities, telecommunications, mining and resources, forestry and
environment, infrastructure and construction.

## APIs

**None.** SmartData publishes no public API, developer portal, SDK, webhook surface or
machine-readable contract. Probed 2026-08-14: the 50-URL sitemap on `www.smart-data.com` has no
`/docs`, `/api` or `/developers` page; `api.` / `docs.` / `developer.` subdomains do not resolve
on either `smart-data.com` or `ndsmartdata.com`; and the only machine surface that exists is the
Django REST backend the web application itself calls at `https://app.ndsmartdata.com/api/v1/`,
which is undocumented, unmarketed, and answers anonymous callers with HTTP 403
`{"detail":"Authentication credentials were not provided."}`.

## Try it

A public demo sandbox — the live SmartData viewer loaded with sample inspection and asset data,
no signup — is at [demo.ndsmartdata.com](https://demo.ndsmartdata.com/).

## Pricing

Published in AUD and metered by hosted dataset count and seats. Storage is a stated fair-use
allowance; overage is reviewed manually rather than billed automatically.

| Plan | Price | Hosted datasets | Storage | Seats |
|---|---|---|---|---|
| BYO Dataset Pass | AUD 149/year | 1 | 50 GB | 2 |
| BYO Starter | AUD 249/year | 3 | 150 GB | 5 |
| BYO Pro | AUD 249/month | 15 | 500 GB | 10 |
| BYO Enterprise | Custom | Custom / unlimited | 5 TB baseline | Custom / unlimited |

## Tags

Drone Data, Geospatial, Asset Inspection, Photogrammetry, LiDAR, Point Cloud, 3D Visualization,
Gaussian Splatting, Computer Vision, Infrastructure, Utilities, Mining, Forestry, Australia

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
