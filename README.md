# 🇲🇽 JJMex Community | Hub Oficial

![Version](https://img.shields.io/badge/Versión-2.0.0-blue.svg?style=for-the-badge)
![Arquitectura](https://img.shields.io/badge/Arquitectura-Data--Driven-success.svg?style=for-the-badge)
![UI](https://img.shields.io/badge/UI-Glassmorphism_3D-8A2BE2.svg?style=for-the-badge)

Un punto de contacto digital (Link Hub) de alto rendimiento diseñado para concentrar la red de inteligencia vial, reportes de movilidad y comunidades de JJMex. 

Este proyecto deja atrás los "Linktrees" estáticos para ofrecer una experiencia inmersiva, reactiva y orientada a datos, simulando el comportamiento de una aplicación nativa premium.

## ✨ Características Élite (UX/UI)

* **Motor Físico 3D:** Tarjetas interactivas con efecto de profundidad e inclinación espacial (Tilt effect) basado en la posición del cursor o el giroscopio del dispositivo móvil.
* **Búsqueda en Tiempo Real (Command Palette):** Buscador ultrarrápido sin recarga de página. Accesible globalmente mediante el atajo de teclado `Cmd/Ctrl + K`.
* **Entorno Ambiental Reactivo:** Orbes de luz de fondo que siguen sutilmente el movimiento del usuario, creando una experiencia inmersiva profunda.
* **Branding Inteligente:** Las tarjetas detectan la plataforma (Telegram/WhatsApp) e iluminan sus bordes e íconos dinámicamente con los colores corporativos al interactuar.
* **Fricción Cero (Web Share API):** Integración nativa con el sistema operativo (iOS/Android) para compartir enlaces directamente a WhatsApp, Instagram o Mensajes.
* **Generación de Códigos QR:** Modal integrado de alto contraste para escanear y unirse a grupos al instante en entornos físicos.

## 🏗️ Arquitectura de Software

El proyecto utiliza una arquitectura **Data-Driven (Orientada a Datos)**. 
El archivo `index.html` funciona únicamente como un motor de renderizado (Plantilla). Todo el contenido, enlaces y categorías se administran exclusivamente desde el archivo `links.json`.

### ¿Cómo agregar un nuevo grupo?

No es necesario tocar el código HTML ni CSS. Simplemente abre el archivo `links.json` y añade un nuevo objeto al array `comunidades`:

```json
{
  "id": 6,
  "titulo": "Nuevo Grupo Élite",
  "descripcion": "Descripción del grupo para la tarjeta.",
  "url": "[https://chat.whatsapp.com/TU_ENLACE_AQUI](https://chat.whatsapp.com/TU_ENLACE_AQUI)",
  "plataforma": "whatsapp",
  "categoria": "Nueva Categoría"
}
```

*La plataforma acepta actualmente los valores: `telegram` y `whatsapp`. El sistema asignará el ícono, los colores y las físicas automáticamente.*

## 🚀 Despliegue (Deployment)

Este proyecto está optimizado para funcionar de manera nativa en **GitHub Pages** (o cualquier servidor estático como Vercel o Netlify) sin necesidad de configuraciones backend.

1. Haz un fork o clona este repositorio.
2. Sube tus archivos a la rama principal (`main`).
3. Ve a `Settings > Pages` en tu repositorio de GitHub y selecciona desplegar desde la rama principal.
4. El sistema usará `fetch` con *cache-busting* (`Date.now()`) para garantizar que tus usuarios siempre descarguen la versión más reciente de tus enlaces.

## 🛠️ Tecnologías Utilizadas

* **Estructura & Estilos:** HTML5, CSS3 Avanzado (Variables globales, Backdrop-filter, Animaciones CSS, CSS Grid/Flexbox).
* **Lógica & Datos:** Vanilla JavaScript (ES6+), Fetch API Asíncrona, JSON.
* **Librerías de Terceros:**
  * [Vanilla-Tilt.js](https://micku7zu.github.io/vanilla-tilt.js/) (Motor 3D).
  * [QRCode.js](https://davidshimjs.github.io/qrcodejs/) (Generación de QR en cliente).

---
*Desarrollado y mantenido por JJMex Systems.*
