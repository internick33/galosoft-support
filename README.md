# Galosoft Support · sitio web

Este sitio usa el mismo sistema de diseño que Galosoft Contable, con paleta propia: base oscura #0A1424 y acento cian #22D3EE.

## Estructura
- **Sitio:**
  - `index.html`: Inicio
  - `servicios.html`
  - `planes.html`
  - `nosotros.html`
  - `contacto.html`
  - `aviso-de-privacidad.html`
- **Landings** (sin menú, con el formulario arriba):
  - `mantenimiento-preventivo.html`
  - `impresoras.html`
  - `antivirus-corporativo.html`
- **`assets/`:** estilos, JS, favicon, ícono táctil y `og-support.png`, la imagen para las vistas previas.

## Publicar
1. Sube todo a `public_html` de galosoftsupport.com. La URL canónica es **https://galosoftsupport.com**, sin `www`; redirige `www` a esa versión.
2. En `assets/main.js`, pon la URL de tu webhook de n8n en `WEBHOOK`.
3. En el nodo Webhook de n8n:
   - Método POST.
   - Responder con código 200.
   - CORS: agrega `https://galosoftsupport.com`.

   El JSON que recibe trae estos campos: `nombre`, `telefono`, `equipos`, `necesidad`, `acepto`, `marca`, `origen`, `pagina`, `utm` y `fecha`.

## Teléfonos
- **WhatsApp de soporte:** 55 9317 8429. Es el número principal en el sitio y en el JSON-LD.
- **Teléfono común:** 55 3887 9954, como contacto adicional.

## Pendientes antes de publicar
Los marcadores aparecen en el sitio con contorno rojo punteado.
- [ ] URL del webhook de n8n (`assets/main.js`).
- [ ] Tiempo de respuesta (inicio, sección "Compromisos claros").
- [ ] Días de garantía en mano de obra (inicio).
- [ ] Marcas de impresoras que atiendes (inicio, FAQ, e `impresoras.html`).
- [ ] Tipos de impresora (tinta, láser) y si vendes consumibles o refacciones (`impresoras.html`).
- [ ] Marca del antivirus corporativo (`antivirus-corporativo.html`).
- [ ] Contenido de cada plan y plazo mínimo, si existe (`planes.html`).
- [ ] Cookies o analítica, si las agregas (aviso de privacidad).
- [ ] Reseñas: la sección está comentada en `index.html`. Actívala solo con reseñas reales.
- [ ] Logo definitivo. La "G" es provisional, igual que en Contable.
