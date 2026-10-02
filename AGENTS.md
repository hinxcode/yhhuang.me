# Agent notes for yhhuang.me

This is a personal site generated from the al-folio v1 starter. Layouts, includes and styles come from the `al_folio_*` / `al_*` gems pinned in `Gemfile`; edit content and `_config.yml`, not gem-owned files.

- `baseurl` is empty (site lives at the domain root, https://yhhuang.me).
- Build: `LANG=C.UTF-8 bundle exec jekyll build` (without a UTF-8 locale the build fails with "invalid byte sequence in US-ASCII").
- Deploy: push to `main`; GitHub Actions builds and publishes with GitHub Pages (no `gh-pages` branch). DNS is in Cloudflare. See README.md.
- `Gemfile` and the `plugins:` list in `_config.yml` must agree; a plugin in only one is silently inert.
- Upstream al-folio docs are kept in `docs/` for reference.
