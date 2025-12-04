# Core Strength + Espresso AR — Street Sign (WebXR) (Minimal)

Single‑page, WebXR‑only AR experience using `<model-viewer>`. No A‑Frame, AR.js, or MindAR.

## Structure

```
AR-Street-Sign-WebXR-for-Core-Strength-Espresso/
├── index.html                 # Model preview + AR (one page)
├── vercel.json                # Asset headers + rewrite
├── CSE-AR-SIGN-NOV-2025.glb
├── CSE-AR-SIGN-NOV-2025.usdz
└── CSE-AR-SIGN-NOV-2025.usdc  # Source USD (packaged inside USDZ)
```

## Steps

1) Copy your GLB export into the project root as `CSE-AR-SIGN-NOV-2025.glb`.
   - Source: `/Users/joshjacobson/Documents/GitHub/AR-Street-Sign-Demo-for-Core-Strength-Espresso/CSE-AR-SIGN-NOV-2025.glb`
2) Create a USDZ bundle for Quick Look (packages the `.usdc` + textures):
   ```sh
   usdzip CSE-AR-SIGN-NOV-2025.usdz CSE-AR-SIGN-NOV-2025.usdc textures
   ```
   - Requires Xcode Command Line Tools (for `usdzip`).
3) Open `index.html` locally, or deploy to Vercel.

## Notes

- This is intentionally minimal to emulate the stability of your `core-strength-espresso-ar` sample.
- Animations: the GLB’s single clip is auto‑played. If clip name changes, update `animation-name`.
- Vercel config sets MIME for `.glb` under `/assets/`.
