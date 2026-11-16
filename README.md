# 🪪 DNI Seguro Offline (Client-Side ID Card Watermark & B&W Generator)

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Utilidad **100% offline y Open Source** en un único archivo HTML/JS sin dependencias externas para proteger copias del **DNI, NIE, pasaporte o tarjeta de identidad** antes de enviarlas a hoteles, inmobiliarias, gimnasios o trámites.

> 🌐 **Versión Web Completa (con exportación directa a archivo PDF A4 multipágina y escala real 85,6 × 54 mm):**  
> 👉 [https://getminitools.com/es/dni-dos-caras-en-pdf/](https://getminitools.com/es/dni-dos-caras-en-pdf/)  
> 👉 Português (RG/CNH): [https://getminitools.com/pt/documento-frente-e-verso-pdf/](https://getminitools.com/pt/documento-frente-e-verso-pdf/)

---

## 🔒 ¿Por qué existe este proyecto?

Organismos de ciberseguridad como **INCIBE** y la Policía recomiendan **no enviar nunca fotos a todo color y sin marca de agua** del documento de identidad, para evitar suplantaciones de identidad o apertura fraudulenta de cuentas.

El problema habitual es que mucha gente busca *"juntar DNI en PDF"* y acaba **subiendo sus dos caras del DNI a servidores remotos desconocidos**.

Este repositorio ofrece una alternativa auditable en **un solo archivo `index.html`**:
- **Zero-Server / 100% Offline:** Funciona incluso sin conexión a internet. Ninguna imagen sale de tu dispositivo.
- **Sin dependencias ni trackers:** Cero librerías externas, cero llamadas de red.
- **Escala de grises real por luminancia:** Transforma píxel a píxel con `0.299R + 0.587G + 0.114B` (compatible en Safari/iOS/Chrome/Firefox).
- **Marca de agua diagonal repetida:** Texto personalizable (p. ej. `COPIA DNI - SOLO CHECK-IN HOTEL 16/11/2026`).
- **Exportación directa:** Descarga como imagen PNG protegida o guarda como **PDF A4** mediante `Imprimir → Guardar como PDF` del navegador.

---

## 🚀 Uso rápido

1. Descarga `index.html` o clona el repositorio:
   ```bash
   git clone https://github.com/Mecsocse/dni-seguro-pdf.git
   ```
2. Haz doble clic sobre `index.html` para abrirlo en tu navegador (puedes desconectar el Wi-Fi antes para comprobarlo).
3. Carga el anverso y reverso, ajusta el texto de marca de agua y descarga o imprime a PDF.

---

## 🛠️ Demo online ampliada (sin descargas)

Si necesitas generar directamente un archivo `.pdf` descargable en móvil con **tamaño exacto ISO ID-1 (85,6 × 54 mm)**, rotación libre y múltiples hojas A4:  
🔗 **[DNI Dos Caras en PDF — MiniTools](https://getminitools.com/es/dni-dos-caras-en-pdf/)** (100% client-side, código local en navegador).

---

## 📄 Licencia

Distribuido bajo licencia **MIT** ([ver `LICENSE`](LICENSE)).

---

## 🌍 English Summary

**Offline ID Card Privacy Tool (Zero-Server, Single HTML File)**  
Protect photos of your national ID, passport, or driver's license before sending them to hotels, landlords, or agencies: converts both sides to luminance grayscale and overlays a repeating diagonal purpose watermark strictly inside browser Canvas memory (zero uploads, zero dependencies).  

- Live full PDF A4 version (`85.6 × 54 mm` ISO scale): [getminitools.com/es/dni-dos-caras-en-pdf/](https://getminitools.com/es/dni-dos-caras-en-pdf/) | [Portuguese version](https://getminitools.com/pt/documento-frente-e-verso-pdf/)

