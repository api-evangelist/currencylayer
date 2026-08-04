# Currencylayer (currencylayer)

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

Currencylayer is a real-time and historical foreign exchange rate JSON API delivering bank-grade exchange rate data for 168 world currencies and precious metals, sourced from 15+ commercial-grade providers. The service is delivered through the APILayer marketplace under a freemium subscription model with refresh cadence ranging from hourly on Free up to 60 seconds on Enterprise tiers.

**APIs.json:** [https://currencylayer.com](https://currencylayer.com)

## Tags

- Currency Exchange
- Foreign Exchange
- FX
- Forex
- Conversion
- Historical Rates
- Time Frame
- Change Report
- Precious Metals
- APILayer
- Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## APIs

### Currencylayer API

The Currencylayer REST API exposes six operations covering currency symbol discovery, real-time and historical rates, on-demand currency conversion, daily time-frame windows, and change reporting. Authentication is via the APILayer `apikey` header on the modern endpoint or the legacy `access_key` query parameter.

- **Human URL:** [https://currencylayer.com/documentation](https://currencylayer.com/documentation)
- **Base URL:** `https://api.apilayer.com/currency_data`

#### Tags

- Currency Exchange
- Foreign Exchange
- APILayer

#### Properties

- [Documentation](https://docs.apilayer.com/currencylayer/docs/api-documentation)
- [API Reference](https://apilayer.com/marketplace/currency_data-api)
- [Quickstart](https://docs.apilayer.com/currencylayer/docs/getting-started)
- [Authentication](https://docs.apilayer.com/currencylayer/docs/getting-started)
- [OpenAPI](openapi/currencylayer-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/currencylayer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/currencylayer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/currencylayer-quotes-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/currencylayer-currencies-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/currencylayer-convert-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/currencylayer-timeframe-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/currencylayer-change-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/currencylayer-error-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/currencylayer-quotes-structure.json)
- [JSON Structure](json-structure/currencylayer-currencies-structure.json)
- [JSON Structure](json-structure/currencylayer-convert-structure.json)
- [JSON Structure](json-structure/currencylayer-timeframe-structure.json)
- [JSON Structure](json-structure/currencylayer-change-structure.json)
- [J S O N- L D](json-ld/currencylayer-context.jsonld)
- [Example](examples/currencylayer-listcurrencies-example.json)
- [Example](examples/currencylayer-getlive-example.json)
- [Example](examples/currencylayer-gethistorical-example.json)
- [Example](examples/currencylayer-convertcurrency-example.json)
- [Example](examples/currencylayer-gettimeframe-example.json)
- [Example](examples/currencylayer-getchange-example.json)
- [Rate Limits](rate-limits/currencylayer-rate-limits.yml)
- [Pricing](plans/currencylayer-plans-pricing.yml)
- [SDK](https://github.com/said-ali/currencylayer)
- [SDK](https://github.com/phlegx/money-currencylayer-bank)
- [SDK](https://github.com/orkhanahmadov/laravel-currencylayer)
- [SDK](https://github.com/keymusicman/CurrencyLayer4NET)
- [SDK](https://github.com/jfayad/currencylayer)
- [Code Examples](https://github.com/apilayer/currencylayer-API)
- [Code Examples](https://github.com/apilayer/currency-converter-app)
- [Code Examples](https://github.com/apilayer/currency-conversion)

## Common Properties

- [Website](https://currencylayer.com)
- [Documentation](https://docs.apilayer.com/currencylayer/docs/api-documentation)
- [API Reference](https://apilayer.com/marketplace/currency_data-api)
- [Pricing](https://currencylayer.com/product)
- [Sign Up](https://apilayer.com/signup)
- [Login](https://apilayer.com/login)
- [Terms of Service](https://currencylayer.com/terms)
- [Privacy Policy](https://currencylayer.com/privacy)
- [Support](https://currencylayer.com/contact)
- [Blog](https://blog.apilayer.com/)
- [GitHub Organization](https://github.com/apilayer)
- [GitHub Repository](https://github.com/apilayer/currencylayer-API)
- [Public APIs Listing](https://github.com/public-apis/public-apis)
- [Spectral Rules](rules/currencylayer-rules.yml)
- [Vocabulary](vocabulary/currencylayer-vocabulary.yml)
- [Plans](plans/currencylayer-plans-pricing.yml)
- [Rate Limits](rate-limits/currencylayer-rate-limits.yml)
- [Fin Ops](finops/currencylayer-finops.yml)
- [Tools](https://blog.apilayer.com/how-to-turn-any-rest-api-into-an-mcp-server-for-claude-complete-2026-pillar-guide/)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
