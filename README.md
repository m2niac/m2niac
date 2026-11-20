# Mykhailo Hladchenko

**Software Architect · Team Lead · Full-stack Developer (PHP/Laravel) · Business-Process Automation & Infrastructure**

Lviv, Ukraine · [LinkedIn](https://www.linkedin.com/in/mhaldchenko/)

---

## Summary

Software architect / Team Lead / FullStack Developer with 20 years of experience who owns the whole cycle: **business analysis → system design → development → deployment → long-term operation**. I design and ship automation systems (ERP/CRM, customs, logistics, postal, healthcare, manufacturing) for regulated and high-stakes industries, and I run them in production on infrastructure I build myself. Currently contributing to the architecture and development of a hosting orchestration platform at **WebPros**; co-owner and CTO of **asign**, a company with 214+ delivered projects, 19+ of them business-automation systems.

## Core competencies

| | |
|---|---|
| **Architecture & design** | Domain modelling for complex ERP/CRM systems; layered service/repository architecture; saga-style pipelines with compensation; async processing; REST/GraphQL API design and versioning; ACL/authorization models; legacy-to-modern migrations with zero downtime |
| **Business analysis & client problem-solving** | Requirements discovery with non-technical stakeholders; mapping real business processes (warehouse, customs, fleet, clinics) into software; integration with government and third-party systems; estimation and scoping |
| **Deployment & operations** | Multi-tenant Docker platform; scripted provisioning with rollback; CI/CD; a fleet of servers across several providers |
| **Security, updates & backups** | Designed and run in-house services for fleet-wide security monitoring and central off-box backups with verification, rotation and alerting. Fleet-wide roll-outs of critical updates, server hardening, incident response and recovery of legacy servers |
| **Leadership** | Head of Development, team lead, technical audits, architecture reviews, mentoring |

## Technical skills

- **Backend:** PHP 4 → 8.4, vanilla PHP, Laravel, Symfony, Livewire, Filament, Drupal 7/8
- **Frontend:** TypeScript/JavaScript, Vue, React, vanilla JS / HTML / CSS
- **Data:** MySQL/MariaDB (incl. stored procedures), PostgreSQL, Redis, Meilisearch, BigQuery
- **APIs & integration:** REST, GraphQL, PASETO/JWT, Stripe, WHMCS, Zoho, Google Workspace, LDAP, QuickBlox, IceCast, postal and tax-authority APIs
- **Infrastructure:** Docker/Compose, Linux, nginx, Cloudflare, Proxmox VE, AWS, Bitbucket Pipelines/GitHub CI, Grafana/Loki
- **Quality & security:** PHPUnit, Larastan, Pint, authorization audits, ...
- **Tooling:** AI-assisted engineering (Claude Code) with project rules, hooks and QA gates

---

## Experience

### WebPros — Senior Full-stack Developer (R&D) (Mar 2025 – present)
*Hosting orchestration platform* (Laravel, PHP 8.4, Proxmox, AWS)

R&D role on a platform that automates the lifecycle of virtual machines and the hosting products installed on them, tied together by an orchestration API.

- **VM lifecycle automation:** automated provisioning of virtual machines on Proxmox clusters, networking, DNS/TLS and licensing; support of the whole VM fleet.
- **Product installation and updates:** unattended installation of products on VMs; automated updates of VMs and of the products on them.
- **Monitoring:** health and state tracking of VMs and installed products (Loki/Grafana).
- **Orchestration API (design and development):** synchronous and asynchronous API versions linking all of the above.
- **Architecture:** step-based provisioning pipeline with persisted state and rollback, async processing, strict layering.
- **Integrating systems without usable APIs.**

### asign — Co-owner & CTO (2006 – present)
Company building custom CRM/ERP and business-process automation; 214+ projects, own CMS and 30+ Filament plugins that I developed and maintain ([filamentphp.com/plugins?q=asign](https://filamentphp.com/plugins?q=asign)). I took part in every project in the portfolio and, on all automation systems except Jet-DP, I was the **sole** business analyst, architect, developer and DevOps engineer: from the first conversation with the client to production and support.

**Automation systems**

- **Duty-free warehouse automation, Poland** — *Laravel, Livewire, vanilla JS.* **Problem:** a warehouse in a duty-free zone must prove, to the gram, where every goods item came from and where it went, and the results must be independently auditable. **Business analysis:** mapped the customs procedures and the documents that drive them. **Designed:** a ledger built on incoming and outgoing customs documents; stock kept in kilograms; separate audit access for the supervising authority; immutable data with corrections made by new documents, never by edits; point-in-time inventory snapshots; automatic generation of customs and tax control documents. **Outcome:** links inbound and outbound movements to customs numbers and writes components off to production. Certified by the Polish tax system; in production since November 2023.
- **Jet-DP (jet-dp.pl) — parcel delivery Poland → Ukraine** — *Laravel, Livewire, vanilla JS.* Online ordering and payment, B2B and C2C data channels, warehouse receiving by barcode scan, automated customs/postal documents, tracking with customer notifications, integrations with InPost and Ukrposhta. **Challenges:** government APIs with strict rate limits (quota-aware call strategy), deferred sync for offline warehouse terminals. **My part:** designed the architecture and built the core of the system (~80% of the code); later handed part of the work to another developer.
- **Transportation company CRM/ERP** — fleet and spare parts, fuel, driver scheduling and payroll, multi-currency billing, automated EU toll payments, collision and idle-time analytics.
- **Photobook production automation (fotobookplus.com)** — product configurator with conditional rules, customer web constructor, production ERP; **in production since 2013**, local file storage at scale, no cloud dependency.
- **Business club CRM** — membership lifecycle, calls/email marketing, events, payments and loyalty; site and CRM decoupled via API.
- **Online radio platform (mjoyradio.com)** — IceCast broadcast, statistics proxy, web and mobile clients.
- **Cargo consolidator** — client portal for requests and documents plus back-office: warehouse receiving, grouping shipments into flights (kg and m³), tracking, notifications in the client's language.
- **Tour operator CRM** — website requests on a stage board, payments in six currencies converted to UAH, tours and prices maintained in the CRM and synced to the website automatically, duplicate-client merging.
- **Healthcare CRM** — field-level access rights, client cabinet where clinics and agencies place and track orders.
- **Internal accounting system** — PDF invoices and acts, automatic payment statuses, contractor payouts, monthly service accounting with margins, multi-currency.
- **In-house monitoring and backup services** — daily monitoring of servers and sites with alerts; central off-box backups with verification and rotation.

**Platform & infrastructure (own multisite hosting platform)**

- Designed one repository that provisions and operates both test and production environments across several providers: shared base images and services, per-site compose template; sites differ only by per-machine config, never by forked scripts.
- Scripted lifecycle (`create / deploy / destroy / backup`) with **self-rollback on failure**, serialized deploys, per-site private package credentials, isolation between tenants.
- **Security:** layered network protection, per-zone TLS, scoped credentials, integrity verification, nightly scanners; coordinated fleet-wide roll-outs of critical fixes and incident response on legacy servers.
- **Reliability:** scheduled backups with de-duplication and retention, off-box backup server, central monitoring, self-healing after infrastructure upgrades.
- Migrated live single-site stacks and legacy sites onto the platform with minutes of downtime; self-hosted private package registry.

### Artlabs — Senior Full-stack Developer (Feb 2024 – Feb 2025)
3D-artist/customer matching platform (Symfony, TypeScript, BigQuery, Cloudflare). Backend support and framework upgrades; data-parsing mechanism that bypasses blocking.

### Vector Software — Senior Full-stack Developer (Nov 2020 – Dec 2023)
- Introduced GraphQL beside REST without disrupting production; two app versions with different business processes on one backend.
- Stripe/QuickBlox finance and job portal; Zoho People ↔ Google Workspace ↔ LDAP synchronizer.
- Technical audits, architecture of new features, performance and fault-tolerance fixes; Laravel and Drupal migrations.

### JetSolutions — Head of Development (May 2019 – Oct 2020)
Led the team: estimation, planning, career development, architecture reviews, conflict resolution and office growth.

### abto (JustAnswer) — Senior Full-stack Developer (Aug 2017 – May 2019)
Drupal 7 → 8 migration of a large platform with zero downtime; Orange HRM extensions; help center with legacy React.

### EchoUA (Platinium Group Ticketing) — Senior Full-stack Developer (Feb – Aug 2017)
High-traffic ticketing for Formula 1/MotoGP; PHP 5 → 7 migration of production; PHP + Angular features.

### Earlier
System administrator, Company Aleks (1998–2008): Windows Server NT4–2008, network and service-centre infrastructure. Co-founder, **Steel Drum** conference series for sysadmins/DevOps (since 2008).

---

## Education

- M.Sc. Public Management — Lviv Polytechnic National University (LPNU), 2022–2024
- M.Sc. Project Management — LPNU, 2016–2017
- M.Sc. Software Engineering — LPNU, 2007–2009
- M.Sc. Biomedical Electronics — LPNU, 1998–2004

## Languages

Ukrainian (native) · English (upper-intermediate) · Polish (basic)
