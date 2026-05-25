# HBSport Web - GitHub Pages

Landing corporativa estática de HBSport lista para desplegar en GitHub Pages.

## Stack

- HTML5
- CSS3
- Google Fonts (Barlow + Space Grotesk)
- Sin backend
- Sin dependencias de Python/Django

## Estructura

```text
.
├── index.html
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── images/
│       ├── favicon.png
│       └── hbsport.png
└── README.md
```

## Contenido actual

- Hero con CTA a WhatsApp.
- Menú anclado por secciones.
- Servicios:
  - Escapes
  - Mecánica
  - Neumáticos
  - Suspensiones
  - Chapa y pintura
  - Pulidos
  - Restauraciones
- Quiénes somos.
- Contacto y horario.
- Ubicación con enlace a Google Maps.
- Instagram oficial.
- Botón flotante de WhatsApp.
- Favicon de marca.

## Deploy en GitHub Pages

1. Sube esta rama (`develop-pages`) a GitHub.
2. En GitHub: `Settings` -> `Pages`.
3. En `Build and deployment` selecciona:
   - `Source`: `Deploy from a branch`
   - `Branch`: `develop-pages`
   - `Folder`: `/ (root)`
4. Guarda y espera el publish.

## Desarrollo local

No requiere instalación.

Opciones:
- Abrir `index.html` directamente en navegador.
- O servir local con un servidor estático:

```bash
python3 -m http.server 8080
```

Luego abrir: `http://localhost:8080/`
