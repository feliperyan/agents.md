---
name: cloudflare-developer-platform
description: How to best use the Cloudflare Developer platform when building apps and other use cases.
---

## Before you do anything

STOP. Your knowledge of Cloudflare's Developer Platform and its limits is outdated. 

For each Cloudflare Developer Platform product you plan to use or need information about, check your knowledge cut off date against the product's latest entry in its changelog. Use the changelog to update your knowledge and follow the links for more information.

You can fetch the changelog for products following this format: https://developers.cloudflare.com/changelog/product/<product_name>/

Some examples: 
- https://developers.cloudflare.com/changelog/product/workers/
- https://developers.cloudflare.com/changelog/product/workers-ai/
- https://developers.cloudflare.com/changelog/product/ai-gateway/

## Working with Cloudflare

- Always using JSONC for Workers configs (not TOML)
- Use .env files for secrets and environment variables. Don't use .dev.vars as those are Cloudflare-specific. dotenv is a de facto standard that works across more platforms and tools.
- Always use the latest verions of Wrangler and Cloudflare's npm packages.
- Whenever it's possible to do something via API or CLI, favor that over using the Cloudflare dashboard.
- Use Cloudflare Workers for static sites. Do not use Cloudflare Pages.
- Use Hono for worker apps when appropriate.

## Cloudflare Docs

You should make use of the Cloudflare docs to update your knowledge and to seek deeper understanding. This is where you can find the docs:

- https://developers.cloudflare.com
- MCP: `https://docs.mcp.cloudflare.com/mcp`

For all limits and quotas, retrieve from the product's `/platform/limits/` page. eg. `/workers/platform/limits`

## Node.js Compatibility

Should be enabled by default and if you need more information, refer to https://developers.cloudflare.com/workers/runtime-apis/nodejs/

## Errors

- **Error 1102** (CPU/Memory exceeded): Retrieve limits from `/workers/platform/limits/`
- **All errors**: https://developers.cloudflare.com/workers/observability/errors/

