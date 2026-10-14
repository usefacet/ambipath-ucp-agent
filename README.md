# Ambipath UCP agent profile

The public UCP platform profile for the Ambipath agent audit, served by GitHub Pages at
https://usefacet.github.io/ambipath-ucp-agent/audit-agent.json

UCP stores fetch this profile to identify the agent on every tool call. It lives here, not on ambipath.com, because stores require a Cache-Control header and Porkbun static hosting cannot set one. GitHub Pages sends `Cache-Control: max-age=600`.

The audit agent browses and builds carts and checkouts. It never pays or places an order, so the profile declares no payment handlers.
