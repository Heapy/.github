# Heapy organization profile

The public landing page for [github.com/Heapy](https://github.com/Heapy).

- [`profile/README.md`](profile/README.md) — the page GitHub displays on the organization's Overview tab.
- [`profile/assets/heapy-pencil-banner.png`](profile/assets/heapy-pencil-banner.png) — the graphite pencil illustration used as the banner, hosted in this repository.
- [`profile/assets/banner-prompt.txt`](profile/assets/banner-prompt.txt) — the image generation prompt, for future revisions.
- [`docs/projects.md`](docs/projects.md) — the complete public project directory, grouped by purpose.

## Updating the page

Edit the Markdown and push to `main`. GitHub renders the profile automatically; no deployment or build is needed. Keep this repository public.

Lead with what someone can do with a project. Verify descriptions against its current README, and distinguish implemented features from goals. Keep experimental, scaffold-only, fork, and archived labels where relevant. Do not infer maintenance or production readiness from recent commits alone.

Use absolute URLs in `profile/README.md`: it is rendered both inside this repository and on the organization profile. Keep the landing page selective; add every public project to the directory. Private repositories must not be listed.

Before publishing, check the Markdown on GitHub, the banner in light and dark themes, links, and the organization page at a narrow viewport. Compare the directory with the public repository list:

```sh
gh api --paginate 'orgs/Heapy/repos?type=public&per_page=100' --jq '.[].name'
```

The initial directory was researched on **2026-10-08** from all 55 existing public repositories, their available READMEs, and repository contents where documentation was missing or described only a proposal. This profile repository is listed separately.
