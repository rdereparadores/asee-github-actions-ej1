# Iván Ruiz López

Sitio web personal estático de Iván Ruiz López, pensado para publicarse con GitHub Pages. El sitio contiene una página principal en HTML con una presentación breve y una hoja de estilos CSS para la apariencia responsive.

## Estructura del repositorio

```text
.
├── .github/
│   └── workflows/
│       ├── pages.yml
│       └── saludo.yml
├── .gitignore
├── .nojekyll
├── assets/
│   └── css/
│       └── styles.css
├── index.html
└── README.md
```

- `index.html`: página principal del sitio.
- `assets/css/styles.css`: estilos base y responsive del sitio.
- `.gitignore`: patrones básicos para archivos locales, IDEs, dependencias y temporales.
- `.nojekyll`: evita el procesamiento con Jekyll en GitHub Pages.
- `.github/workflows/pages.yml`: workflow de GitHub Actions para publicar el sitio en GitHub Pages.
- `.github/workflows/saludo.yml`: flujo auxiliar de GitHub Actions que se ejecuta al hacer push a `main`; no participa en el despliegue.
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

El despliegue del sitio estático se realiza mediante GitHub Pages Actions con el workflow `.github/workflows/pages.yml`. Al ejecutarse sobre la rama principal, el workflow empaqueta el contenido estático del repositorio y lo publica en GitHub Pages.

Para usar este flujo, en la configuración del repositorio en GitHub ve a **Settings > Pages** y selecciona **GitHub Actions** como fuente (*source*) de GitHub Pages. No es necesario configurar Pages para servir desde una rama o desde la raíz del repositorio, porque la publicación la gestiona el workflow.

Nota de alcance local del sprint: la activación/configuración remota de GitHub Pages y la comprobación de la URL pública quedan fuera de la verificación local. En local solo se valida que el sitio estático puede servirse y que la documentación describe el flujo de despliegue esperado.