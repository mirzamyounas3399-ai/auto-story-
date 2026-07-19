# AutoStory AI — Local Setup

This app runs locally on your PC via Bun (no Cloudflare/cloud hosting needed).

## Requirements
- Install Bun: https://bun.sh (one-line installer, works on Windows/Mac/Linux)

## First-time setup
```bash
git clone <your-repo-url>
cd <project-folder>
bun run setup
```
This installs dependencies and builds the app (`bun install && bun run build`).

## Running it
```bash
bun run start
```
This starts the local server. Open the URL it prints (usually `http://localhost:3000`) in your browser.

## Notes
- `bun run build` outputs to `.output/`. If `bun run start` can't find the entry
  file, check `.output/server/` for the actual filename Nitro generated and
  update the `"start"` script in `package.json` to match.
- Every time you pull new code, re-run `bun run build` before `bun run start`.
