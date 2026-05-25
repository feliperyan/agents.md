## Working with Cloudflare

- Always using JSONC for Workers configs (not TOML)
- Use .env files for secrets and environment variables. Don't use .dev.vars as those are Cloudflare-specific. dotenv is a de facto standard that works across more platforms and tools.
- Always use the latest verions of Wrangler and Cloudflare's npm packages.
- Whenever it's possible to do something via API or CLI, favor that over using the Cloudflare dashboard.
- Use Cloudflare Workers for static sites. Do not use Cloudflare Pages.
- Use Hono for worker apps when appropriate.
