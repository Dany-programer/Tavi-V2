# Laboratorio EduPlay – Aprende Jugando (TAVI)

**Laboratorio EduPlay – Aprende Jugando (TAVI)** es una plataforma educativa que utiliza IA para crear experiencias de aprendizaje interactivas y personalizadas, ayudando a los usuarios a descubrir su estilo de aprendizaje y a explorar conocimientos de forma gamificada.

## Características Principales:

1.  **Descubre Tu Estilo de Aprendizaje (Test VARK):**
    *   La aplicación incluye un test VARK (Visual, Auditivo, Lectoescritor, Kinestésico) que ayuda a los usuarios a identificar sus preferencias de aprendizaje.
    *   Comprender el estilo individual permite a los usuarios optimizar sus métodos de estudio y mejorar su rendimiento.

2.  **Juega y Aprende (Experiencias Interactivas Impulsadas por IA):**
    *   **Quizzes Interactivos:** Genera quizzes personalizados sobre una amplia variedad de temas y niveles de dificultad, proporcionando retroalimentación instantánea.
    *   **Recursos de Lectoescritura:** Crea diversos materiales textuales como resúmenes, explicaciones detalladas, historias educativas, e ideas para planes de clase, adaptados al tema y público objetivo.
    *   **Experiencias Kinestésicas:** Diseña y genera juegos HTML5 y simuladores interactivos (ej. juegos de memoria, quizzes, puzzles) para un aprendizaje práctico.
    *   **Herramientas Auditivas:** Convierte texto a voz con ajustes de tono y velocidad, y genera guiones creativos para podcasts, radionovelas o audioguías.
    *   **Contenido Visual:** Genera imágenes a partir de texto, diagramas (mapas mentales, de flujo), y datos para gráficos (barras, líneas, circular) para facilitar la comprensión visual de la información.

3.  **Desafío Diario:**
    *   Ofrece un quiz diario de conocimiento general para mantener la mente activa y fomentar el aprendizaje continuo.

4.  **Mis Resultados:**
    *   Un espacio dedicado para que los usuarios revisen sus estadísticas de progreso, puntuaciones en quizzes y tendencias de aprendizaje a lo largo del tiempo.

5.  **Gestión de Perfil y Configuración:**
    *   Permite a los usuarios gestionar la información de su cuenta.
    *   Sección de configuración para futuras personalizaciones de la aplicación.

## Stack Tecnológico Detallado:

Aquí se describe la tecnología utilizada en la aplicación, dónde se integra, por qué se eligió y los beneficios que aporta.

### Frontend

*   **Framework: Next.js (con App Router)**
    *   *Integración:* Es el framework principal sobre el que se construye toda la aplicación (estructura de carpetas en `src/app`, enrutamiento, etc.).
    *   *Por qué:* Ofrece renderizado del lado del servidor (SSR) y generación de sitios estáticos (SSG) para optimizar el SEO y el rendimiento inicial. El App Router moderniza el enrutamiento y permite el uso de Server Components.
    *   *Beneficios:* Excelente rendimiento, optimización para SEO, estructura de proyecto clara, enrutamiento basado en archivos, optimización automática de imágenes y una gran experiencia de desarrollo. Los Server Components ayudan a reducir el JavaScript enviado al cliente.

*   **Lenguaje: TypeScript**
    *   *Integración:* Utilizado en todo el código base, tanto para el frontend (archivos `.tsx`, `.ts` en `src/`) como para los flujos de IA con Genkit.
    *   *Por qué:* Añade tipado estático a JavaScript, lo que ayuda a prevenir errores comunes en tiempo de desarrollo.
    *   *Beneficios:* Mayor robustez y mantenibilidad del código, detección temprana de errores, mejor autocompletado y refactorización en los editores de código.

*   **Biblioteca de UI: React**
    *   *Integración:* Es la biblioteca fundamental para construir la interfaz de usuario dentro de Next.js. Todos los componentes visuales son componentes React.
    *   *Por qué:* Permite la creación de interfaces de usuario interactivas y reutilizables a través de un modelo basado en componentes.
    *   *Beneficios:* Componentización que facilita la reutilización y organización del código, un vasto ecosistema de bibliotecas y herramientas, y un eficiente manejo del DOM virtual.

*   **Componentes de UI: ShadCN UI**
    *   *Integración:* Utilizado para la mayoría de los elementos de UI pre-construidos como botones, tarjetas, modales, formularios, etc. Los componentes se encuentran en `src/components/ui` y se configuran mediante `components.json`.
    *   *Por qué:* Proporciona una colección de componentes accesibles, personalizables y estéticamente agradables, construidos sobre Radix UI (para la lógica y accesibilidad) y Tailwind CSS (para el estilo). No es una biblioteca tradicional, sino que los componentes se integran directamente en el proyecto.
    *   *Beneficios:* Diseño moderno y limpio, alta accesibilidad, total personalización al tener el código fuente de los componentes, excelente integración con Tailwind CSS.

*   **Estilos: Tailwind CSS**
    *   *Integración:* Es el framework CSS principal utilizado para estilizar todos los componentes y la aplicación en general. Su configuración se encuentra en `tailwind.config.ts` y los estilos base y variables de tema en `src/app/globals.css`.
    *   *Por qué:* Es un framework CSS "utility-first" que permite construir diseños complejos rápidamente aplicando clases directamente en el HTML, sin necesidad de escribir CSS personalizado extensivo.
    *   *Beneficios:* Desarrollo rápido de UI, consistencia en el diseño, alta personalización, optimización del tamaño del CSS final al purgar clases no utilizadas.

*   **Gráficos: Recharts**
    *   *Integración:* Se utiliza en la página "Mis Resultados" (`src/app/(app)/results/page.tsx`) y en el componente `OutputDisplay` de la sección "Visual" para renderizar gráficos de barras, líneas y circulares.
    *   *Por qué:* Es una biblioteca de gráficos para React componible y declarativa, fácil de integrar.
    *   *Beneficios:* Facilidad para crear gráficos dinámicos y personalizados dentro de React, buena variedad de tipos de gráficos listos para usar.

*   **Formularios: React Hook Form & Zod**
    *   *Integración:* `react-hook-form` gestiona el estado y la validación de los formularios en varias secciones (Quizzes, Generador de Texto, Simulador, Visual). `zod` se utiliza para definir los esquemas de validación, tanto en el cliente (a través de `@hookform/resolvers`) como en las Server Actions para la validación en el backend.
    *   *Por qué:* `react-hook-form` es conocido por su rendimiento y facilidad de uso. `zod` ofrece una validación de esquemas potente con una excelente inferencia de tipos, lo que complementa bien a TypeScript.
    *   *Beneficios:* Manejo eficiente del estado de los formularios, validación de datos robusta y clara, mejora la experiencia del usuario al proporcionar mensajes de error precisos.

*   **Gestión de Estado (Cliente):** React Context & Hooks (`useState`, `useEffect`, `useCallback`)
    *   *Integración:* Para el estado local de los componentes y para la gestión de estados compartidos simples, como el proveedor del estado de la barra lateral (`SidebarProvider`).
    *   *Por qué:* Son las herramientas nativas proporcionadas por React para la gestión de estado, adecuadas para muchos casos de uso sin necesidad de bibliotecas externas más complejas.
    *   *Beneficios:* Simplicidad para estados locales y compartidos no complejos, sin dependencias adicionales.

### Backend / Funcionalidad de Inteligencia Artificial

*   **Framework de IA: Genkit (Google)**
    *   *Integración:* Es el núcleo de la funcionalidad de IA. Todos los flujos de generación de contenido (quizzes, simuladores, texto, guiones, contenido visual) están definidos como flujos de Genkit en la carpeta `src/ai/flows/`. La inicialización y configuración base de Genkit se encuentra en `src/ai/genkit.ts`.
    *   *Por qué:* Proporciona un entorno estructurado y herramientas para construir, desplegar y monitorizar aplicaciones de IA robustas y escalables, especialmente con modelos de Google.
    *   *Beneficios:* Organización clara de los flujos de IA, gestión de prompts, integración con Firebase para observabilidad (si se configura), facilita la interacción con diversos modelos de IA.

*   **Modelo de IA (Lenguaje): Gemini (a través de Genkit y `@genkit-ai/googleai`)**
    *   *Integración:* Es el modelo de lenguaje grande (LLM) utilizado por los flujos de Genkit para tareas como generar preguntas de quiz, código HTML para simuladores, guiones de audio, recursos textuales y lógica para contenido visual. El modelo por defecto (`googleai/gemini-2.0-flash`) se especifica en `src/ai/genkit.ts`.
    *   *Por qué:* Es un modelo multimodal potente y versátil desarrollado por Google, capaz de entender y generar texto, código, y más.
    *   *Beneficios:* Altas capacidades de generación de texto creativo y técnico, seguimiento de instrucciones complejas, razonamiento.

*   **Modelo de IA (Imágenes): Gemini 2.0 Flash Experimental (`googleai/gemini-2.0-flash-exp`) (a través de Genkit)**
    *   *Integración:* Utilizado específicamente dentro del flujo `generate-visual-content-flow.ts` para la tarea de generación de imágenes a partir de prompts de texto.
    *   *Por qué:* Es el modelo actualmente recomendado y habilitado dentro de Genkit para la generación de imágenes con la API de Gemini.
    *   *Beneficios:* Permite la creación de contenido visual original directamente desde descripciones textuales.

### Otras Tecnologías y Herramientas

*   **Iconos: Lucide React**
    *   *Integración:* Se utiliza para la mayoría de los iconos presentes en la interfaz de usuario (navegación, botones, tarjetas, etc.).
    *   *Por qué:* Es una biblioteca de iconos SVG ligera, bien diseñada, altamente personalizable y optimizada para React.
    *   *Beneficios:* Proporciona iconos consistentes, de alta calidad y fáciles de integrar, con un impacto mínimo en el rendimiento.

*   **Variables de Entorno: Dotenv**
    *   *Integración:* Utilizado en `src/ai/dev.ts` para cargar variables de entorno (como claves API para servicios de IA) durante el desarrollo local de los flujos de Genkit.
    *   *Por qué:* Es una forma estándar de gestionar secretos y configuraciones específicas del entorno fuera del código fuente.
    *   *Beneficios:* Mejora la seguridad al no incrustar información sensible en el código, permite diferentes configuraciones para desarrollo, staging y producción.

## Primeros Pasos:

Para comenzar a explorar la aplicación, navega a la página de inicio y considera realizar el Test VARK para personalizar tu experiencia. Luego, explora las diversas herramientas en la sección "Juega y Aprende".
```