# DEOC² Studio — sitio multipágina listo para despliegue

## Abrir localmente
Abra `index.html` o ejecute:

```bash
python -m http.server 8000
```

## Publicar
Puede arrastrar **esta carpeta completa** a Netlify Drop o subirla a cualquier hosting estático. No publique solo `index.html`: los recursos y páginas están organizados en subcarpetas.

## Configurar dominio para SEO absoluto
Los canonical son relativos y funcionan al desplegar. Para convertir sitemap, Open Graph y JSON-LD a URLs absolutas, ejecute:

```bash
python set-domain.py https://su-dominio.com
```

Después vuelva a subir la carpeta.

## Antes de producción
1. Validar identidad, contenidos, oferta, datos de contacto y supuestos descritos en `AUDITORIA_REFERENCIAS.md`.
2. Reemplazar contenido demostrativo y conectar formularios, pagos, autenticación o APIs reales.
3. Revisar privacidad, términos, cookies, accesibilidad y requisitos de la jurisdicción.
4. Probar todos los flujos con usuarios y dispositivos reales.

## SEO / GEO / AEO incluidos
- títulos y descripciones únicas;
- canonical por página;
- Open Graph y Twitter Card;
- JSON-LD de entidad, website, página, FAQ y tipos especializados;
- HTML semántico, encabezados y breadcrumbs;
- `robots.txt`, `sitemap.xml`, `manifest.webmanifest`;
- `llms.txt` y `knowledge.json`;
- respuestas directas y FAQ redactadas para motores de respuesta;
- imágenes locales con texto alternativo y dimensiones;
- página 404, privacidad y accesibilidad.

## Publicar en Netlify (sitio estático)
1. En Netlify, elija **Add new project → Import an existing project → GitHub**.
2. Seleccione `danielortegac/curso-de-ia`, rama `main`.
3. Configure el **Publish directory** como `.` (raíz); no requiere build command.
4. Active **Forms → Form detection** y lance un deploy nuevo si la detección estaba desactivada.
5. Verifique `contacto.html` y que el envío aparezca en **Forms**; configure notificaciones desde Netlify.

El contacto usa Netlify Forms con `POST`, honeypot y página `/gracias`; no es un sistema de login. La autenticación de usuarios no está implementada. No añada secretos al repositorio. Revise la política de privacidad y los contenidos provisionales antes de usarlo comercialmente.
