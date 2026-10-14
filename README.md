# catdog.video

A responsive, playful coming-soon landing page for catdog.video, built with Vite, HTML, CSS, and vanilla JavaScript.

## Requirements

- Node.js 18+ (Node.js 20 LTS or newer recommended)
- npm (included with Node.js)

## Run locally

```bash
npm install
npm run dev
```

Open the local URL printed by Vite (usually http://localhost:5173).

## Production build

```bash
npm run build
npm run preview
```

The optimized static website is generated in `dist/`.

## Project structure

```text
catdog-video/
├── public/
│   └── paw.svg
├── src/
│   ├── main.js
│   └── style.css
├── index.html
├── package.json
└── README.md
```

## Deploy

### Netlify (simple option)

1. Push this project to a GitHub repository.
2. In Netlify, choose **Add new site → Import an existing project**.
3. Select the repository.
4. Set **Build command** to `npm run build`.
5. Set **Publish directory** to `dist`.
6. Deploy.

### Cloudflare Pages

1. Create a Pages project and connect the Git repository.
2. Set the build command to `npm run build`.
3. Set the build output directory to `dist`.
4. Deploy.

### Vercel

1. Import the repository into Vercel.
2. Vite is normally detected automatically.
3. Use `npm run build` as the build command and `dist` as the output directory.
4. Deploy.

### Connect catdog.video

At your hosting provider, add `catdog.video` as a custom domain and follow the provider's DNS instructions. Add both the apex domain and `www` if you intend to support both, then choose one canonical domain and redirect the other to it. DNS and TLS setup can take time to propagate.

## Before launch

- Update `hello@catdog.video` in `index.html` if you want a different contact address. The button opens the visitor's email app; it does not store email addresses.
- Google Fonts is loaded remotely. If you need a fully self-hosted site, remove the Google Fonts `<link>` elements and use system fonts, or host licensed font files yourself.
- Update title, description, and social metadata when the product positioning is finalized.
- Check the deployed site on mobile and desktop.

## Implementation approaches

### A. Vite + vanilla JavaScript (current implementation)

**Pros:** small runtime, few dependencies, fast builds, easy static hosting, no framework learning curve.

**Cons:** UI state and reusable components become harder to organize as the product grows.

**Best for:** this temporary landing page and a small static video gallery.

### B. Vite + React

**Pros:** reusable components, familiar state model for filters and modals, easier to maintain a growing interactive UI.

**Cons:** adds dependencies and build/runtime complexity; not necessary for a single coming-soon page.

**Best for:** a future experience with category filtering, video detail views, favorites, and richer interactions.

Recommendation: keep the current vanilla Vite page until the video discovery features are ready. If the UI grows into many interactive components, migrate to React then.
