# Ambipath UCP agent profile

The public UCP platform profile for the Ambipath agent audit, served through jsDelivr at
https://cdn.jsdelivr.net/gh/usefacet/ambipath-ucp-agent@main/audit-agent.json

UCP stores fetch this profile to identify the agent on every tool call. It lives here, not on ambipath.com, because Shopify requires a Cache-Control header and a JSON content type. Porkbun static hosting sends no Cache-Control, raw GitHub sends text/plain, and GitHub Pages is disabled for the org. jsDelivr sends both. After editing, purge its cache: `curl https://purge.jsdelivr.net/gh/usefacet/ambipath-ucp-agent@main/audit-agent.json`.

The audit agent browses and builds carts and checkouts. It never pays or places an order, so the profile declares no payment handlers.
