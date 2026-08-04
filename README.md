# Lloyd's of London (lloyds-of-london)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Lloyd's of London is the world's specialist insurance and reinsurance market, operating as a regulated marketplace rather than as a carrier: the Corporation of Lloyd's oversees syndicates, managing agents, brokers and coverholders who underwrite property, casualty, marine, aviation, energy, cyber, political risk and reinsurance business on a subscription basis from its home market in the United Kingdom.

Its API posture reflects that role. Lloyd's is a standards and market-infrastructure publisher first — the Core Data Record (CDR), the Market Reform Contract (MRC), coverholder and delegated claims reporting standards, and Blueprint Two digital processing requirements — and its technical surface is aimed at brokers, syndicates and market vendors, not at outside developers. **There is no public, self-serve Lloyd's API today.**

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/lloyds-of-london/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/lloyds-of-london/refs/heads/main/apis.yml)

## Tags

- Insurance
- United Kingdom
- Reinsurance
- Specialty Insurance
- London Market
- Underwriting
- Claims
- Delegated Authority
- Broker
- Market Infrastructure
- Standards
- ACORD

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

### Lloyd's Placing API - Submission and Quote v1

Market API for electronic placement in the London subscription market — create submissions and submission versions, upload Market Reform Contract and quote documents, add carriers and underwriters to a submission, send requests for quote, and receive underwriter responses. Partner-gated to onboarded London Market organisations.

- **Human URL:** [https://developer.lloyds.com/placingsubmissionandquote-v1/Developer-Overview](https://developer.lloyds.com/placingsubmissionandquote-v1/Developer-Overview) (portal retired — redirects to www.lloyds.com)
- **Base URL:** `https://api.londonmarketgroup.co.uk/PPL/Lloyds/Placing/V1`

#### Properties

- [Documentation (archived Key Details)](https://web.archive.org/web/20210128061829/https://developer.lloyds.com/placingsubmissionandquote-v1/Key-Details-On-API)
- [API Reference (archived Technical Model)](https://web.archive.org/web/20210128055606/https://developer.lloyds.com/placingsubmissionandquote-v1/Technical-Model)
- [Base API Standard (archived)](https://web.archive.org/web/20200930095802/https://developer.lloyds.com/Get-Started/Base-API-Standard)
- [Authentication (archived)](https://web.archive.org/web/20200930085423/https://developer.lloyds.com/Get-Started/Authentication-Information)

### Lloyd's Placing API - Firm Order

"Finalise Placings, Bind Risks, Sign Transactions" — the bind verb for the London subscription market. Catalogue entry only; no public reference documentation or specification.

- **Human URL:** [Archived API catalogue](https://web.archive.org/web/20200610082013/https://developer.lloyds.com/Explore-Innovate)

### Lloyd's RPAC API (Risk, Premium and Claims)

"Submit Risk, Premium and Claims details for Delegated Authority Placements" — the delegated authority reporting path from coverholders and delegated claims administrators, aligned to Lloyd's Coverholder Reporting Standards and ACORD technical standards. Catalogue entry only; no public reference documentation or specification.

- **Human URL:** [Archived API catalogue](https://web.archive.org/web/20200610082013/https://developer.lloyds.com/Explore-Innovate)

## API Posture

- **Developer portal:** [developer.lloyds.com](https://developer.lloyds.com/) — a genuine Lloyd's API Development Portal ("API Factory", BETA from 8 June 2020) that published a Base API Standard, authentication guidance and a three-API catalogue. It is retired: HTTPS does not complete a connection, HTTP 301s to www.lloyds.com, and Internet Archive captures show the redirect from April 2024 onward. No replacement portal is published.
- **OpenAPI:** one Swagger/OpenAPI 3.0 file was documented for the Placing API v1.10 but is unreachable and unarchived. **No specifications harvested — no `openapi/` directory in this repo.**
- **Auth:** OAuth 2.0 / OpenID Connect via Azure Active Directory (JWT, on-behalf-of flow, service accounts, `user_impersonation` scope) plus a registered X.509 certificate per LIMOSS environment. Never self-serve.
- **Onboarding:** LIMOSS Common Services onboarding, per-environment guesting (Sandbox / PreProd / Production), Azure AD application registration.
- **ACORD:** ACORD-aligned market standards body — the CDR and Coverholder Reporting Standards align to ACORD technical standards, Lloyd's funds free ACORD membership for all coverholders, and ACORD mapped its standards to the Lloyd's API Factory placement specifications in June 2020.
- **Webhooks / AsyncAPI:** none. The Base API Standard explicitly places message-originated and publish-subscribe interfaces out of scope.
- **Postman / GraphQL / gRPC:** none published.

## Standards and Market Resources

- [Requirements and Standards](https://www.lloyds.com/market-resources/requirements-and-standards)
- [Core Data Record](https://www.lloyds.com/market-resources/requirements-and-standards/core-data-record)
- [Coverholder and Delegated Claims Reporting Standards](https://www.lloyds.com/market-resources/delegated-authorities/market-knowledge/reporting-standards)
- [ACORD membership for coverholders](https://www.lloyds.com/insights/news/lloyds-provides-acord-membership-for-all-coverholders)
- [Lloyd's Insights Hub](https://insights.lloyds.com/) — registration-gated; hosts a CDR glossary data feed described as available via an API
- [Crystal+](https://crystalplus.lloyds.com/home) — international regulatory and tax requirements database (login)
- [Delegated Data Manager (DDM)](https://www.lloyds.com/market-resources/tools/delegated-data-manager/faqs) — market bordereaux service via LIMOSS

## Links

- **Website:** [https://www.lloyds.com/](https://www.lloyds.com/)
- **GitHub:** [lloydsdigital](https://github.com/lloydsdigital) (0 public repos) · [LloydsOfLondon](https://github.com/LloydsOfLondon) (0 public repos)
