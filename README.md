# KC Wallflower

Marketing site for **KC Wallflower** — vintage tableware rentals and home garden
consulting in Kansas City. Instagram: [@kcwallflower.co](https://instagram.com/kcwallflower.co)

Static site, no build step. Hosted on **GitHub Pages** at
[kcwallflower.co](https://kcwallflower.co).

## Structure

```
index.html        Single-page site
css/style.css     Styles
assets/           Favicon + (your) photos
CNAME             Custom domain for GitHub Pages
```

## Editing content

- **Text / copy** — edit `index.html`.
- **Colors / fonts** — the palette lives in the `:root` block at the top of `css/style.css`.
- **Email** — currently `hello@kcwallflower.co`; find & replace to change it.

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
