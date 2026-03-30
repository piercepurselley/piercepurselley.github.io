# piercepurselley.github.io

Personal portfolio site for Pierce Purselley — Writer and Comedian in Los Angeles.

Live at: https://piercepurselley.github.io

## Stack

- [Hugo](https://gohugo.io/) static site generator
- Deployed via GitHub Actions to GitHub Pages
- No external CSS frameworks or JavaScript libraries

## Structure

- `hugo.toml` — site config, bio text, params
- `content/` — one markdown file per page
- `data/projects.yaml` — drives the homepage project grid (order matters)
- `static/css/style.css` — all styles
- `static/img/` — card thumbnails (WebP)
- `static/scripts/` — downloadable PDFs (lowercase-hyphenated filenames)
- `layouts/` — Hugo templates

## Pages

| URL | File |
|-----|------|
| `/` | `layouts/index.html` |
| `/writing/` | `content/writing.md` |
| `/the-library/` | `content/the-library.md` |
| `/trash-panda/` | `content/trash-panda/index.md` (page bundle) |
| `/mortified/` | `content/mortified.md` |
| `/doom-scrolling/` | `content/doom-scrolling.md` |
| `/bio/` | `content/bio.md` |
| `/contact/` | `content/contact.md` |

## Adding a project card

Edit `data/projects.yaml`. Order in the file = order on the homepage.

```yaml
- title: "Project Title"
  category: "Category"
  description: "One-line description."
  url: "/page-slug/"
  cover: "/img/filename.webp"
```

## Adding a PDF script

1. Name the file `lowercase-hyphenated.pdf`
2. Drop it in `static/scripts/`
3. Reference it in `content/writing.md` as `/scripts/filename.pdf`

## Local development

```bash
hugo server
```

Runs at http://localhost:1313
