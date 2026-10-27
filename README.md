# MISP Cookbook

<!-- ZQM-START -->
<!-- markdownlint-disable MD033 -->
<p align="center">
  <strong>ZQM Computing — Geospatial Engineering & Scientific Computing</strong><br>
  <a href="https://github.com/ZQM-Computing">ZQM Computing</a>
</p>
<!-- markdownlint-enable MD033 -->
<!-- ZQM-END -->

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

A **MISP cookbook** for threat-intelligence sharing platform, localhost-only deployment. Patterns are drawn from the ZQM fleet's MISP deployment on Node-3 via Docker, localhost-only. Deployment rules from the fleet: never run compose without all five secret environment variables, and re-apply the Authorization-header clone patch after upstream pulls, because the bundled nginx drops it. It is intended for Threat-intelligence teams who share indicators privately. Validate each pattern against your own data, software versions, and operating environment before adopting it.

## Repository role and status

**Status:** Active, public — seeding. Pattern passes land in follow-up work from fleet-verified setups; the tables below list what is planned, not what is already written.

**What this repository is:** MISP patterns — see the table below.

**What it contributes:** Part of the ZQM Computing geospatial portfolio. Intended to provide geospatial data feeds (POI, weather, satellite imagery, geocoding) for the ZQM game platform. The umbrella index for the series is [geospatial-cookbooks](https://github.com/ZQM-Computing/geospatial-cookbooks).

**Standing:** This repository is maintained independently. Automated checks cover only the paths and environments configured in its workflows; they do not establish production readiness or operational certification.

## Who this is for

Threat-intelligence teams who share indicators privately.

## Prerequisites

- MISP via Docker on a private host
- Five secret environment variables, kept out of repos
- A browser on the host for the UI passes

## Patterns (planned)

| # | Example | What it will demonstrate |
|---|---------|--------------------------|
| 01 | `01-docker-deploy` | Deploying MISP with all five secrets set |
| 02 | `02-nginx-auth-patch` | Re-applying the Authorization-header patch after pulls |
| 03 | `03-feed-ingest` | Ingesting feeds into events and attributes |
| 04 | `04-localhost-only` | Keeping the deployment private: bindings and firewall scope |

## Repository layout

```text
misp-cookbook/
├── examples/          # pattern passes, landing in follow-up work
├── README.md
└── LICENSE
```

## Roadmap

- First pattern pass: the first two table rows
- Second pass: the remaining rows, from fleet-verified setups

## Contributing

A contributing guide lands with the first pattern pass. Report security issues to <zqmcomputing@gmail.com> — please do not open a public issue for those.

## More from this series

- [spiderfoot-cookbook](https://github.com/ZQM-Computing/spiderfoot-cookbook) — Passive OSINT automation as a service
- [theharvester-cookbook](https://github.com/ZQM-Computing/theharvester-cookbook) — Passive reconnaissance: domains, emails, and hosts from public sources
- [nuclei-cookbook](https://github.com/ZQM-Computing/nuclei-cookbook) — Bounded, authorized template scanning
