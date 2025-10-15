# CartAI — Carta inteligente con IA (PWA)

Interfaz moderna para cartas de restaurantes con **chat asistente** y **edición ultra-fácil** desde Google Sheets. 100% estático, deploy en Vercel o GitHub Pages.

## ✨ Características
- **PWA** instalable (manifest + service worker)
- **UI Pro** (tema oscuro, acento azul/teal)
- **Edición de carta** vía **Google Sheets** (o `carta.json` local como fallback)
- **Botón de chat flotante** que abre el asistente (popup a tu GPT público)
- **Badges de alérgenos** por plato

## 🔧 Configuración rápida
1. Abre `index.html` y ajusta:
   ```js
   const SHEET_ID = "TU_SHEET_ID";   // déjalo vacío para usar carta.json
   const SHEET_NAME = "Sheet1";
   const CHAT_URL = "https://chat.openai.com/g/tu-gpt"; // tu GPT público
   ```

2. (Opcional) Usa `carta.json` para datos demo o como reserva si falla la Sheet.

## 🧾 Estructura de Google Sheet
Columnas esperadas: `categoria | nombre | precio | alergenos | descripcion | visible`  
Publica la sheet (o usa el endpoint gviz por defecto) y pega el **SHEET_ID**.

## 🚀 Deploy
- **Vercel**: arrastra la carpeta al panel de Vercel → Deploy.
- **GitHub Pages**: Settings → Pages → Branch `main` / root.

## 🧠 Asistente (GPT)
Crea tu GPT en ChatGPT, sube la carta (Sheet o JSON) como *Knowledge* y usa la URL pública en `CHAT_URL`.

¡Listo para producción ligera! ⚡