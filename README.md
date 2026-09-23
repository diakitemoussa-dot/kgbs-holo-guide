# KGBS Holo-Guide — VPS2 Clean

Expérience immersive **NSDK 4.0 / Niantic Spatial** — VPS2 durable avec localisation précise 6DoF & fallback 3DoF sans repère physique.

- **Site VPS2** : `e39560f5-6d2f-4807-a20c-622452c8b41d`
- **Stack** : 8th Wall + NSDK 4.0 (VPS2), WebXR
- **Modèles** : `assets/robot.glb`, `assets/occlusion_mesh.glb`

## Structure

```
.
├── index.html          # Landing + UI Holo-Guide
├── bundle.js           # VPS2 manager + components (vps2-manager, occluder, robot-nav)
├── assets/
│   ├── robot.glb
│   └── occlusion_mesh.glb
└── external/runtime/   # Runtime NSDK
```

## Lancer en local

Ouvre `index.html` via un serveur local (requis pour WebXR) :

```bash
npx serve .
# ou
python -m http.server 8000
```

Puis ouvre `http://localhost:3000` ou `http://localhost:8000` sur mobile.

## Déploiement GitHub Pages

Le site est déployé automatiquement via **GitHub Pages** (branch `main`, dossier `/`).

URL : `https://diakitemoussa-dot.github.io/kgbs-holo-guide/`

> ⚠️ Le `bundle.js` contient un `developerToken` Niantic Spatial (90j). Pour un repo public, pense à le régénérer via Scaniverse Web > Site > Credentials si nécessaire et à ne pas le réutiliser hors POC.

## Scaniverse

- Generate Assets > Set as Production pour activer le VPS précis (6DoF)
- Sans payload : fallback Coarse 3DoF (GPS amélioré, indoor GPS-denied)

---
Kabakoo · KGBS · NSDK 4.0 · 2026
