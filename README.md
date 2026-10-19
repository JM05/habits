# Hábitos

Tracker de hábitos personal, mobile-first y local-first.

- Vista **Hoy** en lista con progreso del día, **Semana** y **Mes** con porcentajes, rachas y calendario.
- Hábitos diarios (sí/no o con contador) y de "X veces por semana".
- **Tus datos viven solo en tu dispositivo.** Este repositorio contiene únicamente la app vacía.
- Respaldo y restauración con un archivo JSON.

## Publicarlo en GitHub Pages (una sola vez)

1. Entra a github.com → botón **New repository** → nombre `habits` → **Public** → **Create repository**.
2. En el repositorio vacío, toca **uploading an existing file**.
3. Arrastra estos archivos: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, `README.md` → **Commit changes**.
4. Ve a **Settings → Pages** → en *Branch* elige `main` y carpeta `/ (root)` → **Save**.
5. Espera 1–2 minutos. Tu link será `https://TU-USUARIO.github.io/habits/`.

## Instalarlo en el iPhone

1. Abre el link en **Safari**.
2. Toca **Compartir → Agregar a pantalla de inicio**.
3. Usa **siempre** ese ícono. Safari y el ícono guardan los datos por separado.

## Respaldo

- Pestaña **Respaldo → Exportar respaldo → AirDrop** a tu laptop (o "Guardar en Archivos"). Una vez por semana.
- Para restaurar: **Respaldo → Restaurar desde archivo**.
- **Nunca subas el archivo `habitos-respaldo-*.json` a este repositorio:** contiene tu historial.

## Actualizar la app

Sube la nueva versión de `index.html` al repositorio (Add file → Upload files). Tus datos no se tocan: viven en el iPhone, no en los archivos.

## Formato de datos

```json
{
  "version": 1,
  "habits": [{ "id": "…", "name": "Tomar agua", "emoji": "💧", "freq": "daily", "type": "count", "target": 4, "unit": "vasos", "weeklyTarget": 3, "createdAt": "2026-10-19" }],
  "logs": { "2026-10-19": { "<id del hábito>": 2 } },
  "meta": { "created": "2026-10-19", "lastBackup": null }
}
```

Formato simple y abierto, pensado para importarse después en el Personal OS.
