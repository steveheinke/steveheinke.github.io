# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

This is Steve Heinke's personal academic homepage, hosted via GitHub Pages at `steveheinke.github.io`. It is a Jekyll site using the built-in `jekyll-theme-minimal` theme (configured in [_config.yml](_config.yml)), with no custom build tooling, package manager, or test suite — GitHub Pages builds and serves the site automatically on push to `main`.

## Architecture

- [index.md](index.md) is the entire site: a single Jekyll page (`layout: default`) containing large blocks of inline HTML/CSS (styles are embedded in a `<style>` block at the top of the file rather than in a separate stylesheet). There is no `_layouts/`, `_includes/`, or `assets/` directory — everything lives in this one file.
- The page is structured as stacked sections identified by anchor `id`s, linked from a sticky dropdown menu (`.menu-dropdown` / `.menu-content`) near the top: `about-me`, `publications`, `working-papers`, `research-in-progress-selected`, `professional-services-selected`, `teaching-experience`. The dropdown opens on hover (desktop) or click/tap (touch devices, via a small inline `<script>` toggling an `.open` class and `aria-expanded`) — this is the only JavaScript in the page.
- Publications and working papers are lists of `<li>` entries, each with a title link, author/venue line, and a collapsible `<details>/<summary>` block holding the abstract. Follow this existing `<li>`/`<details>` pattern when adding new entries rather than introducing new markup styles. Publications is a numbered `<ol reversed start="8">` (highest number first); the `start` value is hardcoded to the current publication count (not browser-auto-computed, which is unreliable across browsers) — update it whenever a publication is added or removed. Working Papers and all other lists on the page use plain bullets (`<ul>`), not numbering.
- The email address in the "About me" section is HTML-entity-encoded (`&#109;&#97;...`) to obscure it from scrapers — preserve this encoding rather than writing the address in plain text.
- Static assets referenced directly from `index.md`: `Steve_Heinke.jpg` (profile photo) and `CV_steveheinke.pdf` (downloadable CV), both at the repo root.

## Working in this repo

- There is no local build/test/lint step. To preview changes, either push to `main` and let GitHub Pages rebuild, or run Jekyll locally (`bundle exec jekyll serve`) if a Gemfile is present — none is currently checked in, so GitHub Pages' hosted build is the normal path.
- Changes are almost always direct edits to [index.md](index.md) (content updates, new publications, styling tweaks); commit messages in this repo's history are short and content-descriptive (e.g. "Update about me", "new cv").
- `git pull`, `git commit`, and `git push` to `origin/main` are pre-authorized in this repo — go ahead and run them without asking for confirmation first. This does not extend to destructive operations (force-push, reset --hard, history rewrites), which still need explicit sign-off.
