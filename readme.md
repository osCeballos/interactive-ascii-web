# Interactive Webcam ASCII Filter (Web Port)

Este proyecto es una adaptación web (port) de una instalación interactiva diseñada originalmente por mí en **TouchDesigner**. 

El objetivo de este desarrollo fue trasladar la experiencia inmersiva del entorno de nodos a una web escalable, permitiendo que el filtro ASCII reaccione en tiempo real a la distancia de los dedos del usuario directamente en el navegador.

## 🧠 Tecnologías Clave

Este proyecto combina gráficos avanzados con visión por computadora en el cliente:

* **Google MediaPipe:** Utilizado para el *Hand Tracking* de alto rendimiento. Detecta los "landmarks" de la mano en tiempo real para calcular la distancia entre el pulgar y el índice sin necesidad de hardware externo (Kinect/Leap Motion).
* **Three.js (WebGL):** Motor de renderizado 3D.
* **GLSL (Shaders):** Lógica personalizada para la generación procedural de caracteres ASCII y gestión de texturas.
* **JavaScript (ES6+):** Lógica de control y gestión de estado.

## ✨ Características de la Interacción

1.  **Detección de Gestos con IA:** Gracias a **MediaPipe**, el sistema reconoce la mano del usuario instantáneamente.
2.  **Transición Suavizada:** Un shader personalizado mezcla el video original con la representación ASCII basándose en la proximidad de los dedos (Gesto de "Pellizco").
3.  **Persistencia de Estado (State Locking):** Si el usuario retira la mano del encuadre, el sistema "recuerda" el último valor del efecto, manteniendo el filtro activo sin resetearse bruscamente.


## 📄 Créditos y Contexto

**Concepto Original:** Diseñado en **TouchDesigner**.
**Implementación Web:** Código generado y optimizado con la asistencia de **Gemini (Google AI)** para portar la lógica de nodos a WebGL/JS.
**Mediapipe:**https://github.com/torinmb/mediapipe-touchdesigner 
---
*Este proyecto es de código abierto para fines educativos y experimentales.*