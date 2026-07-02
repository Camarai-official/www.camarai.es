# Guía y Skill: Creación y Optimización de llms.txt para Inteligencia Artificial

Este archivo contiene las instrucciones y la batería de preguntas para que cualquier agente de IA pueda guiar la creación y optimización de un fichero `llms.txt` y `llms-full.txt` en este proyecto, basado en la guía oficial de **Acumbamail**.

---

## 1. Guía de Referencia (Resumen de la URL: https://acumbamail.com/blog/llms-txt/)

El archivo `llms.txt` es una propuesta de fichero estándar en formato Markdown que se ubica en la raíz del dominio (ej. `tuweb.com/llms.txt`). Su propósito es ofrecer a los modelos de lenguaje (LLMs) y rastreadores de IA una guía rápida, limpia y contextualizada de la web, eliminando el ruido visual y de código (scripts, menús de navegación, estilos, etc.).

### Directivas Principales (Anatomía del fichero)
Las reglas se pueden definir de forma global (`LLM: *`) o para agentes de IA específicos (ej. `LLM: ChatGPT`, `LLM: Claude`).
- **`$trainingAllowed`**: Controla si el contenido puede ser utilizado para entrenar modelos de IA. Valores: `true` / `false`.
- **`$chatAllowed`**: Determina si el contenido puede ser utilizado para generar respuestas en chats. Valores: `true` / `false`.
- **`$embedded`**: Define si el contenido puede ser embebido en respuestas de IA. Valores: `allowed` / `disallowed`.
- **`$responseLength`**: Limita la longitud máxima (en palabras) de las respuestas generadas a partir del contenido de tu sitio.
- **`$embargo`**: Establece un período durante el cual el contenido nuevo o reciente no puede ser utilizado.
- **`Path`**: Especifica rutas o secciones concretas a las que aplicar las reglas (ej. restringir secciones de pago o paneles de administración).

---

## 2. Batería de Preguntas para Recopilar Información (Interactive Verification Battery)

Para que el agente de IA configure correctamente el fichero `llms.txt` de acuerdo a tus necesidades, debe realizarte las siguientes preguntas para rellenar la máxima cantidad de información posible y verificar que todos los puntos estén cubiertos:

### A. Información de Marca y Propósito General
1. **¿Cuál es el nombre oficial de la marca o proyecto?** (Ej. *Camarai*)
2. **¿Cuál es la propuesta de valor principal de la web?** (Define en 1 o 2 oraciones qué hace el proyecto y para quién va dirigido, esto irá en el bloque de resumen inicial del archivo).
3. **¿Cuál es la URL principal de la web?** (Ej. *https://camarai.es/*)

### B. Directivas de Acceso para la IA
4. **¿Deseas permitir que los modelos de IA se entrenen con el contenido de tu web?**
   - *Opción A:* Permitir entrenamiento (`$trainingAllowed: true`)
   - *Opción B:* Bloquear entrenamiento (`$trainingAllowed: false`)
5. **¿Deseas permitir que los asistentes de chat (como ChatGPT o Claude) respondan preguntas a los usuarios utilizando tu información?**
   - *Opción A:* Permitir respuestas (`$chatAllowed: true`)
   - *Opción B:* Bloquear respuestas (`$chatAllowed: false`)
6. **¿Quieres establecer un límite de palabras para las respuestas de la IA basadas en tu web?** (Ej. `$responseLength: 150`)
7. **¿Existen secciones de tu web que quieras bloquear completamente para la IA?** (Ej. `/admin`, `/privado`, `/premium`).
8. **¿Quieres aplicar reglas diferentes para IAs específicas?** (Ej. permitir que Claude use tu contenido para responder pero bloquear a ChatGPT).

### C. Catálogo de Páginas y Estructura
9. **¿Cuáles son las páginas y secciones más importantes que la IA debe conocer?** (Ej. Inicio, Servicios, Tarifas/Calculadora, Contacto, Política de Privacidad, Términos y Condiciones).
10. **Proporciona una breve descripción (de una línea) sobre el propósito de cada una de esas páginas.**
11. **¿Existe un archivo `sitemap.xml` activo en el proyecto?** (El agente debe leerlo para asegurarse de que no se olvida ninguna URL pública relevante).

### D. Contexto Técnico e Integración
12. **¿Qué tecnologías y frameworks se utilizan en este proyecto?** (Es útil detallarlo en la sección de arquitectura del `llms.txt` para que los agentes que lean el código sepan qué stack técnico están analizando).
13. **¿Es necesario crear un archivo complementario `llms-full.txt`?** (Recomendado si tienes documentación técnica extensa, artículos de blog completos o catálogos grandes de productos que la IA deba leer en su totalidad).
14. **¿Deseas añadir referencias al archivo `llms.txt` en el archivo `robots.txt`?** (Como comentario para facilitar su descubrimiento por parte de los rastreadores).

---

## 3. Workflow de Verificación del Agente de IA

El agente de IA que trabaje en esta web debe seguir los siguientes pasos para verificar que el archivo esté completo:

1. **Lectura de la estructura:** Comprobar que el archivo `llms.txt` empiece con un título `# [Nombre del Proyecto]` y un bloque de cita `> [Resumen del sitio]`.
2. **Revisión de directivas:** Confirmar que se han incluido las directivas de consentimiento (`$trainingAllowed`, `$chatAllowed`, etc.) en la parte superior.
3. **Verificación de Enlaces:** Comprobar que todos los enlaces a las páginas clave sean correctos, utilicen URLs absolutas y contengan descripciones explicativas claras.
4. **Mapeo de Rutas:** Asegurar que la estructura del proyecto esté documentada de forma legible en la sección de arquitectura.
