# Fractured Realms Launcher

- `npm start` — ejecutar · `npm run dist` — instalador Windows
- URLs en `src/config.js`.

## Manifest (`/launcher/manifest.json`)
```json
{ "version": "0.1.0",
  "files": [ { "path": "data/maps.pak", "url": "https://…/maps.pak", "sha256": "…", "size": 1234 } ] }
```
- `version`: cualquier cadena; si difiere de la instalada, se actualiza.
- `path`: relativo a la carpeta del juego (sin `..`).
- `sha256`: los archivos con hash distinto se vuelven a descargar.

Generarlo:
`node scripts/build-manifest.js ./game-assets 0.1.0 https://fracturedrealms.eu/launcher/files`
Sube `manifest.json` a `/launcher/` y los assets a `/launcher/files/`.
