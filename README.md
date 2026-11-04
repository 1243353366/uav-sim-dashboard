# UAV Sim Dashboard

Clean, deploy-only repository: the public dashboard for the **UAV Safe Sim**
research platform, published as a static-assets Cloudflare Worker.

The research code (simulation core, tests, docs) lives in
[uav-safe-sim-v2](https://github.com/1243353366/uav-safe-sim-v2) — this repo
contains only what Cloudflare needs to deploy.

## Structure

```
public/index.html   the dashboard (single file, no build step)
wrangler.jsonc      assets-only Worker config
```

## Deploy

Connect this repo in the Cloudflare dashboard (Workers & Pages → Create →
Connect to Git) and set the deploy command:

```
npx wrangler deploy
```

Output: `https://uav-sim-dashboard.<account>.workers.dev`

## Validate locally

```
npx wrangler deploy --dry-run
```

Content is derived from the Apache-2.0 licensed uav-safe-sim project.

---

Thanks for reading. More of my work: [github.com/1243353366](https://github.com/1243353366).
