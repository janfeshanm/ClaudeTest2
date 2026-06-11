# Three.js Tree — Android PWA

An interactive 3D tree scene built with [Three.js](https://threejs.org/), optimised for Android phones.  
Features touch orbit/zoom, procedural tree with recursive branches, floating leaf particles, and a sky gradient.

## Running on your Android phone

### Option A — Local network (fastest)

1. Make sure your phone and computer are on the **same Wi-Fi**.
2. On your computer, serve the project:

```bash
npm start
# or: npx serve . -l 3000
```

3. Find your computer's local IP (e.g. `192.168.1.42`).
4. Open **Chrome** on your Android phone and go to:

```
http://192.168.1.42:3000
```

5. Tap the **⋮ menu → Add to Home screen** to install it as a full-screen app.

### Option B — GitHub Pages (no computer needed)

1. Push this repo to GitHub.
2. Go to **Settings → Pages → Deploy from branch → main / root**.
3. Open the generated `https://<user>.github.io/<repo>` URL on your phone.

### Option C — Any static host

Deploy the files to Netlify, Vercel, Cloudflare Pages, etc., then open the URL in Chrome on Android.

## Controls

| Gesture | Action |
|---------|--------|
| Drag one finger | Orbit around the tree |
| Pinch two fingers | Zoom in / out |
| Auto-rotate | Starts automatically, stops on first touch |

## Tech

- [Three.js r160](https://threejs.org/) — 3D engine (loaded from CDN)
- `OrbitControls` — mouse + touch camera control
- PWA manifest + service worker — "Add to Home Screen" on Android/iOS
- Zero build step — pure HTML + ES modules
