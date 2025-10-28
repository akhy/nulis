# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Zola static site generator blog called "Nulis Aja Dulu" hosted at nulisajadulu.web.id. The site uses the "tabi" theme and is deployed via Netlify.

## Common Commands

### Building the Site
- `zola build` - Build the static site (outputs to `public/`)

### Development
- `zola serve` - Start development server with live reload
- `zola check` - Validate content and links

### Deployment
The site auto-deploys to Netlify when pushed to main branch. Build configuration is in `netlify.toml` with Zola version 0.21.0.

## Project Structure

```
├── config.toml          # Main site configuration
├── content/            # Site content (markdown files)
│   ├── _index.md       # Homepage
│   ├── about.md        # About page
│   └── posts/          # Blog posts
├── static/             # Static assets (images, etc.)
├── templates/          # Zola templates (if customized)
├── sass/              # Sass stylesheets (if theme customized)
├── netlify.toml       # Netlify deployment config
└── themes/            # Contains apollo theme (unused - using tabi)
```

## Configuration Notes

- Theme: "tabi" with "lavender" skin
- Base URL: https://nulisajadulu.web.id
- Author: Pepe Ronny
- Features enabled: RSS feeds, Sass compilation, HTML minification
- Menu: blog (/posts) and tentang (/about)
- Custom stylesheet: override.css
- hCard microformat enabled with avatar at img/peperonny.png

## Content Management

- Blog posts go in `content/posts/`
- Use front matter with tags taxonomy
- Markdown with code highlighting enabled (CSS theme)
- All content should be in Indonesian as per existing content
- Post markdown files should use TOML front-matter by default (triple plus sign - `+++`)

## Writing Style Guide

- Use Indonesian language with casual, informal tone (formal only for serious topics)
- No em-dash punctuation style
- First person: "Gw" (casual) or "Saya" (formal), context-dependent
- Second person: "Kalian" or "Kamu"
- Write with tech-savvy millennial voice

## Development Notes

- The `themes/apollo/` directory exists but is unused (theme is set to "tabi")
- Static files (images, etc.) go in `static/` directory
- The `scratchpad/` directory contains draft content
