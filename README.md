# MGBfC Patient & Family Resource — Web Preview

This is a browser-based preview of the iOS/Android app for clinical reviewers. It is **not a production build** — it exists so PICU testers can see the resources and contacts they have been authoring in the CMS without having to install TestFlight.

**Live URL:** https://mgh-lcs.github.io/patient-family-resource-web-preview/

## What you should know before using it

- **No PHI. Ever.** This build is **not encrypted**. A red banner across every screen says so. Treat it as a content-preview tool only — do not enter patient information.
- **Your bookmarks live in this browser.** Anything you bookmark, mark as recently-viewed, or set as your unit/phase is saved in this browser only. Clearing site data wipes it. It does not follow you to other devices or browsers.
- **The content is real.** The app reads from the production content mirror, so what you see here is exactly what the iOS app sees in TestFlight after the latest CMS publish.
- **Updates happen automatically.** When new content is published in the CMS, this preview will pick it up on the next refresh. If the app looks stale, close and reopen the tab.

## How it stays in sync with the app

This preview is rebuilt automatically every time the main app code changes. The build pipeline lives in the [`patient-family-resource-app`](https://github.com/MGH-LCS/patient-family-resource-app) repo under `.github/workflows/deploy-web-preview.yml`.

Content updates do not require a rebuild — they come from the public mirror at [`patient-family-resource-content`](https://github.com/MGH-LCS/patient-family-resource-content) on the `production-mirror` branch.

## Reporting issues

If something looks wrong:

1. **Wrong content?** That is a CMS data issue — open an issue on the CMS repo or message the editor.
2. **App misbehaves (crashes, layout broken, missing button)?** Open an issue on the [`patient-family-resource-app`](https://github.com/MGH-LCS/patient-family-resource-app) repo and include: the browser you used, what you were doing, and a screenshot if you can.

## What this repo contains

Just the built static files for GitHub Pages, on the `gh-pages` branch. No source code lives here — the source is in [`patient-family-resource-app`](https://github.com/MGH-LCS/patient-family-resource-app).
