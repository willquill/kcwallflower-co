# KC Wallflower

Marketing site for **KC Wallflower** — vintage tableware rentals and home garden
consulting in Kansas City. Instagram: [@kcwallflower.co](https://instagram.com/kcwallflower.co)

Static site, no build step. Hosted on **GitHub Pages** at
[kcwallflower.co](https://kcwallflower.co).

## Structure

```
index.html        Tabbed chooser — switch between the design options
original/          Design option: the original full site (css + assets self-contained)
a/                 Design option A — "Heirloom"
b/                 Design option B — "Garden Press"
c/                 Design option C — "Field & Table"
css/ , assets/     Styles + favicon for the original design
CNAME              Custom domain for GitHub Pages
```

Once a design is chosen, promote that folder's `index.html` (and any assets) to
the repo root and drop the chooser + the other options.

## Editing content

- **Text / copy** — edit `index.html`.
- **Colors / fonts** — the palette lives in the `:root` block at the top of `css/style.css`.
- **Contact** — Instagram DM only (no email set up yet). Contact links point to
  [@kcwallflower.co](https://instagram.com/kcwallflower.co).

## Adding real photos

The gallery currently shows four placeholder tiles. To use real photos:

1. Drop images into `assets/` (e.g. `assets/table-1.jpg`).
2. In `index.html`, find the `<!-- ============ GALLERY ============ -->` block and
   replace each `<div class="gallery__tile"><span>Add photo</span></div>` with:
   ```html
   <div class="gallery__tile"><img src="assets/table-1.jpg" alt="Vintage tablescape" /></div>
   ```

## Deploying

Any push to `main` publishes automatically via GitHub Pages (Settings → Pages →
Source: `main` / root). The `CNAME` file keeps the custom domain attached.
