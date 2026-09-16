# UAV Sim Dashboard — Claude Code Project Context

## What this is
The deploy home for the UAV Safe Sim dashboard: a single static page
(`public/index.html`) published as an assets-only Cloudflare Worker.
The research platform itself (Python core, tests, polyglot components,
docs) lives in the `uav-safe-sim-v2` repository — that is the source of
truth for content. Edit there, copy the dashboard here.

## Commands
```bash
npx wrangler deploy --dry-run   # validate config + assets locally
npx wrangler deploy             # publish public/ to
                                # uav-sim-dashboard.<account>.workers.dev
```

## Rules of engagement
1. This repo stays lean: only `public/`, `wrangler.jsonc`, and docs.
   No build step, no dependencies, no framework.
2. Keep `wrangler.jsonc`'s `name` in sync with the repo name — the Worker
   URL derives from it.
3. Pushes to `main` trigger CI (wrangler dry-run) and the Cloudflare
   build. Both must stay green.
