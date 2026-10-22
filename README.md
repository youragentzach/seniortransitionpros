# seniortransitionpros.com

The Senior Transition Pros website, served by GitHub Pages from `main`.
GitHub Pages builds it with Jekyll, using only plugins GitHub Pages supports
(`jekyll-seo-tag`, `jekyll-sitemap`, `jekyll-feed`).

## Layout of the repo

| Path | What it is | Owner |
| --- | --- | --- |
| `index.html` | Landing page with the family intake and provider claim forms. Plain HTML, no front matter, so Jekyll copies it unchanged | Operating agent |
| `guide-cleanout-parents-house-atlanta.html` | The original cleanout guide. Plain HTML, URL kept as is | Blog |
| `guides/index.html` | The guides index at /guides/ | Blog |
| `_posts/` | Published guides, one Markdown file each, served at /guides/guide-name/ | Blog |
| `_drafts/` | Guides in progress. Never built or published | Blog |
| `_layouts/`, `_includes/`, `assets/css/site.css` | Shared templates and styles for guides and site pages | Blog |
| `about.md`, `how-we-make-money.md`, `how-we-verify.md`, `how-we-write-our-guides.md`, `privacy.md`, `contact.md` | Trust pages | Blog, with Zach's approval |

## Rules for everyone working in this repo

1. Never push straight to `main`. Work on a branch and open a pull request.
2. Zach approves every pull request that adds or changes a public page or claim.
3. Nothing is merged while the repo still contains an unresolved `[CONFIRM: ...]` marker:
   `grep -rn "\[CONFIRM:" --include="*.md" --include="*.html" --exclude=README.md .` must return nothing.
4. The operating agent uses published guides in outreach but does not edit them.
   It flags problems in a pull request comment instead.
5. Every number in a guide has a source or a label saying where it came from.
   No invented statistics, quotes, experts or testimonials.

## Publishing a guide

1. Draft it in `_drafts/` from `_drafts/guide-template.md`.
2. Open a pull request with a one-line summary of its claims and sources.
3. Once approved, move it to `_posts/YYYY-MM-DD-slug.md` with the publish date and merge on that date.
4. Submit the new URL in Google Search Console and update the tracker in the blog plan.
