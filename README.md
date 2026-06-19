# cumulus-platform-docs

Public product documentation for the **Cumulus Agentic Platform**, built with
[MkDocs](https://www.mkdocs.org/) + [Material](https://squidfunk.github.io/mkdocs-material/)
and published to GitHub Pages.

## Local preview

```bash
pip install -r requirements.txt
mkdocs serve
```

Then open <http://127.0.0.1:8000>.

## Structure

```
docs/
  index.md            # Home
  user-guide/         # Getting started & concepts
  knowledge-base/     # How-to articles
  api-reference.md    # API overview
  faq.md              # Frequently asked questions
  incidents/          # Public incident reports
mkdocs.yml            # Site configuration
```

## Publishing

Pushing to `main` triggers the [Deploy Docs](.github/workflows/deploy-docs.yml)
workflow, which builds the site and deploys it to GitHub Pages.

> One-time setup: in the repository settings, set **Pages → Build and
> deployment → Source** to **GitHub Actions**.

## Contributing

Keep content concise and public-safe — avoid internal hostnames, credentials, or
sensitive operational detail.
