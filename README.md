# FlatTwin Landing Page

Landing page minimalista y animada para el pre-lanzamiento de **FlatTwin**, la aplicación para encontrar el compañero de piso ideal ("Tinder para roommates").

## 📋 Descripción General
Esta landing page está diseñada como una experiencia de usuario fluida y progresiva (SPA) que utiliza Vanilla JS, CSS3 y HTML5 para maximizar la compatibilidad y velocidad de carga. Su objetivo principal es captar "leads" (interesados) antes del lanzamiento oficial.

## 🏗️ Estructura del Proyecto
- **index.html**: Archivo principal que contiene la estructura, estilos y lógica de navegación.
- **index_v2.html**: Versión optimizada con animaciones mejoradas y flujos de interacción pulidos.
- **CNAME**: Configuración de dominio personalizado.

## 🚀 Flujo de Usuario (Navegación)
La aplicación se divide en 4 pantallas principales gestionadas mediante la función `goToScreen(num)`:
1.  **Screen 1 (Hero)**: Propuesta de valor inicial y CTA "Quiero entrar".
2.  **Screen 2 (Narrativa)**: Tres frases clave con efecto "typing" que aparecen progresivamente. Transición automática a la siguiente pantalla.
3.  **Screen 3 (Interacción Chat)**: Simulación de una interfaz de chat móvil. El bot ofrece la entrada y el usuario debe confirmar con un mensaje interactivo ("Sí, quiero entrar").
4.  **Screen 4 (Conversión)**: Formulario de captura de datos (Nombre, Email, Teléfono).

## ⚙️ Integración Técnica
### Backend & API
Los datos del formulario se envían mediante una petición `fetch` (POST) a:
`https://flattwinbackend-production.up.railway.app/api/v1/leads`

### Seguridad (CORS)
El backend debe tener habilitado CORS para permitir peticiones desde el dominio donde esté alojada esta landing. Para pruebas locales, se recomienda permitir `http://localhost:8000`.

### Estética y Diseño
- **Tipografía**: 'Inter' (Google Fonts).
- **Colores**: Gradientes de azul profundo (#1a2744 a #4774D0) con estética "Glassmorphism" (transparencias y desenfoque de fondo).
- **Efectos**: Capa de ruido (noise) para textura premium y sombras multi-capa para profundidad.

## 🤖 Notas para Desarrolladores / IAs
- **Animaciones**: Se basan en clases CSS (`visible`, `animate-down`, `typing`) y funciones `async/await` en JS para el control del tiempo.
- **Responsividad**: Utiliza `clamp()` y `viewport units` para asegurar que el texto sea legible tanto en móvil como en escritorio.
- **Validación**: El formulario requiere al menos Email o Teléfono para ser procesado.

---
*Mantenido por el equipo de FlatTwin.*