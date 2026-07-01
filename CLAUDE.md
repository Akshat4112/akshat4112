# CLAUDE.md

Guidance for AI assistants (Claude Code and others) working in this repository.

## What this repository is

This is **`akshat4112/akshat4112`** — a GitHub **special profile repository**.
When a repository's name matches its owner's username, GitHub renders that
repository's `README.md` at the top of the owner's public profile page
(https://github.com/akshat4112).

There is **no application code, build system, test suite, or dependencies** here.
The repository's entire purpose is to present a personal profile card. Treat it
as a documentation/presentation repo, not a software project. Do not scaffold
tooling (package managers, linters, CI, test frameworks) unless the user
explicitly asks — it would not belong here.

## Layout

| File | Purpose |
| --- | --- |
| `README.md` | The profile card rendered on the GitHub profile page. This is the primary artifact. |
| `newreadme.md` | Empty scratch/placeholder file. Safe to ignore; confirm with the user before deleting. |
| `CLAUDE.md` | This file. |

## The `README.md`

`README.md` is a single HTML+Markdown document (GitHub Flavored Markdown allows
inline HTML). Its structure, top to bottom:

1. **Heading block** — centered `<h1>`/`<h3>` with the name and tagline.
2. **Badges** — a profile-views counter (komarev) and a Twitter follow badge
   (shields.io).
3. **Bullet intro** — links to projects, topics, contact email, and résumé.
4. **"Connect with me"** — a row of social icons (Twitter, LinkedIn,
   Stack Overflow, Kaggle, Instagram), each an `<a>` wrapping an `<img>`. Some
   entries (HackerRank, LeetCode) are commented out with `<!-- -->` and kept for
   easy re-enabling.
5. **"Languages and Tools"** — a row of technology logos, each an `<a>`/`<img>`
   pointing at an external SVG (devicon, vectorlogo.zone, worldvectorlogo, etc.).

### Conventions to preserve when editing

- **Centered headings, left-aligned body.** Headings use `align="center"`;
  content paragraphs use `<p align="left">`. Keep this contrast.
- **Icons are `<a target="_blank">` wrapping an `<img>`** with `height`/`width`
  around `30-40`px. Match the existing sizing and attribute order when adding
  a new social link or tech logo.
- **Images are hosted externally** (CDNs and logo repos). Do not commit binary
  image assets; follow the existing pattern of linking to a canonical SVG URL.
- **Keep commented-out blocks intact** unless asked to remove them — they are
  intentional toggles.
- **Personal data is intentional and public** (name, handles, email, résumé
  link). When updating it, use exactly what the user provides; don't guess at
  new URLs or contact details.

## Working in this repo

- Verification is **visual**, not automated: after editing `README.md`, render
  it as Markdown to confirm layout, and check that any new image/link URLs are
  well-formed. There is nothing to compile, lint, or test.
- Keep changes minimal and scoped to what the user asks. This is a
  presentation surface — restructuring it is a design decision the user owns.

## Git workflow

- Default branch: `master`.
- Commit history is small and message style is informal (e.g. "Update
  README.md"). Write clear, descriptive commit messages regardless.
- **Do not push to `master` directly** in assistant-driven sessions. Work on the
  designated feature branch and push there; open a pull request only when the
  user explicitly asks.
- Commit and push only when the user requests it.
