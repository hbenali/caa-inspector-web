# CAA Checker

A free, single-page CAA (Certification Authority Authorization) record checker and generator. Live at [caa.hbenali.ovh](https://caa.hbenali.ovh).

No backend, no build step, no dependencies — it's one static `index.html` calling public APIs directly from the browser.

## Features

- **Lookup** any domain's CAA DNS records via DNS-over-HTTPS
- **Generator** — build `issue` / `issuewild` / `iodef` records with autocomplete for common CAs
- **Load existing** — pull records from a lookup straight into the generator to edit
- **BIND output** — export the generated records as ready-to-paste zone file lines
- **Dark mode** with persisted preference
- Fully responsive, accessible (labeled fields, WCAG AA contrast), and SEO-tagged (Open Graph, Twitter Card, JSON-LD)

## Running locally

No build step required — just serve the directory:

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Data sources

All lookups happen client-side against a free public API:

- [dns.google](https://developers.google.com/speed/public-dns/docs/doh) — DNS-over-HTTPS for CAA record lookups

## Deployment

Deployed automatically to GitHub Pages on every push to `main` (see `.github/workflows/`).

## License

MIT — see [LICENSE](LICENSE).
