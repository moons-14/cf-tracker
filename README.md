# CF Tracker
A simple BitTorrent tracker on Cloudflare Workers.

## How to run
```bash
pnpm install
pnpm run dev
```

## Deployment
```bash
pnpm run deploy
```

## TypeScript types for Cloudflare Workers bindings
[For generating/synchronizing types based on your Worker configuration run](https://developers.cloudflare.com/workers/wrangler/commands/#types):

```bash
pnpm run cf-typegen
```

Pass the `CloudflareBindings` as generics when instantiation `Hono`:

```ts
// src/index.ts
const app = new Hono<{ Bindings: CloudflareBindings }>()
```
