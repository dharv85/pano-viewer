# pano-viewer — ArcGIS Experience Builder custom widget

Static host of the built **360 Panorama Viewer** ExB widget (`exbVersion 1.18`, targets ArcGIS Enterprise 12.0). Register in Portal via My Content → Add Item → Application → Experience Builder widget → paste the manifest URL below.

**Manifest URL:** https://dharv85.github.io/pano-viewer/manifest.json

## What it does
Uploads 360° equirectangular panoramas (Twinmotion exports) to Portal as Image items, organized by site (vantage point) × phase (project state). End users pan/zoom the scene and toggle phases with view angle preserved for direct visual comparison — built for SLR mine reclamation deliverables.

## Repo contents
- `manifest.json`, `config.json`, `icon.svg` — widget metadata
- `dist/runtime/widget.js` — runtime bundle (Pannellum bundled in, ~76 KB minified)
- `dist/setting/setting.js` — settings-panel bundle (~12 KB minified)

## Rebuilding
Source lives outside this repo at `/Users/dan/Desktop/Visual_Sims/pano-viewer/` on Dan's dev machine. Rebuild with `npm run build:prod` in `~/Downloads/exb-1.18/client/` (ExB 1.18 Developer Edition, Node 22), then copy `dist/widgets/pano-viewer/*` into this repo and `git push`. GitHub Pages redeploys automatically in ~30 seconds.
