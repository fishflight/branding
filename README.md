# branding

Brand kit for **Fish Flight Entertainment** — logos, color palette, typography, voice/tone, and machine-readable brand data.

## Brand kit page

`index.html` is a static, no-build brand kit page covering logo usage & downloads, color, typography, brand story, and voice. It's built to be served directly by GitHub Pages from this repo.

- **Live site**: not yet enabled — see "Enable GitHub Pages" below. Once enabled it will be at `https://<org-or-user>.github.io/branding/`.
- **Preview locally**: open `index.html` directly in a browser, no server needed.

## Brand assets

All logo source files live at the repo root (PSD/TIF hi-res masters plus web-ready JPG/PNG exports and favicon crops). `design-tokens.json` documents every variant — which background it's for, and minimum display size — alongside the color and typography values.

## For AI agents

`.claude/skills/fish-flight-brand/SKILL.md` is a Claude Code Skill that teaches an agent to apply the Fish Flight brand (colors, typography, logo choice, voice) automatically when generating on-brand copy or assets for this project. It reads its exact values from `design-tokens.json`.

## Enable GitHub Pages

1. Push this branch and merge it into `main`.
2. In GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, then pick **Branch: main / (root)**.
3. The brand kit page will publish at `https://<org-or-user>.github.io/branding/`.

Or from the CLI, once merged to `main`:

```sh
gh api -X POST repos/{owner}/{repo}/pages -f "source[branch]=main" -f "source[path]=/"
```

## Cut a GitHub Release

To publish a versioned, downloadable bundle of the design tokens and the agent skill:

```sh
zip -r fish-flight-brand-skill.zip .claude/skills/fish-flight-brand
git tag v1.0.0
git push origin v1.0.0
gh release create v1.0.0 \
  design-tokens.json \
  fish-flight-brand-skill.zip \
  --title "Fish Flight Brand Kit v1.0.0" \
  --notes "Design tokens (colors, typography, logo refs) and the Claude Code brand skill."
```
