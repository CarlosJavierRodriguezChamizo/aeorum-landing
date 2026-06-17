# AEORUM — Landing Page

Landing page de **AEORUM**, aceite de oliva virgen extra de Jaén (100% Arbequina), orientada al mercado alemán. Markteinführung 2026.

Estética xilográfica en verde oscuro + crema/marfil, con tipografía Barlow Condensed / DM Sans, animaciones GSAP y un formulario de captación de leads (Vormerkung) con consentimiento RGPD.

## Estructura

Sitio estático, sin build. Se sirve tal cual.

```
index.html            # Landing principal
impressum.html        # Aviso legal (§5 DDG/TMG)
datenschutz.html      # Política de privacidad (DSGVO/RGPD)
kontakt.html          # Contacto
favicon.svg           # Favicon (oliva + hoja)
laurel.svg            # Marco decorativo (laurel) — fondos oscuros
laurel-dark.svg       # Marco decorativo (laurel) — fondos claros
*.jpg / *.png         # Imágenes (lata, cosecha, ensalada, paisaje, patrón…)
```

## Desarrollo local

Cualquier servidor estático sirve. Por ejemplo:

```bash
python3 -m http.server 8000
# o
npx serve .
```

Luego abre http://localhost:8000

## Despliegue — GitHub Pages (automático)

El despliegue está automatizado con GitHub Actions (`.github/workflows/deploy.yml`):
cada `push` a `main` publica el sitio.

**Configuración inicial (una sola vez):**

1. Sube el repositorio a GitHub.
2. En **Settings → Pages → Build and deployment**, selecciona **Source: GitHub Actions**.
3. Listo. A partir de ahí, cada push a `main` ejecuta el workflow y publica en
   `https://<usuario>.github.io/<repo>/`.

Puedes ver el estado en la pestaña **Actions** y lanzarlo a mano con **Run workflow**
(evento `workflow_dispatch`).

El archivo `.nojekyll` evita el procesado por Jekyll.

## Pendiente antes de producción

- Rellenar los datos `[entre corchetes]` en `impressum.html`, `datenschutz.html` y `kontakt.html`.
- Auto-alojar Google Fonts y GSAP (ahora vía CDN) para cumplir RGPD de forma estricta.
- Conectar el formulario a un backend / servicio de email (ahora guarda en `localStorage` y exporta CSV en local).
- Optimizar/convertir las imágenes a WebP.

---

🤖 Generated with [Claude Code](https://claude.com/claude-code)
