# Vants-Proteger

Código de VantsSeguridad: el sitio estático de VANTS GAMES con autenticación **Auth0** y datos en **Neon**. Hay una versión nueva en Vue dentro de `web/`.

Las medidas de seguridad de toda la plataforma no están aquí, sino en la [documentación de seguridad](https://vantsgg.mintlify.app/referencia/seguridad).

## Estructura

| Ruta | Contenido |
| --- | --- |
| Raíz | SPA estática: HTML, JS y CSS (`app.js`, `auth0-config.js`, `faceit.js`, `admin.js`) |
| `web/` | App Vue con Vite: vistas de inicio, jugadores, torneos, ranking, planes, calendario, cuenta y admin. Incluye pruebas (Vitest y Playwright) |
| `bot/` | Bot de Discord en Python (versión anterior; ver [Bot de Discord](https://vantsgg.mintlify.app/referencia/bot-de-discord)) |
| `desktop/` | App de escritorio con Tauri |
| `android/` | App Android (TWA) |
| `neon-functions/` | `discord-notify`, `steam-login` y `stripe-webhook` |

## Integraciones

- **Auth0**: identidad.
- **Neon**: PostgreSQL con Data API.
- **Stripe**: pagos de planes.
- **Steam**: login con OpenID.
- **FACEIT**: vinculación de cuenta y partidas.
- **Discord**: bot y notificaciones.

## Despliegue y CI

Se publica como sitio estático en GitHub Pages y Netlify. Workflows: `web-ci`, `deploy-web`, `desktop-build` y `android-build`.

## Más información

El repositorio incluye [`ARCHITECTURE.md`](ARCHITECTURE.md) con diagramas completos, [`web/ADMIN.md`](web/ADMIN.md) y [`bot/SETUP.md`](bot/SETUP.md). La documentación interna está en [vantsgg.mintlify.app](https://vantsgg.mintlify.app/repos/vants-seguridad).

## Seguridad

No subas secretos, tokens, claves ni archivos `.env`. Si encuentras una vulnerabilidad, no la publiques en un issue: avisa en privado al equipo de VANTS.
