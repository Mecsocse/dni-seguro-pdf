# Offline ID Card Watermark & Redact Tool (Single HTML File · MIT)

> Zero-server, zero-dependency HTML5 Canvas utility to combine both sides of an ID card, driver's license, or passport in **grayscale**, stamp a **card-fitted diagonal watermark**, and permanently **blackout or pixelate** sensitive numbers completely offline inside your browser.

[![Live Demo](https://img.shields.io/badge/Live_Demo-GitHub_Pages-2563eb)](https://mecsocse.github.io/dni-seguro-pdf/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## English Documentation

### Why this exists

Hotels, landlords, vacation rentals, gyms, and administrative forms routinely ask for a scan of both sides of a national ID or driver's license. Sending full-color, unredacted scans to third parties or uploading them to ad-heavy "cloud PDF converters" creates permanent identity-theft exposure.

Most cybersecurity agencies (EU GDPR authorities / INCIBE / NIST guidance) recommend keeping ID copies:
1. **In Black & White (Grayscale)** — harder to reuse in automated color/liveness spoofing.
2. **With a specific Diagonal Watermark** fitted directly across the ID card indicating recipient and purpose.
3. **With non-essential fields Redacted/Pixelated** (such as card support numbers, signatures, or CAN codes).

### Features & Security Guarantees

- **100% Auditable Single File (`index.html`, zero external scripts/CDNs):** Zero `fetch()`, zero telemetry, zero fonts loaded over the network. Works completely offline even after saving locally (`File → Save Page As`).
- **True Grayscale Conversion (Safari/iOS Safe):** Avoids `ctx.filter` browser bugs by converting luminance per pixel directly via `0.299R + 0.587G + 0.114B`.
- **Card-Clipped 3-Line Auto-Fit Watermark + Cropped PNG Export:** Keeps the entire custom watermark readable inside each card frame and exports either full A4 (`1240 × 1754 px` @ 150 DPI, ISO/IEC 7810 ID-1 `85.6 × 54 mm` scale) or tight card-cropped PNGs.
- **Irreversible Blackout & Mosaic Pixelation:** Drag boxes directly over sensitive fields (CAN, serial number, signature). Pixelated areas are downsampled directly on Canvas before watermarking so original digits cannot be reconstructed in PDF editors.
- **Instant `EN / ES` Language Toggle:** Automatically defaults to English or Spanish based on `navigator.language`, with one-click switching.
- **Direct Export:** Download A4 `.png`, tight **Cropped PNG**, or save cleanly as A4 `.pdf` via native `@media print`.

### Usage

1. Download [`index.html`](index.html) or launch the [Live GitHub Pages Demo](https://mecsocse.github.io/dni-seguro-pdf/).
2. Select front and back photos (nothing leaves browser RAM).
3. Select **Blackout Box** or **Pixelate Zone** and drag over unnecessary numbers/signatures.
4. Customize the watermark text (e.g. `ID COPY - APARTMENT LEASE ONLY - NOV 2026`).
5. Click **Download A4 PNG**, **Cropped PNG**, or **Save PDF (A4)**.

If you need multi-page batch layout and direct mobile `.pdf` file export (especially convenient on Android/iOS), there is also a free full web composer:
- **English:** [MiniTools ID Card Watermark & Redact PDF](https://getminitools.com/id-card-watermark-pdf/)
- **Español:** [MiniTools DNI Dos Caras Protegido en PDF](https://getminitools.com/es/dni-dos-caras-en-pdf/)
- **Português:** [MiniTools Documento Frente e Verso em PDF](https://getminitools.com/pt/documento-frente-e-verso-pdf/)

---

## Documentación en Español

Utilidad abierta en **un único archivo HTML (`index.html`)** sin librerías externas ni peticiones de red para juntar las dos caras del DNI/NIE en **blanco y negro**, cruzar una **marca de agua diagonal ajustada a la tarjeta** y **tapar o pixelar datos sensibles** (CAN, número de soporte, equipo o firma) 100% en la memoria Canvas del navegador.

### Novedades (v1.1 — con mejoras de la comunidad)

- **💧 Texto ajustado dentro de cada cara del DNI + `✂️ PNG recortado` (PR #1 de [@otger](https://github.com/otger)):** Dibuja 3 líneas diagonales centradas y autoescaladas dentro de los bordes de cada tarjeta para que el texto siempre se lea completo, además de permitir descargar solo la zona recortada de las tarjetas.
- **⬛ Censura y pixelado irreversible (petición de la comunidad):** Selecciona `+ Rectángulo Negro` o `+ Pixelar Zona` y arrastra sobre el CAN, nº de soporte o firma antes de exportar. Los píxeles se reescriben directamente sobre el lienzo HTML5, de modo que ningún editor PDF puede levantar la caja negra para ver debajo.
- **🌐 Selector instantáneo `ES / EN`:** Detecta el idioma del navegador automáticamente y permite alternar español/inglés en un clic.
- **🪪 Tamaño real de tarjeta ISO ID-1 (85,6 × 54 mm)** sobre folio A4 (`1240 × 1754 px`).

### Uso rápido

1. Abre la **[Demo en GitHub Pages](https://mecsocse.github.io/dni-seguro-pdf/)** o descarga `index.html` para ejecutarlo incluso sin conexión a internet.
2. Sube el anverso y reverso del DNI.
3. Marca **Rectángulo Negro** o **Pixelar Zona** y tapa los campos prescindibles según el trámite (consulta nuestra [Guía AEPD/INCIBE](https://getminitools.com/es/guias/enviar-dni-seguro-marca-de-agua-aepd/) para hoteles, alquileres y KYC).
4. Descarga en **PNG (A4)**, **PNG recortado** o pulsa **Guardar PDF (A4)** con `Ctrl+P`.
5. Para generar directamente un binario `.pdf` multipágina desde el móvil iOS/Android sin pasar por el diálogo de impresión: **[MiniTools DNI Dos Caras en PDF](https://getminitools.com/es/dni-dos-caras-en-pdf/)**.

---

## License

MIT License — see [`LICENSE`](LICENSE).
