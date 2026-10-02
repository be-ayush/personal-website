# ayushbhattacharya.com

Personal site of Ayush Bhattacharya, founder of [Aika Labs](https://aikalabs.ai). Live at **https://ayushbhattacharya.com**.

A single static page that you scroll through as a story: oil-painted scenes zoom past, torn-paper notes slide over them, career parchments get tossed onto a table, and it ends on Aika Labs blog posts and a contact sheet.

## Layout

```
index.html        the whole site: markup, styles and script, no build step
favicon.svg
CNAME             custom domain for GitHub Pages
assets/art/       paintings as responsive WebP (720/1280/1920), plus home-tall-* for phones and hero-og.jpg for link previews
assets/logos/     company and university logos
CLAUDE.md         notes for AI agents working on the site
```

## Editing and deploying

1. Edit `index.html`.
2. Preview it locally with any static server, for example `python3 -m http.server 4173`, then open http://localhost:4173.
3. Commit and push to `main`. GitHub Pages deploys within about a minute.

Where the content lives:

- **Career summaries:** each `.pp` element in the "paper trail" section.
- **Popup text:** the `<template id="d-…">` blocks near the end of `<main>`.
- **Blog list:** the `.posts` list in the writing section.

## Hosting

The site is served by GitHub Pages from the `main` branch root. DNS is at GoDaddy: four `A` records for `@` pointing at GitHub Pages, and `www` as a CNAME to `be-ayush.github.io`. HTTPS is enforced, with the certificate issued by GitHub.

## Paintings

The paintings were generated with Gemini 3 Pro Image (through treg) in a realistic 19th-century oil style. Agent-facing details, including the art style rules, how to encode new images and the owner's design preferences, are in `CLAUDE.md`.
