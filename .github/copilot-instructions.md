## Purpose

This file gives compact, actionable context for AI coding agents acting on this repository. Keep instructions short and specific to what's actually present in the workspace.

## Repo high-level snapshot

- Current workspace contains a minimal static-site repository with a single stylesheet at `styles.css` in the repo root.
- No build scripts, package manifests, server code, or test harnesses were present at the time of writing. If you need to make structural changes (add HTML, JS, build tool), note them in a PR and call out intended developer workflows.

## What to do first (orienting checks)

1. Confirm repository root contents. The canonical file to edit is `styles.css` when working on styling.
2. If you expect HTML/JS entrypoints, look for `index.html`, `src/`, or `public/` — none were present; create them only when necessary and document where you added them.

## Recommended agent behaviors for this project

- Make minimal, explicit changes. This repo appears to be a simple static site; avoid adding heavy build tooling unless requested.
- When editing style rules, prefer updating `styles.css`. Show exact lines changed in PRs and include a brief visual testing note (e.g., "I previewed changes in Browser — header color updated").
- If adding new files (HTML/JS), include a one-line README addition describing run/preview steps.

## Patterns & conventions (discoverable examples)

- Single global CSS file: `styles.css` — assume global rules and no CSS modules or preprocessors unless you find a config file (e.g., package.json, postcss.config.js).
- No explicit build/test commands: runtime is plain static files; preview locally using the browser or a static-server. Example: open `index.html` in the browser (or run a tiny local server) — but do not add server dependencies unless requested.

## How to run / preview (explicit help for contributors)

- Local preview (when only static files exist): open the repo root in a code editor and open any HTML file in the browser. If there is no HTML yet, create an `index.html` alongside `styles.css` and test styling by opening it.
- If asked to provide commands in PRs, suggest using lightweight commands developers can run (macOS/zsh):

  - Use a tiny static server (optional, mention in PR): `python3 -m http.server 8000` from repo root, then open http://localhost:8000

## Integration points & external dependencies

- None discovered in the current snapshot. If you add dependencies, place them in a manifest (`package.json`, `requirements.txt`, etc.) and document expected commands to install and run.

## Editing and PR guidance for the agent

- Keep changes focused and small. Each PR must include:
  - A 1–2 line PR description of intent.
  - Files changed with short reasons for each change.
  - How the change was validated locally (browser preview, screenshot, or short test note).

## Where to look next (useful files/locations)

- `styles.css` — primary styling file.
- Root of repository — the place to add `index.html`, `README.md`, or minimal build manifests if the feature request requires them.

## When you should ask the user before proceeding

- Adding a build system, installing packages, or introducing backend/server code.
- Renaming or moving `styles.css` or making global structural changes.

## Short example (how to edit safely)

- Want to change the body background color? Edit `styles.css` and in your PR include:
  - The exact CSS diff lines.
  - A note: "Previewed at http://localhost:8000/index.html (created a temporary index.html) — background color updated to #f5f5f5."

---

If anything in this file looks incomplete or you expected other source files (HTML, JS, or config files), tell me what you expect and I will update this guidance and the repo accordingly.
