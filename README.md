# Vants-Proteger

 anuncio/cuartel-agentes
Repo de la organización VANTSNET. La rama `main` está vacía ahora mismo: el
contenido anterior se retiró en los PR #2 y #3. Este README deja constancia
del anuncio del ecosistema.

## Agentes: el cuartel es flask-Agents

**Anuncio del ecosistema VANTS GAMES:** el cuartel de los agentes es
[`VANTSNET/flask-Agents`](https://github.com/VANTSNET/flask-Agents): ahí vive
el código de todos los agentes, los viejos y los nuevos, y su web es
https://vants-ai.vercel.app/. Los demás repos de la org se comunican con el
cuartel como clientes (colas de Neon y VANTS-BUS) y no guardan copias de su
código.
=======
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
 main
