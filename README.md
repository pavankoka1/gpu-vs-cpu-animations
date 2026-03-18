# GPU vs CPU Animations

Compare **width/height** (CPU, layout-thrashing) vs **transform/scale** (GPU, compositor-only) animation approaches side by side.

## Live demo

Deploy to GitHub Pages, Vercel, or Netlify — it's a single static HTML file.

## Run locally

```bash
# Option A: Open directly
open index.html

# Option B: Local server
npx serve . -p 3333
# Open http://localhost:3333
```

## How to test

- **Desktop**: Chrome DevTools → Toggle device toolbar (Cmd+Shift+M) → pick iPhone
- **Safari iOS**: Open on a real device for the clearest performance difference

## What to look for

| Approach        | Expected behavior                          |
| --------------- | ------------------------------------------ |
| Width & Height  | CPU spikes, FPS drops, possible jank       |
| Transform/Scale | Smoother FPS, lower CPU, fewer frame drops |

Click each toggle during the animation and watch the FPS counter. Use **Stress** to run both at once.

## Deploy

### GitHub Pages

1. Push to GitHub
2. Settings → Pages → Source: Deploy from branch
3. Branch: `main`, folder: `/` (root)

### Vercel

```bash
npx vercel
```

### Netlify

```bash
npx netlify deploy --prod --dir=.
```
