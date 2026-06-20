# Airtop (airtop)

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
