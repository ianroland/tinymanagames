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
| `typlympics-title.jpg` | Title screen for Typlympics |
| `beerleague-title.jpg` | Title art for Beer League Hockey |
| `pickleball-title.jpg` | Title screen for Pickleball Dynasty |
| `fridaynight-title.jpg` | Title screen for Friday Night Dynasty |

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

## Community Mana Jams

The gallery, the share form and the jam jars use a Supabase project (`tiny-mana-jams`). The key in `index.html` is the public one; row-level security limits it to reading approved entries, submitting new ones and adding jars.

To moderate, open the `jam_entries` table in the Supabase dashboard:

- New submissions arrive with `status` set to `pending` and are not shown on the site.
- Set `status` to `approved` to list an entry, or `rejected` to keep it hidden.
- `jars` is the running total and updates on its own.

## Retro DNA generator

The game pool lives in the `GENRES` list in `index.html`. Only games from the 128-bit era and earlier are eligible. The daily theme is seeded by the UTC date, so changing the list changes which pair a given day lands on.
