# Personal Cloudflare deployment

The `deploy/rusiru-sh` branch exports the reader as static files for Cloudflare Pages.
The upstream feature PR keeps the original Next.js server configuration.

- Site: https://salalihini.rusiru.sh
- Pages project: `salalihini-rusiru`
- Cloudflare production branch: `deploy/rusiru-sh`

With `CLOUDFLARE_API_TOKEN` and `CLOUDFLARE_ACCOUNT_ID` available in your shell:

```sh
npm ci
npm run build
npx wrangler pages deploy out --project-name salalihini-rusiru --branch deploy/rusiru-sh
```

The output contains all verse pages and the first MP3. Subsequent recordings stream from
Internet Archive, preserving their original attribution and separate noncommercial licence.
Only static files are deployed; there is no Next.js server or server-side API.
