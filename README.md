# ☀️ SOLARIX PWA — Calculadora y Dimensionamiento Solar Fotovoltaico

**SOLARIX PWA** es una aplicación web progresiva (Progressive Web App) profesional diseñada para calcular y dimensionar instalaciones solares fotovoltaicas (Off-Grid y autónomas). Permite calcular consumo energético diario, número de paneles solares requeridos, capacidad del banco de baterías, potencia del inversor y amperaje del controlador de carga.

---

## 📱 Características Principales y PWA

- 🚀 **Instalable en Móviles y Escritorio**: Incluye un **botón "Instalar App"** en el encabezado para descargar la aplicación directamente a la pantalla de inicio de tu smartphone (Android / iOS) o como app de escritorio independiente.
- ⚡ **Funcionamiento Offline Completo**: Gracias al Service Worker (`sw.js`), la aplicación se almacena en caché localmente y funciona sin necesidad de conexión a internet.
- 📊 **Cálculos Automáticos en Tiempo Real**: Recalcula corriente, potencia y requerimientos solares al instante.
- 💾 **Historial de Proyectos**: Guarda múltiples diseños de instalaciones solares en `localStorage`.
- 🖨️ **Generación de Reportes PDF**: Exportación limpia para imprimir o guardar como informe PDF.

---

## 🛠️ Cómo Subir este Proyecto a GitHub y Activar GitHub Pages

Para publicar tu PWA y permitir que cualquier usuario la instale desde la web o un enlace en su móvil:

### 1. Inicializar el Repositorio e Subir a GitHub
```bash
git init
git add .
git commit -m "feat: Convert SOLARIX into a full-featured PWA with native install capability"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/SOLARIX_PWA.git
git push -u origin main
```

### 2. Activar GitHub Pages (HTTPS Gratuito y Requerido para PWA)
1. Ve a tu repositorio en GitHub: `https://github.com/TU_USUARIO/SOLARIX_PWA`.
2. Haz clic en **Settings** (Configuración) -> **Pages** (en el menú lateral izquierdo).
3. En **Source** (Fuente), selecciona la rama `main` (o `master`) y la carpeta `/ (root)`.
4. Haz clic en **Save** (Guardar).
5. En un par de minutos, GitHub te proporcionará una URL HTTPS similar a:
   `https://TU_USUARIO.github.io/SOLARIX_PWA/`

---

## 📲 Cómo Instalar SOLARIX en un Dispositivo Móvil

Una vez desplegada en GitHub Pages o cualquier servidor web HTTPS:

### En Android (Chrome / Edge / Samsung Internet / Brave)
1. Abre el enlace de la app en tu navegador móvil.
2. Haz clic en el botón amarillo **"⚡ Instalar App"** situado en la parte superior derecha de la aplicación.
3. Confirma la instalación en la ventana emergente que mostrará Chrome/Android.
4. ¡Listo! El icono de SOLARIX aparecerá en el menú de aplicaciones y pantalla de inicio de tu smartphone.

### En iPhone / iPad (iOS Safari)
1. Abre el enlace en el navegador **Safari**.
2. Toca el botón **Compartir** ⎋ (el icono de un cuadrado con una flecha hacia arriba).
3. Desplázate hacia abajo en la lista de opciones y selecciona **"Agregar a la pantalla de inicio"** ➕.
4. Presiona **Agregar**. La app se abrirá a pantalla completa sin barras del navegador.

---

## 📁 Estructura del Proyecto

```
SOLARIX_PWA/
├── index.html            # Archivo principal de la aplicación con UI moderna y PWA handler
├── SOLARIX_app.html      # Copia principal/alias compatible
├── manifest.json         # Manifiesto PWA (iconos, temas, nombre, modo standalone)
├── sw.js                 # Service Worker para almacenamiento en caché y offline mode
├── icons/                # Iconos PNG y SVG adaptativos (192x192, 512x512, maskable, apple-touch)
│   ├── favicon.svg
│   ├── favicon-64.png
│   ├── icon-192.png
│   ├── icon-512.png
│   ├── icon-maskable-192.png
│   ├── icon-maskable-512.png
│   └── apple-touch-icon.png
└── README.md             # Documentación del proyecto y guía de instalación
```

---

## 💻 Desarrollo Local y Pruebas

Para probar la PWA localmente antes de subir a GitHub:
Puedes usar cualquier servidor HTTP local (los Service Workers requieren `localhost` o `https://`):

```bash
# Opción 1: Python HTTP server
python -m http.server 8000

# Opción 2: Node npx serve
npx serve .
```

Abre `http://localhost:8000` en tu navegador para verificar el registro del Service Worker y la instalación de la PWA.
