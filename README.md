# TGU · Encomiendas y courier

Proyecto independiente de React + Vite. No requiere Base44 ni servidor para mostrar la web.

## Requisitos

- Node.js 20.19+ (recomendado Node.js 22 LTS)
- npm

## Ejecutar en Visual Studio Code

1. Abre esta carpeta en VS Code.
2. Abre Terminal → New Terminal.
3. Ejecuta `npm install`.
4. Ejecuta `npm run dev`.
5. Abre la dirección local que indique Vite (normalmente `http://localhost:5173`).

## Comprobar la versión de producción

```bash
npm run build
npm run preview
```

## Desplegar a GitHub Pages

```bash
npm run deploy
```

Esto genera la carpeta `dist` y publica el sitio con `gh-pages`.

## Publicar en GitHub Pages

1. Sube el contenido del proyecto a un repositorio GitHub.
2. En el repositorio entra en Settings → Pages.
3. En Build and deployment selecciona GitHub Actions.
4. Puedes usar el workflow `Deploy to GitHub Pages` si se agrega desde la pestaña Actions o crear `.github/workflows/deploy.yml` con el workflow de Vite para GitHub Pages.
5. En `vite.config.js`, `base: './'` deja las rutas de los archivos preparadas para un sitio bajo el nombre del repositorio.

## Datos y editor local

El contenido inicial está en `src/lib/site.js`. La sección `/admin` guarda los cambios en `localStorage` del navegador actual. Como GitHub Pages es hosting estático, esos cambios **no se sincronizan con otros visitantes ni con GitHub**. Para publicar cambios para todos, edita los datos en el código y vuelve a desplegar. No se incluye autenticación real ni una contraseña secreta en el cliente.

El ZIP original no incluía registros de servicios ni tarifas exportados desde Base44; por eso se conservan las secciones visuales, pero las listas comienzan vacías hasta que agregues tus datos.

# PRUEBA
