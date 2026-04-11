# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio/resume website for Marcel Richter, deployed as a GitHub Pages site at `mrclrchtr.de`. Built with Jekyll using the `sproogen/resume-theme` remote theme. All content is configured in `_config.yml` — there are no separate content files (except `index.md` which is intentionally empty).

## Development Commands

```bash
bundle install                # Install Ruby gems
bundle exec jekyll serve      # Local dev server at http://localhost:4000
bundle exec jekyll build      # Build static site to _site/
```

## Architecture

Content lives almost entirely in `_config.yml` — experience, education, skills, social links, and personal info are all YAML sections there. The site delegates layout and styling to the remote theme `sproogen/resume-theme`; local customization is limited to `assets/main.scss`.

Key files:
- `_config.yml` — all personal content and site configuration
- `assets/main.scss` — custom styles (imports theme, add overrides here)
- `stackoverflow.html` / `xing.html` — redirect pages to social profiles
- `CNAME` — custom domain (`mrclrchtr.de`)
- `renovate.json` — automated dependency updates for `Gemfile`

## Making Changes

- **Update personal info, experience, education, skills**: edit the relevant sections in `_config.yml`
- **Add social/redirect links**: create a new `.html` file with a meta-refresh redirect
- **Custom styling**: add SCSS rules to `assets/main.scss`
- **Theme changes**: the remote theme is `sproogen/resume-theme`; check its documentation for available layout options and config keys
