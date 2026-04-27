# Project Name

> One-line description of what this does.

---

## Features

- **Offline-first** — Full functionality after first load via Service Worker
- **Installable PWA** — "Add to Home Screen" on iOS and Android
- **Security-hardened** — CSP, Referrer-Policy, and Permissions-Policy via meta tags
- **Zero dependencies** — Vanilla HTML, CSS, and JavaScript only
- **Privacy-first** — All logic runs client-side; no data leaves the device
- **Mobile-first** — Touch-optimized, responsive, WCAG-compliant touch targets

---

## Tech Stack

| Layer | Choice |
|---|---|
| Markup | HTML5 |
| Styles | CSS3 (Custom Properties, Flexbox, Grid) |
| Logic | Vanilla JavaScript (ES2022, module pattern) |
| Offline | Service Worker (Stale-While-Revalidate) |
| PWA | Web App Manifest |
| Hosting | GitHub Pages (static) |

---

## Local Development

No build step. No package manager. No Node.js required.

```bash
# 1. Clone the repository
git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git

# 2. Enter the directory
cd YOUR-REPO

# 3. Serve locally (choose one)
npx serve .                          # Node.js
python3 -m http.server 8080          # Python
# Or open index.html directly in a browser
```

> **Note:** Service Workers require `localhost` or HTTPS. Use a local server (not `file://`) to test offline functionality.

---

## Deployment

Push to the `main` branch. GitHub Pages will serve the repo root automatically.

Configure in: **Settings → Pages → Source → Deploy from branch → main / (root)**

---

## Security Score

This project targets an **A+ on Mozilla Observatory**.

Headers implemented via `<meta>` tags (no server config required):

| Header | Value |
|---|---|
| Content-Security-Policy | `default-src 'self'; script-src 'self'; ...` |
| Referrer-Policy | `strict-origin-when-cross-origin` |
| X-Content-Type-Options | `nosniff` |
| Permissions-Policy | `geolocation=(), microphone=(), camera=()` |

---

## Project Structure

```
├── .github/
│   └── pull_request_template.md
├── .editorconfig
├── .gitignore
├── .nojekyll
├── CONTRIBUTING.md
├── LICENSE
├── README.md
├── app.js
├── humans.txt
├── index.html
├── manifest.json
├── robots.txt
├── sitemap.xml
├── style.css
└── sw.js
```

---

## License

MIT — see [LICENSE](LICENSE)
