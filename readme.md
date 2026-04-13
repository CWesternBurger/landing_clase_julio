# Landing Consultorio Dental

Sitio estatico listo para desplegar en cualquier servidor web.

## Estructura principal

- `index.html`: entrada principal para produccion.
- `assets/css/styles.css`: estilos separados para cacheo y mantenimiento.
- `assets/img/`: imagenes locales (sin dependencia critica de terceros).
- `manifest.webmanifest`: metadatos PWA basicos.
- `robots.txt` y `sitemap.xml`: soporte SEO para rastreo.

## Como probar en local

Puedes abrir `index.html` directo en navegador, o usar un servidor local:

```powershell
cd .
python -m http.server 8080
```

Luego abre `http://localhost:8080`.

## Publicar en servidor

1. Sube todo el contenido del repositorio al directorio publico del hosting.
2. Verifica que `index.html` quede en la raiz del sitio.
3. Si cambias el dominio, actualiza estas rutas:
	- `index.html` (`canonical`, `og:url`, `og:image`, `twitter:image`)
	- `robots.txt` (`Sitemap`)
	- `sitemap.xml` (`loc`)

## Nota importante

Los metadatos apuntan a `https://www.sonrisanorte.com/` como dominio de ejemplo. Debes reemplazarlo por tu dominio real antes de publicar.
