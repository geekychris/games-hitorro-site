# games.hitorro.com

The Hitorro Games website: one static page listing the games. The folder `site/` is
what's served.

**Hosting:** cloud-stack's proxy on mp2 serves it straight from this repo's `main`
branch. The route is `{name: games, site: {repo: geekychris/games-hitorro-site, dir: site},
exposure: public}` in cloud-stack's `infra/inventory.yaml`; see cloud-stack's
`docs/PROXY.md`, "Websites".

**Updating:** edit `site/` and push to `main`. The proxy checks every two minutes and
swaps in the new files.

**Rules for this repo:**
- Plain HTML, CSS and images only. The proxy serves files; it runs no code.
- `site/404.html` is the not-found page.
- Never link the unlisted test-build download pages from here. This repo and the site
  are both public.

The images come from the games' own art, and the bull and the night sky from Lantern's
`publishers/hitorro` pack, re-encoded as WebP.
