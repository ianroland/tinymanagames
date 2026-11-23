# Tiny Mana Studios

The studio site for [tinymana.games](https://tinymana.games): retro games for the browser, built with AI agents on HTML, CSS and JavaScript.

## What's here

A single static page with no build step.

| File | What it is |
| --- | --- |
| `index.html` | The whole site: markup, styles and scripts |
| `badge.png` | Round studio badge used in the hero |
| `wordmark.png` | Horizontal logo used in the header and footer |
| `favicon.png` | Browser tab icon |
| `ryan-title.jpg` | Title screen for Ryan's Road to the LPGA |
| `aussie8-title.jpg` | Title screen for Aussie8 |

## Run it locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploy

Any static host works. On Netlify, leave the build command empty and publish the repo root.

## Add a build

1. Add the title screen image to the repo root.
2. Copy a `.build` block in the Builds section of `index.html` and update the title, tagline, Retro DNA and link.
3. Add a matching `.slot` row to the Tiny Arcade menu in the header.
