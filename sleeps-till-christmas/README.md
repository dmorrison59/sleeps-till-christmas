# Sleeps Till Christmas

An installable web app (PWA): a live Christmas countdown with a rotating "Holiday Picks" card.

## Files

| File | What it does |
|---|---|
| `index.html` | The whole app. Edit the `DEALS` list near the bottom to change products. |
| `manifest.webmanifest` | App name, colors and icons, so phones can install it. |
| `sw.js` | Service worker. Makes the app installable and lets it open offline. |
| `icons/` | App icons (home screen, splash, browser tab). |

## Put it online with GitHub Pages (Windows Command Prompt)

1. On github.com, create a new **public** repository named `sleeps-till-christmas`. Don't add a README.
2. Unzip this folder, then in CMD:

```
cd %USERPROFILE%\Downloads\sleeps-till-christmas
git init
git add .
git commit -m "Sleeps Till Christmas"
git branch -M main
git remote add origin https://github.com/dmorrison59/sleeps-till-christmas.git
git push -u origin main
```

3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root) → Save.**
4. After a minute or two it's live at:
   `https://dmorrison59.github.io/sleeps-till-christmas/`

## Installing it on a phone

- **Android (Chrome):** open the link and tap **📲 Add to home screen** (or ⋮ → Install app).
- **iPhone (Safari):** tap **Share → Add to Home Screen**. The button on the page shows these steps.

## Updating deals later

1. Edit the `DEALS` list in `index.html` (title, text, price, link).
2. In `sw.js`, bump `CACHE` (e.g. `sleeps-v1` → `sleeps-v2`).
3. Push:

```
git add .
git commit -m "Update deals"
git push
```

Installed copies pick up the change the next time they're opened with a connection.

## Before launch

- Replace every `https://example.com/...` link with your Stripe Payment Link or affiliate links.
- Keep the "Sponsored" label and disclosure line (FTC rule for affiliate links).
- Optional: buy a short domain and point it at GitHub Pages (Settings → Pages → Custom domain).
