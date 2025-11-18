# Sala de Belleza Martha — Sitio web (Astro + Tailwind)

Sitio web estático para el salón de belleza “Martha”, construido con Astro 5 y Tailwind CSS 4 (vía `@tailwindcss/vite`). Incluye navegación responsive con menú hamburguesa, secciones de servicios, quiénes somos y contacto.

## ✅ Requisitos

- Node.js 18 o superior
- pnpm (recomendado) o npm

## ⚙️ Instalación

```bash
pnpm install
```

## � Scripts

- `pnpm dev`: inicia el servidor de desarrollo en `http://localhost:4321`
- `pnpm build`: genera la versión de producción en `./dist/`
- `pnpm preview`: vista previa local de la build de producción
- `pnpm astro ...`: comandos de la CLI de Astro (p. ej. `astro check`)

## 🗂️ Estructura del proyecto

```text
/
├── public/
│   └── imagenes/                  # Imágenes públicas
├── src/
│   ├── assets/
│   │   ├── favicon.svg
│   │   └── icons/                 # Iconos en componentes Astro
│   ├── components/
│   │   ├── Navbar.astro
│   │   ├── Header.astro
│   │   ├── Hero.astro
│   │   ├── Footer.astro
│   │   └── Chatbotia.astro
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   └── index.astro
│   ├── sections/
│   │   ├── Inicio.astro
│   │   ├── Servicios.astro
│   │   ├── Quienes.astro
│   │   └── Contacto.astro
│   └── styles/
│       └── global.css             # Estilos globales
├── astro.config.mjs               # Configuración Astro + Tailwind (Vite plugin)
├── package.json
└── pnpm-lock.yaml
```

## 🎨 Estilos

- Tailwind CSS 4 vía plugin `@tailwindcss/vite` configurado en `astro.config.mjs`.
- Estilos adicionales en `src/styles/global.css`.

## 🧩 Notas de implementación

- El menú hamburguesa móvil se controla en `Navbar.astro` con un script inline que espera a `DOMContentLoaded` y alterna la clase `show` en `.nav-links`.
- Para colores con transparencia se usan valores RGBA, por ejemplo: `background: rgba(255, 91, 141, 0.7);`.

## 🚀 Despliegue

El proyecto genera HTML estático en `dist`, compatible con cualquier hosting estático (Netlify, Vercel, GitHub Pages, etc.).

Pasos típicos:

1. `pnpm build`
2. Sube la carpeta `dist/` a tu proveedor o conecta el repositorio para builds automáticas.

## � Licencia

Proyecto con fines demostrativos. Ajusta o añade licencia según tus necesidades.
