# Lloyd's of London

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

Lloyd's of London is the world's specialist insurance and reinsurance market, operating as a regulated marketplace rather than as a carrier: the Corporation of Lloyd's oversees syndicates, managing agents, brokers and coverholders who underwrite property, casualty, marine, aviation, energy, cyber, political risk and reinsurance business on a subscription basis from its home market in the United Kingdom. Its API posture reflects that role. Lloyd's is a standards and market-infrastructure publisher first — the Core Data Record (CDR), the Market Reform Contract (MRC), coverholder and delegated claims reporting standards, and Blueprint Two digital processing requirements — and its technical surface is aimed at brokers, syndicates and market vendors, not at outside developers. Lloyd's ran a public API Development Portal at developer.lloyds.com (the "API Factory", BETA from June 2020) that published a Base API Standard and a catalogue of three market APIs: Placing — Submission and Quote, Placing — Firm Order, and RPAC for delegated authority risk, premium and claims. That portal now redirects to www.lloyds.com and no replacement self-serve developer portal is published. Production access to the underlying London Market API gateway (https://api.londonmarketgroup.co.uk) has always been partner-gated: an organisation must be onboarded to LIMOSS Common Services, registered in the Common Services Azure Active Directory tenant, and register an X.509 certificate before it can call anything. There is no public, self-serve Lloyd's API, no public sandbox and no public downloadable specification reachable today — the honest record for this market body is documentation-and-standards-first. What Lloyd's does still operate, verified by live probe, is a genuine gated API estate: three isolated gateway environments (Sandbox, PreProd, Production), an OpenID Connect discovery document and JWKS published on each, and a routed Catastrophe Codes v1 endpoint whose unauthenticated /health meta resource answers 200 while its data resources return 401 "Client certificate is missing". Its most reusable public artifact is the Lloyd's Base API Standard — a normative RFC 2119 document fixing the resource model, query grammar, collection and error envelopes, versioning compatibility rules and the dual mutual-TLS + JWT security model for every API published to the market.

**Areas:** Insurance · United Kingdom · Reinsurance · Specialty Insurance · London Market · Underwriting · Claims · Delegated Authority · Brokerage · Market Infrastructure · Standards · ACORD

## Lloyd's of London on APIs.io

Everything profiled for Lloyd's of London is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/lloyds-of-london/](https://apis.io/providers/lloyds-of-london/)** — or go straight to one of the APIs or properties below.

### APIs (4)

- [Lloyd's Placing API - Submission and Quote v1](https://apis.io/apis/lloyds-of-london/lloyds-placing-api-submission-and-quote/) — Market API for electronic placement in the London subscription market — create submissions and submission versions, upload Market Reform Contract and quote…
- [Lloyd's Placing API - Firm Order](https://apis.io/apis/lloyds-of-london/lloyds-placing-api-firm-order/) — Second Placing API listed in the Lloyd's API catalogue, described by Lloyd's as "Finalise Placings, Bind Risks, Sign Transactions" — the BIND verb of the…
- [Lloyd's RPAC API (Risk, Premium and Claims)](https://apis.io/apis/lloyds-of-london/lloyds-rpac-api/) — Third API listed in the Lloyd's API catalogue, described by Lloyd's as "Submit Risk, Premium and Claims details for Delegated Authority Placements" — the…
- [Lloyd's Catastrophe Codes API v1](https://apis.io/apis/lloyds-of-london/lloyds-catastrophe-codes-api/) — Lloyd's catastrophe event reference data served from the London Market API Gateway — the market's canonical codes for aggregating losses to a named…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Examples (22)

Example requests and responses.

- [Lloyds Of London Catastrophecodes Collection](https://apis.io/examples/lloyds-of-london/lloyds-of-london-catastrophecodes-collection/)
- [Lloyds Of London Catastrophecodes Singleton](https://apis.io/examples/lloyds-of-london/lloyds-of-london-catastrophecodes-singleton/)
- [Lloyds Of London Error Document](https://apis.io/examples/lloyds-of-london/lloyds-of-london-error-document/)
- [Lloyds Of London Identity Document](https://apis.io/examples/lloyds-of-london/lloyds-of-london-identity-document/)
- [Lloyds Of London Placing Brokerdepartment Collection](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-brokerdepartment-collection/)
- [Lloyds Of London Placing Submission Collection](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submission-collection/)
- [Lloyds Of London Placing Submission Get](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submission-get/)
- [Lloyds Of London Placing Submission Post Request](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submission-post-request/)
- [Lloyds Of London Placing Submission Post Response](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submission-post-response/)
- [Lloyds Of London Placing Submission Put Request](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submission-put-request/)
- [Lloyds Of London Placing Submission Put Response](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submission-put-response/)
- [Lloyds Of London Placing Submissiondialogue Quote Request](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submissiondialogue-quote-request/)
- [Lloyds Of London Placing Submissiondialogue Quote Response](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submissiondialogue-quote-response/)
- [Lloyds Of London Placing Submissiondialogue Rfq Request](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submissiondialogue-rfq-request/)
- [Lloyds Of London Placing Submissiondialogue Rfq Response](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submissiondialogue-rfq-response/)
- [Lloyds Of London Placing Submissiondocument Collection](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submissiondocument-collection/)
- [Lloyds Of London Placing Submissiondocument Post Request](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submissiondocument-post-request/)
- [Lloyds Of London Placing Submissiondocument Post Response](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submissiondocument-post-response/)
- [Lloyds Of London Placing Submissionunderwriter Post Request](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submissionunderwriter-post-request/)
- [Lloyds Of London Placing Submissionunderwriter Post Response](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-submissionunderwriter-post-response/)
- [Lloyds Of London Placing Underwriterorganisation Collection](https://apis.io/examples/lloyds-of-london/lloyds-of-london-placing-underwriterorganisation-collection/)
- [Lloyds Of London Version Document](https://apis.io/examples/lloyds-of-london/lloyds-of-london-version-document/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Lloyds Of London Authentication](https://apis.io/security/lloyds-of-london/lloyds-of-london-authentication/)
- [Lloyds Of London Domain Security](https://apis.io/security/lloyds-of-london/lloyds-of-london-domain-security/)
- [Lloyds Of London Vulnerability Disclosure](https://apis.io/security/lloyds-of-london/lloyds-of-london-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Lloyds Of London Scopes](https://apis.io/scopes/lloyds-of-london/lloyds-of-london-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.lloyds.com/)
- [Documentation](https://www.lloyds.com/market-resources/requirements-and-standards)
- [Support](https://www.lloyds.com/contact-us)
- [Blog](https://www.lloyds.com/news-and-insights)
- [Security](https://www.lloyds.com/security-reports)
- [Terms of service](https://www.lloyds.com/help/terms-and-conditions)
- [Privacy policy](https://www.lloyds.com/help/privacy)
- [GitHub](https://github.com/lloydsdigital)

## API Evangelist rating

**Kin Score 32.2** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 80.4 |
| Contract quality | 6.5 |
| Contract governance | 18.2 |
| Operational transparency | 28.9 |
| Developer ergonomics | 42.9 |
| Access clarity | 21.1 |

**Agent readiness 6.7** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 42.1** — Insurance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/lloyds-of-london/](https://apis.io/providers/lloyds-of-london/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Lloyd's of London: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/lloyds-of-london/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
