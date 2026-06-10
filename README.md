# Xyra Bulk SMS — Developer Documentation

Mintlify-powered docs for the Xyra Bulk SMS HTTP API.

**Live site:** https://docs.bulksms.xyratechnology.co.ke

## Local development

```bash
# one-time
npm i -g mint

# from this folder
mint dev
```

The dev server runs at http://localhost:3000 and hot-reloads MDX + the OpenAPI spec.

## Project structure

| Path                          | Purpose                                                |
| ----------------------------- | ------------------------------------------------------ |
| `docs.json`                   | Mintlify site config — theme, nav, OpenAPI binding.    |
| `openapi.yaml`                | API spec. Drives the auto-generated API reference.     |
| `introduction.mdx`            | Landing page.                                          |
| `quickstart.mdx`              | Five-minute first message.                             |
| `authentication.mdx`          | How `apikey` + `partnerID` work.                       |
| `concepts/`                   | Sender IDs, DLR semantics, GSM-7 vs Unicode encoding.  |
| `api-reference/`              | One MDX wrapper per endpoint with extra prose/notes.   |
| `errors.mdx`                  | Response code reference.                               |
| `changelog.mdx`               | Versioned change log.                                  |
| `logo/`                       | Brand assets (light + dark SVG).                       |

## Deploy

1. Push this folder to a GitHub repo (e.g. `xyra-technology/bulksmsdocs`).
2. In the Mintlify dashboard, connect the repo. Every push to `main` triggers a rebuild.
3. Add a CNAME record on `docs.bulksms.xyratechnology.co.ke` pointing to `cname.mintlify.app`.
4. In the Mintlify dashboard → **Settings → Custom Domain**, enter `docs.bulksms.xyratechnology.co.ke`.

## Editing checklist

- All endpoint URLs use the canonical base `https://bulksms.xyratechnology.co.ke/api/services`.
- Sender ID examples use `XYRA`.
- All MSISDN examples use the international `2547xxxxxxxx` format (no `+`).
- Keep `clientsmsid` examples as integers (the API expects an integer there).
