# test-paginas.cauce-ingenieria.com

Ambiente de pruebas de los proyectos web de **Cauce Ingeniería S.A.S.**
Cada cambio se publica aquí antes de salir a producción, para revisarlo y aprobarlo.

## Cómo funciona

Este repo es el sitio de GitHub Pages de la organización y tiene el dominio `test-paginas.cauce-ingenieria.com`.
Todo repo de la organización que publique en Pages aparece automáticamente como una carpeta:

| Repo | Ambiente de pruebas | Producción |
|---|---|---|
| [`landings`](https://github.com/Cauce-Ing-LABS/landings) | [/landings/](https://test-paginas.cauce-ingenieria.com/landings/) | [cauce-ingenieria.com](https://cauce-ingenieria.com) |

La página de inicio (`index.html`) muestra una tarjeta por proyecto.

## Agregar un proyecto

1. En el repo del proyecto, configura el workflow de deploy a test (ver `.github/workflows/deploy-test.yml` en `landings`)
   y en **Settings → Pages → Source** elige **GitHub Actions**.
2. Aquí, en `index.html`, agrega un bloque a la lista `PROYECTOS`:

   ```js
   {
     nombre: "Nombre visible",
     carpeta: "nombre-del-repo",
     descripcion: "Qué es, en una línea.",
     estado: "en revisión",          // o "borrador"
     produccion: "dominio-real.com"   // opcional
   }
   ```

## Importante

- Todo lo que se publica aquí es **visible para cualquiera que tenga el enlace**. No publiques datos de clientes ni secretos.
- Google no indexa este ambiente (`robots.txt` y `noindex` en cada página).

## Licencia

Todos los derechos reservados · Cauce Ingeniería S.A.S. Ver `LICENSE`.
