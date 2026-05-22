# HBSport Web (V1)

Web corporativa inicial para el taller **HBSport** (mecánica + chapa/pintura) desarrollada con Django.

## Estado del proyecto

Esta es la **primera versión** con landing page funcional y diseño base inspirado en la identidad visual de la marca (verde/negro).

Incluye:
- Hero principal con CTA a WhatsApp.
- Navegación por secciones.
- Sección de servicios.
- Sección "Quiénes somos".
- Sección de contacto y ubicación.
- Enlace a Instagram.
- Botón flotante de WhatsApp.
- Favicon personalizado.

## Tecnologías usadas

- Python 3.13
- Django 6.0.4
- HTML (Django Templates)
- CSS (estilos propios, responsive)
- `python-dotenv` (carga opcional de `.env`)

## Estructura principal

```text
hbsport/
├── config/                 # Configuración Django (settings, urls, wsgi, asgi)
├── core/                   # App principal (views + urls)
├── static/
│   ├── css/main.css        # Estilos globales de la web
│   └── images/
│       ├── favicon.png     # Favicon actual
│       └── hbsport.png     # Imagen usada en el hero (desktop)
├── templates/
│   ├── base.html
│   └── core/home.html      # Landing principal
├── manage.py
└── README.md
```

## Configuración de entorno

El proyecto carga variables desde `.env` (si existe). Variables relevantes:

```env
DJANGO_SECRET_KEY=...
DJANGO_DEBUG=True
DJANGO_ALLOWED_HOSTS=127.0.0.1,localhost,192.168.0.44
DJANGO_CSRF_TRUSTED_ORIGINS=
DJANGO_LANGUAGE_CODE=es-es
DJANGO_TIME_ZONE=Europe/Madrid
```

Notas:
- `ALLOWED_HOSTS` se parsea desde `DJANGO_ALLOWED_HOSTS` separado por comas.
- Si `python-dotenv` no está instalado en algún intérprete, el proyecto no rompe (fallback aplicado en `settings.py`).

## Cómo ejecutar en local

1. Crear/activar entorno virtual (opcional si ya usas conda/venv).
2. Instalar dependencias:

```bash
pip install django python-dotenv
```

3. Migraciones:

```bash
python3 manage.py migrate
```

4. Ejecutar servidor:

```bash
python3 manage.py runserver 0.0.0.0:8000
```

5. Abrir:
- `http://127.0.0.1:8000/`
- o `http://192.168.0.44:8000/` (según red local)

## Contenido actualizado en esta V1

- Paleta visual adaptada a la marca (negro + verde neón).
- Redes sociales: solo Instagram activo.
- Contacto:
  - Teléfono/WhatsApp: `+34 659 66 73 32`
  - Horario: **Lunes a viernes, 8:00 a 17:00**
- Ubicación:
  - San Cibrao das Viñas, Ourense
  - Enlace Google Maps: `https://maps.app.goo.gl/ZF8ri1K6f6GwHktw5?g_st=ic`
- Servicios actuales en cards:
  - Escapes
  - Mecánica
  - Neumáticos
  - Suspensiones
  - Chapa y pintura
  - Pulidos
  - Restauraciones
- Navegación superior alineada a la derecha (sin logo textual en la izquierda).
- Favicon configurado desde `static/images/favicon.png`.

## Próximos pasos sugeridos (V2)

- Reemplazar textos de placeholder por copy comercial final.
- Añadir formulario de contacto real (con backend + validación + antispam).
- Integrar mapa embebido.
- Mejorar SEO (meta tags Open Graph, sitemap, robots).
- Preparar despliegue (producción, estáticos, dominio, HTTPS).

