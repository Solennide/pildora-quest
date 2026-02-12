# 💊 PÍLDORA QUEST - APP PARA IPHONE

## 🎮 ¿Qué es esto?

Una **Progressive Web App (PWA)** que funciona como una app nativa en tu iPhone sin necesidad de App Store. El juego funciona completamente sin conexión después de la instalación inicial.

---

## ⚡ INSTALACIÓN RÁPIDA (3 PASOS)

### Paso 1: Subir archivos a internet

Necesitas poner estos archivos en un servidor web. Las opciones MÁS FÁCILES son:

#### 🌟 OPCIÓN A: GitHub Pages (GRATIS - MÁS FÁCIL)

1. Ve a [github.com](https://github.com) y crea una cuenta
2. Crea un nuevo repositorio (botón verde "New")
3. Sube TODOS estos archivos:
   - index.html
   - pildora_quest.html
   - manifest.json
   - service-worker.js
   - icon-192.png
   - icon-512.png

4. Ve a: **Settings** → **Pages**
5. En "Source" selecciona: **main branch**
6. Copia la URL que aparece (ejemplo: `https://tuusuario.github.io/pildora-quest`)

#### 🌟 OPCIÓN B: Netlify Drop (GRATIS - SÚPER FÁCIL)

1. Ve a [drop.netlify.com](https://app.netlify.com/drop)
2. Arrastra la carpeta con TODOS los archivos
3. ¡Listo! Te da una URL al instante

### Paso 2: Abrir en iPhone

1. Abre **Safari** en tu iPhone (DEBE SER SAFARI, no Chrome)
2. Ve a la URL de tu servidor
3. El juego se cargará

### Paso 3: Instalar como App

1. Toca el botón **Compartir** (📤 en la parte inferior)
2. Desplázate y toca **"Añadir a la pantalla de inicio"**
3. Toca **"Añadir"**

**¡LISTO!** 🎉 Ahora tienes el icono en tu pantalla de inicio

---

## 📱 Características

✅ **Sin navegador visible** - Parece una app real
✅ **Funciona sin internet** - Después de la primera carga
✅ **Icono personalizado** - 💊 en tu pantalla
✅ **Pantalla completa** - Experiencia inmersiva
✅ **Controles táctiles** - Optimizados para iPhone
✅ **Sin App Store** - No necesitas pagar ni esperar aprobación

---

## 🎯 Cómo Jugar

### Controles
- **← →** Mover izquierda/derecha
- **↑** Saltar

### Objetivo
- 💊 **Píldoras** = +10 puntos cada una
- 🦠 **Virus** = -1 vida + reduces velocidad
- ❤️ **3 vidas** = Cuando pierdes las 3, Game Over

### Estrategia
Cada vez que un virus te toca, tu personaje se vuelve más lento, ¡así que evítalos a toda costa!

---

## 📁 Archivos Incluidos

```
📦 Píldora Quest
 ┣ 📄 index.html              (Juego principal)
 ┣ 📄 pildora_quest.html      (Copia del juego)
 ┣ 📄 manifest.json           (Configuración PWA)
 ┣ 📄 service-worker.js       (Modo offline)
 ┣ 🖼️ icon-192.png            (Icono 192x192)
 ┣ 🖼️ icon-512.png            (Icono 512x512)
 ┣ 📄 README.md               (Este archivo)
 ┗ 📄 INSTRUCCIONES_IPHONE.txt (Ayuda detallada)
```

---

## 🚨 Problemas Comunes

### "No puedo añadir a pantalla de inicio"
- ✅ Usa **Safari** (no Chrome, no Firefox)
- ✅ Verifica que la URL use **HTTPS** (GitHub Pages lo hace automático)
- ✅ Asegúrate que todos los archivos estén subidos

### "No funciona sin internet"
- ✅ La primera vez NECESITA internet para instalarse
- ✅ Después de cargar una vez, funcionará offline
- ✅ Cierra y abre la app completamente

### "Los controles no responden"
- ✅ Cierra la app completamente (desliza hacia arriba)
- ✅ Abre de nuevo desde el icono
- ✅ Asegúrate de tocar los botones en pantalla

### "El icono no aparece"
- ✅ Verifica que `icon-192.png` y `icon-512.png` estén en el servidor
- ✅ Borra la app y vuelve a instalarla
- ✅ Espera 10 segundos después de instalar

---

## 🆚 PWA vs App Nativa

### ¿Por qué PWA?

| PWA (Esta solución) | App Nativa (App Store) |
|---------------------|------------------------|
| ✅ GRATIS | ❌ $99/año |
| ✅ Sin Mac necesaria | ❌ Requiere Mac + Xcode |
| ✅ Instalación instantánea | ❌ Esperar 1-2 semanas revisión |
| ✅ Actualizaciones inmediatas | ❌ Cada update va a revisión |
| ✅ Funciona en cualquier móvil | ⚠️ Solo iOS |

### ¿Cuándo necesitas App Nativa?

Solo si necesitas:
- Notificaciones push avanzadas
- Acceso a sensores del teléfono
- Pagos in-app
- Aparecer en búsquedas de App Store

Para juegos simples como este, **PWA es perfecto**.

---

## 🔧 Para Desarrolladores

### Modificar el juego

Todos los archivos son HTML/CSS/JavaScript estándar:

- **Cambiar colores:** Edita las variables CSS en `<style>`
- **Ajustar dificultad:** Modifica `player.speed`, `virus.speed`
- **Nuevos niveles:** Agrega plataformas en `initPlatforms()`
- **Diferentes gráficos:** Edita las funciones `drawPlayer()`, `drawVirus()`

### Probar localmente

```bash
# Opción 1: Python
python3 -m http.server 8000

# Opción 2: Node.js
npx http-server

# Luego abre: http://localhost:8000
```

### Actualizar la app

1. Modifica los archivos
2. Sube al servidor
3. Cambia la versión en `service-worker.js`:
   ```javascript
   const CACHE_NAME = 'pildora-quest-v2'; // v1 → v2
   ```
4. Los usuarios verán la actualización al abrir la app

---

## 📚 Recursos Útiles

- [GitHub Pages Docs](https://pages.github.com/)
- [PWA Documentation](https://web.dev/progressive-web-apps/)
- [Netlify Drop](https://app.netlify.com/drop)
- [Safari PWA Guide](https://developer.apple.com/documentation/webkit/safari_web_extensions)

---

## ❓ Preguntas Frecuentes

**P: ¿Funciona en Android?**  
R: ¡Sí! Pero Android tiene mejor soporte para PWAs (puede recibir notificaciones).

**P: ¿Puedo monetizarla?**  
R: Sí, puedes agregar AdSense o links de afiliados en el HTML.

**P: ¿Los datos se guardan?**  
R: Las puntuaciones se guardan en localStorage del navegador. Se borran si desinstalas la app.

**P: ¿Puedo distribuirla?**  
R: Sí, solo comparte el link. Cada persona la instala desde Safari.

**P: ¿Cuánto espacio ocupa?**  
R: ~100KB. Es súper ligera.

---

## 🎨 Personalización Rápida

### Cambiar colores del juego

Busca en `index.html` estas líneas y modifica:

```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); /* Color de fondo */
```

```javascript
ctx.fillStyle = '#4a90e2'; // Color del jugador
ctx.fillStyle = '#7cfc00'; // Color del virus
ctx.fillStyle = '#ff6b9d'; // Color de píldora
```

### Cambiar velocidad

```javascript
player.speed = 5;        // Velocidad del jugador (aumenta para más rápido)
virus.speed = 1.5;       // Velocidad de virus (aumenta para más difícil)
player.jumpPower = 15;   // Altura de salto (aumenta para saltar más alto)
```

---

## 🏆 Créditos

- Creado con HTML5 Canvas
- Diseñado para iPhone
- PWA optimizada para iOS 11.3+

---

## 📄 Licencia

Libre para usar, modificar y distribuir. Si creas algo genial con esto, ¡compártelo! 🚀

---

**¿Necesitas ayuda?** Lee `INSTRUCCIONES_IPHONE.txt` para guía detallada paso a paso.

¡Disfruta jugando! 🎮💊🦠
