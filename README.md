# ted registry proxy

this is a minimal vercel proxy for the `ted` code editor extension registry.

## how it works
it proxies requests from `registry.ted.tomlin7.com` (available via `/`, `/v1`, or `/v1/extensions.json`) to the actual source JSON at `extensions.ted.tomlin7.com/v1/extensions.json`.

## configuration
- **type**: rewrite (masked proxy)
- **ttl**: 300 seconds (5 minutes)
- **cors**: enabled (`*`)
- **headers**: optimized for JSON consumption by desktop editors.

## deployment
1. Install [vercel cli](https://vercel.com/download).
2. Run `vercel deploy --prod`.
