# apipick-ip-geolocation

A [Claude Code](https://claude.ai/claude-code) skill that looks up geographic and network information for any IP address using the [apipick](https://www.apipick.com) IP Geolocation API.

## What it does

Given a public IPv4 or IPv6 address (or no address to look up your own), this skill returns:

- **Location** — country, continent, city, latitude/longitude
- **Timezone** — IANA timezone identifier
- **Currency** — ISO 4217 currency code for the country
- **Network** — ISP name and ASN number

Omit the IP address to look up the caller's own public IP.

## Requirements

An apipick API key is required. Get 100 free credits at [apipick.com](https://www.apipick.com).

## Installation

Install via Claude Code:

```bash
claude skills install https://github.com/apipick-lab/apipick-ip-geolocation
```

## Usage

Once installed, just ask Claude naturally:

- *"Where is the IP address 8.8.8.8 located?"*
- *"What country does 185.220.101.1 belong to?"*
- *"What's the ISP for IP 1.1.1.1?"*
- *"Look up my current IP location"*

Claude will call the apipick API and return the location and network details.

## API Reference

| Field | Value |
|-------|-------|
| Endpoint | `GET https://www.apipick.com/api/ip-geolocation` |
| Auth | `x-api-key` header |
| Cost | 1 credit per request |

See [`references/api_reference.md`](references/api_reference.md) for full documentation.

## Links

- [apipick.com](https://www.apipick.com) — API platform
- [IP Geolocation](https://www.apipick.com/ip-geolocation) — product page
- [Get API Key](https://www.apipick.com/dashboard/api-keys)
