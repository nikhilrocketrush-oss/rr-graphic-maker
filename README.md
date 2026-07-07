# RocketRush Graphic Maker

A browser-based tool for writers to turn a photo + headline into a finished LinkedIn post graphic, no design software needed. Three templates: Photo + Headline, Cutout + Background, and Photo + Screenshot.

Everything runs client-side (uploads, rendering, PNG export) — no backend, no build step, just one static `index.html`.

## Deploy to GitHub Pages (matches your rr-tracker / rr-proposals setup)

From inside this folder:

```bash
git init
git add .
git commit -m "Initial commit: RocketRush Graphic Maker"
git branch -M main
git remote add origin https://github.com/teamrocketrush-ui/rr-graphic-maker.git
git push -u origin main
```

Then in the repo on GitHub: **Settings → Pages → Source → Deploy from a branch → main / (root)**.

It'll be live at:
```
https://teamrocketrush-ui.github.io/rr-graphic-maker/
```

(First deploy can take a minute or two to go live.)

## Notes

- The optional "Auto-remove background (remove.bg)" button needs a free remove.bg API key, pasted in-session by whoever's using the tool. Nothing is stored — it's not saved to this repo, a cookie, or anywhere else.
- The "Try free unlimited auto-remove (experimental)" button loads an open-source AI model from a public CDN at runtime. It needs no key, but depends on the visitor's browser supporting it — if it fails, remove.bg or the manual brush still work.
- No env vars, no secrets, nothing to configure. It's safe to make this repo public.
