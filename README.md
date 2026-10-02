# yhhuang.me

Personal academic website of Ying Huang, built with [al-folio](https://github.com/alshedivat/al-folio) (Jekyll) and hosted on Cloudflare Pages.

## Where things live

The site is a single page (`/`).

| What                     | File                                           |
| ------------------------ | ---------------------------------------------- |
| Bio and links            | `_pages/about.md`                              |
| Profile photo            | `assets/img/prof_pic.jpg`                      |
| Publications             | `_bibliography/papers.bib`                     |
| News items               | `_news/*.md` (`date_label` overrides the date) |
| Co-author homepage links | `_data/coauthors.yml`                          |
| Look and layout          | `_sass/_custom.scss`, `_layouts/about.liquid`  |
| Site name, URL, features | `_config.yml`                                  |

## Preview locally

```bash
bundle install
LANG=C.UTF-8 bundle exec jekyll serve   # http://localhost:4000
```

## Deploy

Every push to `main` runs `.github/workflows/deploy.yml`, which builds the site and publishes it with GitHub Pages
(repo Settings → Pages → Source: **GitHub Actions**, custom domain `yhhuang.me`).

DNS for `yhhuang.me` lives in Cloudflare, set to **DNS only** (grey cloud):

- `yhhuang.me`: A records `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- `www`: CNAME `hinxcode.github.io`
