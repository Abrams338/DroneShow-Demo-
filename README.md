<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# 🚁 DroneShow Visualizer

Una aplicación web moderna para visualizar y diseñar shows de drones con inteligencia artificial. Genera imágenes y videos impresionantes de espectáculos de drones personalizados usando Google AI (Gemini, Imagen 4.0 y Veo 3.1).

![Version](https://img.shields.io/badge/version-0.0.0-blue.svg)
![React](https://img.shields.io/badge/React-19.2.0-61dafb.svg)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8.2-3178c6.svg)
![Vite](https://img.shields.io/badge/Vite-6.2.0-646cff.svg)

**[Ver App en AI Studio](https://ai.studio/apps/drive/1lzYbyKgKFe0yf2rDWkwvk9zJZLgqSVby)**

---

## ✨ Características Principales

### 🎨 Generación con IA
- **Generación de Imágenes**: Crea visualizaciones fotorrealistas de shows de drones con Imagen 4.0
- **Edición Inteligente**: Modifica las imágenes generadas con prompts en lenguaje natural usando Gemini 2.5 Flash Image
- **Generación de Videos**: Anima tus imágenes con Veo 3.1 Fast para crear videos dinámicos
- **Análisis de Contexto**: Sube imágenes de referencia del lugar y la IA las analiza para generar visualizaciones más precisas

### 🎯 Gestión de Proyectos
- **Guardar Proyectos**: Almacena tus visualizaciones favoritas localmente
- **Galería Visual**: Explora todos tus proyectos guardados con una interfaz elegante
- **Filtrado por Tipo**: Organiza proyectos por tipo de evento (Bodas, Festivales, Corporativos, etc.)
- **Detalles Completos**: Visualiza toda la información de cada proyecto guardado

### 💎 Experiencia de Usuario Premium
- **Loader Temático**: Animación de drones orbitando durante la carga
- **Preview de Imágenes**: Vista previa de imágenes de referencia con opciones de editar/eliminar
- **Efecto Reveal**: Animación dramática al revelar visualizaciones generadas
- **Notificaciones Toast**: Feedback elegante para todas las acciones
- **Badges de Evento**: Identificadores visuales con iconos y colores por tipo de evento
- **Animaciones Stagger**: Las tarjetas aparecen progresivamente en la galería
- **Diseño Responsive**: Optimizado para desktop, tablet y móvil

---

## 🛠️ Tecnologías

- **Frontend**: React 19.2 + TypeScript
- **Build Tool**: Vite 6.2
- **Estilos**: TailwindCSS (vía CDN)
- **IA**: Google GenAI SDK
  - Gemini 2.5 Flash (descripción de imágenes)
  - Imagen 4.0 (generación de imágenes)
  - Gemini 2.5 Flash Image (edición de imágenes)
  - Veo 3.1 Fast (generación de videos)

---

## 🚀 Instalación y Configuración

### Prerrequisitos

- **Node.js** (v18 o superior)
- **Cuenta de Google Cloud** con facturación habilitada
- **API Key de Google AI**

### 1. Clonar el Repositorio

```bash
git clone https://github.com/jesusq18/DroneShow-Demo.git
cd DroneShow-Demo
```

### 2. Instalar Dependencias

```bash
npm install
```

### 3. Configurar la API Key

#### Obtener la API Key de Google AI

1. Ve a [Google AI Studio](https://aistudio.google.com/apikey)
2. Crea una nueva API Key o usa una existente
3. **Habilita los siguientes servicios en Google Cloud Console**:
   - Gemini API: https://console.cloud.google.com/apis/library/generativelanguage.googleapis.com
   - Imagen API (generación de imágenes)
   - Veo API (generación de videos) - **Requiere facturación**

#### Configurar la Variable de Entorno

1. Copia el archivo de ejemplo:
   ```bash
   cp .env.example .env
   ```

2. Edita el archivo `.env` y agrega tu API key:
   ```env
   VITE_API_KEY=tu_api_key_aqui
   ```

⚠️ **Importante**:
- El archivo `.env` está en `.gitignore` y **nunca se subirá a Git**
- Para generación de videos, necesitas **habilitar facturación** en Google Cloud
- Consulta los [precios de Google AI](https://ai.google.dev/gemini-api/docs/billing)

### 4. Ejecutar la Aplicación

```bash
npm run dev
```

La aplicación estará disponible en `http://localhost:5173`

---

## 📁 Estructura del Proyecto

```
DroneShow-Demo/
├── components/
│   ├── icons/
│   │   └── DroneIcon.tsx         # Icono de drone personalizado
│   ├── Loader.tsx                # Loader animado temático
│   └── Toast.tsx                 # Sistema de notificaciones
├── services/
│   └── geminiService.ts          # Integración con Google AI
├── App.tsx                       # Componente principal
├── types.ts                      # Definiciones de TypeScript
├── constants.ts                  # Constantes (tipos de eventos)
├── index.tsx                     # Punto de entrada
├── index.html                    # HTML base
├── vite.config.ts                # Configuración de Vite
├── tsconfig.json                 # Configuración de TypeScript
├── .env                          # Variables de entorno (NO en Git)
├── .env.example                  # Plantilla de variables de entorno
└── package.json                  # Dependencias del proyecto
```

---

## 🎨 Tipos de Eventos Soportados

La aplicación soporta los siguientes tipos de eventos con badges personalizados:

| Tipo | Icono | Color |
|------|-------|-------|
| Boda | 💍 | Rosa |
| Festival | 🎪 | Púrpura |
| Corporativo | 🏢 | Azul |
| Concierto | 🎵 | Rojo |
| Política | 🗳️ | Verde |
| Otro | 📋 | Gris |

---

## 🎬 Flujo de Uso

1. **Crear Proyecto**
   - Completa el formulario con detalles del cliente y evento
   - Opcionalmente sube una imagen de referencia del lugar
   - Especifica las figuras deseadas para el show

2. **Generar Visualización**
   - La IA genera una imagen fotorrealista del show de drones
   - Efecto de reveal dramático al mostrar el resultado

3. **Editar (Opcional)**
   - Usa prompts en lenguaje natural para modificar la imagen
   - Ejemplo: "Añade un filtro retro" o "Cambia las luces a tonos rojos"

4. **Generar Video (Opcional)**
   - Anima tu imagen para crear un video dinámico
   - Los drones se mueven y las luces parpadean de forma mágica

5. **Guardar Proyecto**
   - Guarda tu visualización en la galería local
   - Accede a ella en cualquier momento desde "Ver Proyectos"

---

## 🔧 Scripts Disponibles

```bash
# Desarrollo
npm run dev          # Inicia servidor de desarrollo

# Producción
npm run build        # Genera build de producción
npm run preview      # Vista previa del build

# Limpieza
rm -rf node_modules  # Elimina dependencias
rm -rf dist          # Elimina build
```

---

## 🌈 Mejoras Visuales Implementadas

### 1. Loader Temático de Drones
- Animación de drones orbitando en formación
- Efectos de estelas de luz
- Gradientes animados de fondo
- Puntos parpadeantes sincronizados

### 2. Preview de Imagen Subida
- Vista previa inmediata al cargar imagen
- Botones para editar/eliminar con overlay hover
- Bordes brillantes cyan
- Gestión automática de memoria

### 3. Efecto Reveal Dramático
- Desenfoque progresivo al mostrar imagen generada
- Efecto shimmer (brillo deslizante)
- Transiciones suaves de escala y opacidad
- Animación de entrada de 1 segundo

### 4. Sistema de Notificaciones Toast
- Diseño elegante con iconos según tipo
- Animación de entrada desde la derecha
- Barra de progreso animada
- Auto-cierre después de 4 segundos
- 3 tipos: Éxito, Error, Info

### 5. Galería Mejorada
- Badges coloridos por tipo de evento
- Iconos temáticos para cada categoría
- Animaciones stagger (aparición progresiva)
- Hover con elevación y sombras cyan
- Iconos informativos (ubicación, drones)
- Empty state elegante

---

## 📊 Modelos de IA Utilizados

| Modelo | Uso | Características |
|--------|-----|----------------|
| **Gemini 2.5 Flash** | Descripción de imágenes | Rápido, eficiente, multimodal |
| **Imagen 4.0** | Generación de imágenes | Alta calidad, fotorrealista, 16:9 |
| **Gemini 2.5 Flash Image** | Edición de imágenes | Edición basada en prompts |
| **Veo 3.1 Fast** | Generación de videos | 720p, animaciones fluidas |

---

## 💰 Costos y Facturación

- **Generación de Imágenes**: Incluido en cuota gratuita
- **Descripción y Edición**: Incluido en cuota gratuita
- **Generación de Videos**: **Requiere facturación habilitada**

Consulta los precios actualizados en: https://ai.google.dev/gemini-api/docs/billing

---

## 🔒 Seguridad

- ✅ API Key almacenada en `.env` (nunca en código)
- ✅ `.env` incluido en `.gitignore`
- ✅ Validación de tamaño de archivos (máx 4MB)
- ✅ Manejo seguro de errores
- ✅ Limpieza automática de URLs de objetos

---

## 🐛 Solución de Problemas

### Error: "API_KEY environment variable not set"
- Verifica que el archivo `.env` existe
- Asegúrate de que la variable se llama `VITE_API_KEY`
- Reinicia el servidor de desarrollo después de crear/modificar `.env`

### Error al generar videos
- Verifica que la facturación está habilitada en Google Cloud
- Asegúrate de que la API de Veo está habilitada
- Revisa los permisos de tu API key

### La imagen no se genera correctamente
- Verifica que la API de Imagen 4.0 está habilitada
- Revisa que el prompt tenga sentido y sea descriptivo
- Intenta regenerar con un prompt diferente

---

## 🤝 Contribuir

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

---

## 📝 Licencia

Este proyecto es privado y está diseñado como demo interna.

---

## 👨‍💻 Autor

**Jesus Quintero**
- GitHub: [@jesusq18](https://github.com/jesusq18)

---

## 🙏 Agradecimientos

- Google AI por las APIs de Gemini, Imagen y Veo
- Comunidad de React y TypeScript
- TailwindCSS por el sistema de utilidades

---

<div align="center">
  <p>Hecho con ❤️ y 🤖 IA</p>
  <p><strong>DroneShow Visualizer</strong> - Versión Demo Interna</p>
</div>
