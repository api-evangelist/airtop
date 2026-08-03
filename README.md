# Airtop (airtop)

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

Airtop is a cloud-browser API for AI agents. It runs remote Chromium sessions in the cloud and exposes them through a REST API so agents can open windows, navigate pages, and interact with sites using natural-language instructions - clicking, typing, scraping, and querying pages with AI - without brittle selectors or self-hosted browser infrastructure.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/airtop/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/airtop/refs/heads/main/apis.yml)

## Tags

- Browser Automation
- AI Agents
- Cloud Browser
- Web Scraping
- Headless Chrome

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Airtop Sessions API

Creates and manages cloud browser sessions - remote Chromium instances with optional profiles, proxies, recording, captcha solving, and idle timeouts. Returns CDP and WebDriver connection URLs for the live session.

- **Human URL:** [https://docs.airtop.ai/api-reference/airtop-api](https://docs.airtop.ai/api-reference/airtop-api)
- **Base URL:** `https://api.airtop.ai/api/v1`

#### Tags

- Sessions
- Cloud Browser
- Lifecycle

#### Properties

- [Documentation](https://docs.airtop.ai/guides/how-to/creating-a-session)
- [API Reference](https://docs.airtop.ai/api-reference/airtop-api/sessions/create)
- [OpenAPI](openapi/airtop-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/airtop.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/airtop.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Airtop Windows API

Creates browser windows (tabs) inside a session, loads URLs, reads window info, and closes windows. A window is the unit that pages load into and that page-interaction and AI-query operations act on.

- **Human URL:** [https://docs.airtop.ai/api-reference/airtop-api/windows/create](https://docs.airtop.ai/api-reference/airtop-api/windows/create)
- **Base URL:** `https://api.airtop.ai/api/v1`

#### Tags

- Windows
- Navigation
- Tabs

#### Properties

- [Documentation](https://docs.airtop.ai/api-reference/airtop-api/windows/create)
- [API Reference](https://docs.airtop.ai/api-reference/airtop-api)
- [OpenAPI](openapi/airtop-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/airtop.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/airtop.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Airtop Page Interaction API

Drives a page using natural-language element descriptions instead of selectors or XPaths - click, hover, type, and scroll. AI resolves the described element to an on-page target before performing the action.

- **Human URL:** [https://docs.airtop.ai/guides/how-to/ai/page-interactions](https://docs.airtop.ai/guides/how-to/ai/page-interactions)
- **Base URL:** `https://api.airtop.ai/api/v1`

#### Tags

- Page Interaction
- Click
- Type
- Scroll

#### Properties

- [Documentation](https://docs.airtop.ai/guides/how-to/ai/page-interactions)
- [API Reference](https://docs.airtop.ai/api-reference/airtop-api/windows/click)
- [OpenAPI](openapi/airtop-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/airtop.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/airtop.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Airtop AI Query and Extraction API

Asks natural-language questions about the current page (page-query), extracts structured data against an optional JSON output schema, follows pagination links for paginated extraction, and scrapes raw page content.

- **Human URL:** [https://docs.airtop.ai/api-reference/airtop-api/windows/page-query](https://docs.airtop.ai/api-reference/airtop-api/windows/page-query)
- **Base URL:** `https://api.airtop.ai/api/v1`

#### Tags

- AI Query
- Extraction
- Scraping

#### Properties

- [Documentation](https://docs.airtop.ai/api-reference/airtop-api/windows/page-query)
- [API Reference](https://docs.airtop.ai/api-reference/airtop-api/windows/paginated-extraction)
- [OpenAPI](openapi/airtop-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/airtop.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/airtop.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Airtop Screenshots API

Captures a screenshot of the current state of a window for visual inspection, debugging, or feeding back into a vision-capable agent loop.

- **Human URL:** [https://docs.airtop.ai/api-reference/airtop-api](https://docs.airtop.ai/api-reference/airtop-api)
- **Base URL:** `https://api.airtop.ai/api/v1`

#### Tags

- Screenshots
- Visual

#### Properties

- [Documentation](https://docs.airtop.ai/api-reference/airtop-api)
- [OpenAPI](openapi/airtop-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/airtop.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/airtop.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Airtop Profiles API

Persists browser state (cookies, local storage, logged-in sessions) into named profiles that can be saved when a session terminates and loaded into future sessions, and deletes profiles when no longer needed.

- **Human URL:** [https://docs.airtop.ai/api-reference/airtop-api](https://docs.airtop.ai/api-reference/airtop-api)
- **Base URL:** `https://api.airtop.ai/api/v1`

#### Tags

- Profiles
- Persistence
- Authentication

#### Properties

- [Documentation](https://docs.airtop.ai/api-reference/airtop-api)
- [OpenAPI](openapi/airtop-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/airtop.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/airtop.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/airtop-ai)
- [LinkedIn](https://www.linkedin.com/company/airtop-ai)
- [Website](https://www.airtop.ai)
- [Documentation](https://docs.airtop.ai)
- [Plans](plans/airtop-plans-pricing.yml)
- [Rate Limits](rate-limits/airtop-rate-limits.yml)
- [Fin Ops](finops/airtop-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
