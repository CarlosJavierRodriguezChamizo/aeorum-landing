# AURO — Aceite de Oliva Virgen Extra

Marca de aceite de oliva virgen extra **100% Picual** de cosecha temprana, **Sierra Mágina · Jaén**.
Estética mediterránea, artesanal, premium y editorial.

## Estructura

```
index.html            # Web principal (ES) — sistema visual / e-commerce gourmet
styles.css            # Sistema visual (variables, componentes, responsive)
assets/
  logo-auro.png         # Logotipo (AURO + rama de olivo + gota dorada)
  lata-auro.png         # Producto: lata 500 ml
favicon.svg           # Favicon (oliva + hoja)

de/                   # Landing de prelanzamiento mercado alemán (archivada)
  index.html            # Versión alemana
  index.es.html         # Versión española de esa landing
  impressum.html · datenschutz.html · kontakt.html   # Legales (DSGVO)
  *.jpg · *.svg         # Sus imágenes y marcos de laurel

.github/workflows/    # Despliegue automático a GitHub Pages
```

## Sistema visual (web principal)

- **Paleta** (variables `:root`): negro oliva `#171713`, verde oliva `#6F6B2E`, dorado `#B9983A`,
  crema `#F4EFE5`, terracota `#B64222`, blanco cálido `#FFFAF2`, gris texto `#5F5A4D`.
- **Tipografías**: Oswald (titulares), Inter (cuerpo/UI), Cormorant Garamond (editorial).
- **Componentes**: header, hero, bloque de origen, atributos (4 cards), sección producto
  (con selector de cantidad), bloque editorial y footer.
- **Botones**: principal, secundario y editorial.
- Textura papel sutil, separadores finos, formas geométricas y motivos de olivo.
- Responsive mobile-first.

## Desarrollo local

```bash
python3 -m http.server 8000   # o: npx serve .
```
Web principal → http://localhost:8000 · Landing alemana → http://localhost:8000/de/

## Despliegue — GitHub Pages (automático)

GitHub Actions (`.github/workflows/deploy.yml`) publica en cada `push` a `main`.
Configuración: **Settings → Pages → Source: GitHub Actions**.

- Web principal: `https://<usuario>.github.io/<repo>/`
- Landing alemana: `https://<usuario>.github.io/<repo>/de/`

### Dominio propio (opcional)

`CNAME.example` contiene el dominio. Renómbralo a `CNAME` cuando el DNS apunte a GitHub Pages
(ver IPs en el historial del archivo) y configúralo en **Settings → Pages → Custom domain**.

## Pendiente antes de producción

- Sustituir placeholders: precio, email (`hola@auro.es`), teléfono, redes.
- Conectar el botón **Comprar** a carrito/checkout real.
- Versión clara/transparente del logo para fondos oscuros (footer).
- Rellenar datos legales `[entre corchetes]` (en `de/` y crear las legales ES si se necesitan).
- Auto-alojar fuentes para RGPD estricto y optimizar imágenes a WebP.

---

🤖 Generated with [Claude Code](https://claude.com/claude-code)
