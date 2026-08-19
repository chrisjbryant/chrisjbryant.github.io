# chrisjbryant.github.io

Personal academic website of Christopher Bryant, built with [Jekyll](https://jekyllrb.com/)
and the [al-folio](https://github.com/alshedivat/al-folio) theme, deployed to GitHub Pages.

Live at <https://chrisjbryant.github.io>.

## Editing content

| What you want to change             | Where                        |
| ----------------------------------- | ---------------------------- |
| Bio, profile picture, CV links      | `_pages/about.md`            |
| Publications                        | `_bibliography/papers.bib`   |
| News items on the homepage          | `_news/` (one file per item) |
| Social links, email                 | `_data/socials.yml`          |
| Venue colours on publication badges | `_data/venues.yml`           |
| Co-author homepage links            | `_data/coauthors.yml`        |
| Paper PDFs, slides, posters         | `assets/pdf/`                |
| Site title, name, URL, plugins      | `_config.yml`                |

Publications are grouped by year automatically, so a new `.bib` entry appears
without touching `_pages/publications.md`. Each entry's `pdf=` field points at a
filename in `assets/pdf/`, and `abbr=` selects a venue badge from `_data/venues.yml`.

## Running locally

```bash
docker compose up -d
```

The site is then at <http://localhost:8080>. Edits to content reload
automatically; changes to `_config.yml` restart Jekyll, which takes a few
seconds. Stop it with `docker compose down`.

Note that `docker-compose-slim.yml` is not used here — the
`amirpourmand/al-folio:slim` image it pulls is currently broken upstream (its
bundler raises `NoMethodError`), and it fails the same way on an unmodified
al-folio checkout.

With a native Ruby toolchain, `bundle install && bundle exec jekyll serve` also
works. GitHub Actions builds with Ruby 3.3.5.

## Deployment

Pushing to `master` runs the `Deploy site` workflow, which builds the site and
force-pushes the result to the `gh-pages` branch. GitHub Pages serves that
branch. Repository Settings must have Actions granted read and write
permissions, and Pages set to deploy from `gh-pages`.

## Theme upgrades

al-folio v1 is a thin starter: layouts, includes, styles and features live in
versioned gems pinned in `Gemfile` and listed under `plugins:` in `_config.yml`.
Both lists must agree — a plugin named in only one of them silently does
nothing. To check for newer releases:

```bash
bundle exec al-folio upgrade audit
```

Theme documentation is under `docs/`.
