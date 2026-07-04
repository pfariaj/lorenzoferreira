# Lorenzo Ferreira — Portfolio

Personal portfolio website for Lorenzo Ferreira, aspiring artist and cinematographer based in Lisbon.

## Stack

Plain HTML/CSS/JS — no build tools, no dependencies. Works offline and can be hosted on any static hosting service (Netlify, Vercel, GitHub Pages, etc.).

## File structure

```
├── Lorenzo Ferreira - Portfolio.dc.html   # Main portfolio file (open this in browser)
├── projetos.json                           # Project data (titles, descriptions, gallery images, video links)
├── support.js                             # Runtime support file (do not delete)
├── assets/
│   ├── homePortfolio.mp4                  # Home page background video
│   ├── lorenzo.jpg                        # Photo used in About Me section
│   ├── background.png                     # Fallback background
│   └── projetos/                          # Project gallery images
│       ├── desejo-do-rei/
│       ├── cereal/
│       └── nao abras a porta/
```

## How to run

Open `Lorenzo Ferreira - Portfolio.dc.html` directly in a browser. No server needed.

## Adding a new project

1. Create a folder inside `assets/projetos/` with the project's slug (e.g. `assets/projetos/my-project/`)
2. Add gallery images inside it (e.g. `01.png`, `02.png`, …)
3. Add a cover image
4. Open `projetos.json` and add a new entry following the existing format:

```json
{
  "id": "my-project",
  "titulo_pt": "Nome do Projeto",
  "titulo_en": "Project Name",
  "ano": "2025",
  "tc": "00",
  "descricao_pt": "Descrição em português.",
  "descricao_en": "Description in English.",
  "capa": "assets/projetos/my-project/01.png",
  "video_url": "https://www.youtube.com/watch?v=XXXXXXX",
  "galeria": [
    "assets/projetos/my-project/01.png",
    "assets/projetos/my-project/02.png"
  ]
}
```

> **Note:** `video_url` supports YouTube links. For Vimeo use `video_vimeo` instead.  
> If a YouTube video shows "embedding disabled", go to YouTube Studio → video → More options → enable "Allow embedding". Until then, a click-through button to YouTube is shown automatically.

## Updating content

| What | Where |
|---|---|
| About Me text | Logic class in the `.dc.html` file — `about_p1` / `about_p2` in `copy()` |
| Contact email | Template in the `.dc.html` file — search for `mailto:` |
| Social links | Logic class — `socials` array in `renderVals()` |
| Home background video | Replace `assets/homePortfolio.mp4` |
| About Me photo | Replace `assets/lorenzo.jpg` |

## Colors

| Role | Value |
|---|---|
| Background | `#0d0f12` |
| Text | `#c7cacc` |
| Accent | `#c91b68` |
| Hover | `#809fff` |

## Publishing

Upload the entire project folder to any static host. Recommended: [Netlify](https://netlify.com) — drag and drop the folder and it goes live instantly.
