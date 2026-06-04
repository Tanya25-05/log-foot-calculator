# BoardFootCal

A modern board foot calculator for woodworkers, contractors, and DIYers. Real-time calculation, SVG isometric visualizer, multi-item cut list, and cost estimation with waste factor.

Built with [Astro](https://astro.build) and [Tailwind CSS v4](https://tailwindcss.com).

## Features

- **Real-time board foot calculation** — results update as you type
- **Price per board foot** with 10-currency selector (USD, EUR, GBP, CAD, AUD, JPY, CNY, INR, BRL, MXN)
- **SVG isometric lumber visualizer** — scaled 3D preview with dimension annotations
- **Multi-item cut list** — add multiple board sizes, adjust quantities, see running totals
- **Waste factor slider** (0–50%) for realistic material estimates
- **Imperial / Metric toggle**
- **Quick Fill presets** for common lumber sizes (2×4, 2×6, 1×6, 4×4, etc.)
- **Dark / Light mode** with system preference detection
- **localStorage persistence** — cut list and theme survive page reloads
- **5 MPA pages** — Home, About, Contact, Privacy Policy, Terms & Conditions
- **SEO optimized** — sitemap.xml, robots.txt, OG/Twitter meta tags, JSON-LD schema, canonical URLs
- **Google Analytics** (G-X3VYVBGR8D)
- **Custom 404 / 500 error pages**
- **Cloudflare Pages ready** — `_headers` and `_redirects` included

## Tech Stack

| Layer | Choice |
|---|---|
| Framework | Astro 6 (static output) |
| CSS | Tailwind CSS v4 |
| Vite plugin | `@tailwindcss/vite` |
| Icons | Inline SVG |
| Fonts | Inter + JetBrains Mono via Google Fonts |
| Hosting | Cloudflare Pages |
| Analytics | Google Analytics (gtag) |

## Prerequisites

- Node.js >= 22.12.0

## Local Development

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

The dev server runs at `http://localhost:4321`.

## Project Structure

```
/
├── public/               # Static assets (favicons, sitemap, robots.txt, _headers)
├── src/
│   ├── components/       # Astro components (NavBar, Footer, Calculator, FAQ, etc.)
│   ├── layouts/          # Layout.astro (SEO meta, OG tags, schema, theme toggle)
│   ├── pages/            # Route pages (index, about, contact, privacy, terms, 404, 500)
│   └── styles/           # Global CSS (Tailwind import, design tokens, custom classes)
├── astro.config.mjs      # Astro config (site URL: boardfootcal.com)
└── package.json
```

## Deploy to Cloudflare Pages

1. Push this repo to GitHub
2. In Cloudflare Dashboard → Workers & Pages → Pages, click **Create → Pages → Connect to Git**
3. Select this repo and set:
   - **Build command:** `npm run build`
   - **Build output:** `dist/`
   - **Environment variable:** `NODE_VERSION = 22`
4. Deploy
5. Add your custom domain `boardfootcal.com` in the Pages dashboard

## Domain Configuration

The site is configured for `boardfootcal.com`:
- Canonical URLs point to `https://boardfootcal.com`
- Sitemap: `https://boardfootcal.com/sitemap.xml`
- Open Graph / Twitter card images reference the domain
- Google Analytics tag G-X3VYVBGR8D

## License

MIT
