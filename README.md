# KGBS Holo-Guide ÔÇö VPS2 Clean

Exp├®rience immersive **NSDK 4.0 / Niantic Spatial** ÔÇö VPS2 durable avec localisation pr├®cise 6DoF & fallback 3DoF sans rep├¿re physique.

- **Site VPS2** : `e39560f5-6d2f-4807-a20c-622452c8b41d`
- **Stack** : 8th Wall + NSDK 4.0 (VPS2), WebXR
- **Mod├¿les** : `assets/robot.glb`, `assets/occlusion_mesh.glb`

## Structure

```
.
Ôö£ÔöÇÔöÇ index.html          # Landing + UI Holo-Guide
Ôö£ÔöÇÔöÇ bundle.js           # VPS2 manager + components (vps2-manager, occluder, robot-nav)
Ôö£ÔöÇÔöÇ assets/
Ôöé   Ôö£ÔöÇÔöÇ robot.glb
Ôöé   ÔööÔöÇÔöÇ occlusion_mesh.glb
ÔööÔöÇÔöÇ external/runtime/   # Runtime NSDK
```

## Lancer en local

Ouvre `index.html` via un serveur local (requis pour WebXR) :

```bash
npx serve .
# ou
python -m http.server 8000
```

Puis ouvre `http://localhost:3000` ou `http://localhost:8000` sur mobile.

## D├®ploiement GitHub Pages

Le site est d├®ploy├® automatiquement via **GitHub Pages** (branch `main`, dossier `/`).

URL : `https://diakitemoussa-dot.github.io/kgbs-holo-guide/`

> ÔÜá´©Å Le `bundle.js` contient un `developerToken` Niantic Spatial (90j). Pour un repo public, pense ├á le r├®g├®n├®rer via Scaniverse Web > Site > Credentials si n├®cessaire et ├á ne pas le r├®utiliser hors POC.

## Scaniverse

- Generate Assets > Set as Production pour activer le VPS pr├®cis (6DoF)
- Sans payload : fallback Coarse 3DoF (GPS am├®lior├®, indoor GPS-denied)

---
Kabakoo ┬À KGBS ┬À NSDK 4.0 ┬À 2026
