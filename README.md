# Currencylayer

Currencylayer is a real-time and historical foreign exchange rate JSON API delivering bank-grade exchange rate data for 168 world currencies and precious metals, sourced from 15+ commercial-grade providers. The service is delivered through the APILayer marketplace under a freemium subscription model with refresh cadence ranging from hourly on Free up to 60 seconds on Enterprise tiers.

- **APIs.yml:** [apis.yml](apis.yml)
- **Website:** https://currencylayer.com
- **Documentation:** https://docs.apilayer.com/currencylayer/docs/api-documentation
- **API Reference:** https://apilayer.com/marketplace/currency_data-api
- **Parent provider:** APILayer

## Type and Tier

- **x-type:** company
- **x-tier:** 3 (bulk-registered from public-apis)
- **x-parent:** apilayer
- **Source:** [public-apis/public-apis](https://github.com/public-apis/public-apis) &mdash; category: Currency Exchange

## API Surface

| Method | Endpoint | Summary | Min Plan |
|---|---|---|---|
| GET | `/list` | List Supported Currencies | Free |
| GET | `/live` | Get Live Exchange Rates | Free |
| GET | `/historical` | Get Historical Exchange Rates | Free |
| GET | `/convert` | Convert Currency Amount | Basic |
| GET | `/timeframe` | Get Time-Frame Exchange Rates | Enterprise |
| GET | `/change` | Get Currency Change Data | Enterprise Plus |

Base URL: `https://api.apilayer.com/currency_data` &middot; Auth: `apikey` header (modern) or `access_key` query (legacy).

## Artifacts

### Contract
- [openapi/currencylayer-openapi.yml](openapi/currencylayer-openapi.yml) &mdash; full OpenAPI 3.0 contract with all six operations and the success/error envelope.

### Schemas
- [json-schema/currencylayer-quotes-schema.json](json-schema/currencylayer-quotes-schema.json)
- [json-schema/currencylayer-currencies-schema.json](json-schema/currencylayer-currencies-schema.json)
- [json-schema/currencylayer-convert-schema.json](json-schema/currencylayer-convert-schema.json)
- [json-schema/currencylayer-timeframe-schema.json](json-schema/currencylayer-timeframe-schema.json)
- [json-schema/currencylayer-change-schema.json](json-schema/currencylayer-change-schema.json)
- [json-schema/currencylayer-error-schema.json](json-schema/currencylayer-error-schema.json)

### JSON Structure
- [json-structure/currencylayer-quotes-structure.json](json-structure/currencylayer-quotes-structure.json)
- [json-structure/currencylayer-currencies-structure.json](json-structure/currencylayer-currencies-structure.json)
- [json-structure/currencylayer-convert-structure.json](json-structure/currencylayer-convert-structure.json)
- [json-structure/currencylayer-timeframe-structure.json](json-structure/currencylayer-timeframe-structure.json)
- [json-structure/currencylayer-change-structure.json](json-structure/currencylayer-change-structure.json)

### JSON-LD Context
- [json-ld/currencylayer-context.jsonld](json-ld/currencylayer-context.jsonld) &mdash; semantic mapping for the Currencylayer response envelope.

### Examples
- [examples/currencylayer-listcurrencies-example.json](examples/currencylayer-listcurrencies-example.json)
- [examples/currencylayer-getlive-example.json](examples/currencylayer-getlive-example.json)
- [examples/currencylayer-gethistorical-example.json](examples/currencylayer-gethistorical-example.json)
- [examples/currencylayer-convertcurrency-example.json](examples/currencylayer-convertcurrency-example.json)
- [examples/currencylayer-gettimeframe-example.json](examples/currencylayer-gettimeframe-example.json)
- [examples/currencylayer-getchange-example.json](examples/currencylayer-getchange-example.json)

### Spectral Rules
- [rules/currencylayer-rules.yml](rules/currencylayer-rules.yml) &mdash; enforces operationId / summary / Title Case / Currencylayer envelope / `apikey` auth conventions.

### Naftiko Capabilities
- [capabilities/shared/currencylayer-shared.yaml](capabilities/shared/currencylayer-shared.yaml) &mdash; per-API operation primitives with plan gating.
- [capabilities/currency-conversion.yaml](capabilities/currency-conversion.yaml) &mdash; convert an amount with `/live` fallback.
- [capabilities/historical-rate-lookup.yaml](capabilities/historical-rate-lookup.yaml) &mdash; point-in-time rate lookup for reconciliation and audit.
- [capabilities/treasury-reporting.yaml](capabilities/treasury-reporting.yaml) &mdash; daily window FX exposure report via `/timeframe` + `/change`.
- [capabilities/ecommerce-multi-currency-pricing.yaml](capabilities/ecommerce-multi-currency-pricing.yaml) &mdash; storefront price localization with caching.

### Vocabulary
- [vocabulary/currencylayer-vocabulary.yml](vocabulary/currencylayer-vocabulary.yml) &mdash; resources, endpoints, parameters, capabilities, commercial dimensions, and data sources.

### Commercial & FinOps
- [plans/currencylayer-plans-pricing.yml](plans/currencylayer-plans-pricing.yml) &mdash; Free, Basic ($14.99), Professional ($39.99), Enterprise ($59.99), Enterprise Plus ($99.99), Custom.
- [rate-limits/currencylayer-rate-limits.yml](rate-limits/currencylayer-rate-limits.yml) &mdash; monthly quotas, overage policy, freshness cadence.
- [finops/currencylayer-finops.yml](finops/currencylayer-finops.yml) &mdash; FOCUS mapping, allocation tags, optimization plays.

## Plan and Feature Gating

| Plan | Price (mo) | Requests/mo | Refresh | HTTPS | Source Switching | /convert | /timeframe | /change |
|---|---|---|---|---|---|---|---|---|
| Free | $0 | 100 | Hourly | No | No (USD) | No | No | No |
| Basic | $14.99 | 10,000 | Hourly | Yes | Yes | Yes | No | No |
| Professional | $39.99 | 100,000 | 10-min | Yes | Yes | Yes | No | No |
| Enterprise | $59.99 | 100,000 | 60-sec | Yes | Yes | Yes | Yes | No |
| Enterprise Plus | $99.99 | 500,000 | 60-sec | Yes | Yes | Yes | Yes | Yes |
| Custom | Contact | Volume | 60-sec | Yes | Yes | Yes | Yes | Yes |

Overage pricing per request: Basic $0.005996 &middot; Professional / Enterprise $0.0023996 &middot; Enterprise Plus $0.00079992 &middot; Custom negotiated. Annual billing offers ~10-15% effective savings.

## Authentication

Currencylayer supports two authentication surfaces:

| Surface | Endpoint | Mechanism |
|---|---|---|
| Modern (recommended) | `https://api.apilayer.com/currency_data/*` | `apikey` HTTP header |
| Legacy | `https://api.currencylayer.com/*` (and `http://` on Free) | `access_key=` query parameter |

## Error Envelope

```json
{
  "success": false,
  "error": {
    "code": 104,
    "type": "monthly_usage_limit_reached",
    "info": "Your monthly API request volume has been reached. Please upgrade your Subscription Plan."
  }
}
```

Known codes: 101 (invalid key), 103 (no such function), 104 (quota exceeded), 105 (plan does not include feature), 106 (no results), 404 (not found).

## Tags

Currency Exchange, Foreign Exchange, FX, Forex, Conversion, Historical Rates, Time Frame, Change Report, Precious Metals, APILayer, Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## Maintainers

- **Kin Lane** &mdash; kin@apievangelist.com
