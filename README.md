# Cotton + Cradle — Website (First Pass)

A professional online presence + online-shopping demo for **Cotton + Cradle**,
a baby & children's boutique in historic downtown Murfreesboro, TN.

This is a **front-end prototype** ("art of the possible"). Product data, inventory
counts, cart, and registry are mocked in the page to demonstrate the experience
before wiring up live systems.

---

## What's inside

```
index.html      ← the site
support.js       ← runtime that renders the page (required, keep next to index.html)
assets/          ← store + product photography
```

Keep all three together at the repo root — `index.html` loads `support.js` and the
`assets/` images by relative path.

> Note: deploy these files **as-is**. Don't run them through an HTML "inliner"/bundler —
> the product images load at runtime, and a bundler will log `[bundle] error` for them.
> A normal static host (Vercel, GitHub Pages, Netlify) serves the files directly and
> everything resolves correctly.

---

## Deploy to GitHub Pages (free hosting)

1. Create a new repository on GitHub, e.g. `cotton-and-cradle`.
2. Upload the contents of this folder (`index.html` + the `assets/` folder) to the
   repo root — drag-and-drop in the GitHub web UI works fine.
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Set branch to **main** and folder to **/ (root)**, then **Save**.
6. Wait ~1 minute. Your site is live at
   `https://<your-username>.github.io/cotton-and-cradle/`.

To use a custom domain later (e.g. `cottonandcradle.com`), add it under
**Settings → Pages → Custom domain** and point your domain's DNS to GitHub.

---

## Pages & features demonstrated

- **Home** — editorial hero with the storefront photo, category tiles, new
  arrivals, a live-inventory band, brand story, registry CTA, and an Instagram
  "shop the look" grid.
- **Shop** — product grid with filters (category, size, color, brand) and
  real-time stock badges (*Only a few left*, *In store only*, *Just arrived*).
- **Product detail** — image gallery, live stock status, size & color pickers,
  add-to-bag, pickup/gift-wrap/registry notes.
- **Registry** — baby & gift registry flow with favorites.
- **About / Our Story**, **Visit Us** (hours, address, map), **Events & classes**.
- **Cart drawer** with subtotal and Shopify-checkout placeholder.

---

## Going live (next steps)

When you're ready to turn the prototype into a real store:

- **Shopify** powers the catalog, cart, secure checkout, and payments. The
  product grid and cart here map directly onto Shopify's Storefront API.
- **Real-time inventory** syncs from your Shopify/POS so the stock badges reflect
  what's actually on the racks.
- **Product images** can pull from vendor feeds where available, or be uploaded
  manually — same layout as the demo.
- **Registry, gift cards, events, email signup, and loyalty** each have a Shopify
  app or integration that drops into these same screens.

This package is the visual + UX foundation; the connections above get wired in
during build-out.
