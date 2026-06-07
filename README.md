# Iván Ruiz López

Sitio web personal estático de Iván Ruiz López, pensado para publicarse con GitHub Pages. El sitio contiene una página principal en HTML con una presentación breve y una hoja de estilos CSS para la apariencia responsive.

## Estructura del repositorio

```text
.
├── .github/
│   └── workflows/
│       └── saludo.yml
├── assets/
│   └── css/
│       └── styles.css
├── index.html
└── README.md
```

- `index.html`: página principal del sitio.
- `assets/css/styles.css`: estilos base y responsive del sitio.
- `.github/workflows/saludo.yml`: flujo de GitHub Actions que se ejecuta al hacer push a `main`.
- `README.md`: documentación del proyecto.

## Uso local

Este proyecto es un sitio estático y no requiere instalación de dependencias ni proceso de compilación.

### Abrir directamente en un navegador

1. Clona o descarga el repositorio.
2. Abre el archivo `index.html` directamente con tu navegador web, por ejemplo haciendo doble clic sobre el archivo o usando la opción de abrir archivo del navegador.

### Usar un servidor local

Como alternativa, puedes servir la raíz del repositorio con Python:

```bash
python3 -m http.server 8080
```

Después abre esta URL en el navegador:

```text
http://localhost:8080
```

## Despliegue en GitHub Pages

Después de fusionar o publicar estos cambios en la rama principal, configura GitHub Pages para servir el sitio desde la rama principal (`main`) y desde la raíz del repositorio (`/`).