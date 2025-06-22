# 📚 LearnMentor

**Author:** Alejandro Barrena Millán
**License:** MIT License (see `LICENSE` file - though for a single HTML, you can include it in the README)

![image](https://github.com/user-attachments/assets/bf909a6e-1ab0-488f-b36f-f550812b4ed0)


[Saltar a la Documentación en Español](#documentación-en-español)

## 🇬🇧 English Documentation

### Overview

The LearnMentor is a powerful, single-HTML-file web application designed to help users generate various types of questions from their Markdown-based syllabus or notes. It leverages Large Language Models (LLMs) via APIs like OpenRouter or Google Gemini to create intelligent and context-aware study materials.

Being a single HTML file, this application is extremely portable. You can run it directly in any modern web browser on a desktop, laptop, tablet, or even a smartphone without needing any server-side setup or complex installations!

### Features

*   **API Provider Choice:**
    *   Connects to **OpenRouter** (access to various free and paid models).
    *   Connects to **Google Gemini** (via REST API using your Google AI Studio API Key).
*   **Model Selection:**
    *   Dynamically loads and lists available models (prioritizing free models on OpenRouter).
    *   Allows users to select their preferred LLM.
*   **Markdown File Upload:**
    *   Upload one or more `.md` files containing your syllabus content.
    *   Select a specific file to generate questions from.
*   **Multiple Question Types:**
    *   **Development Questions:** Open-ended questions requiring detailed answers.
    *   **Single-Choice Tests:** Multiple-choice questions with one correct answer, options (A, B, C, D), and justification.
    *   **Fill-in-the-Blanks:** Text passages with missing words/phrases for the user to complete.
    *   **Multi-Choice Tests:** Multiple-choice questions where one or more options can be correct.
*   **Configurable Number of Questions:**
    *   Specify how many questions (1-10) to generate for individual types.
*   **Exam Mode:**
    *   Generate a mixed exam by specifying the number of questions for each type.
    *   The LLM attempts to create content best suited for each requested question format.
*   **Interactive Answering & Checking:**
    *   Input fields for development answers and fill-in-the-blanks.
    *   Radio buttons for single-choice tests and checkboxes for multi-choice tests.
    *   **AI-Powered Evaluation (for Development Questions):** Get feedback on your development answers, with the AI's explanation tailored to a selected education level.
    *   **Automated Checking (for Test & Fill-in-the-blanks):** Instant feedback with correct answers and justifications.
*   **Iterative Learning:**
    *   **"Re-Explain":** Ask the AI to provide a different explanation if the initial one isn't clear.
    *   **"Rebuttal" (for Development Questions):** Challenge the AI's evaluation if you believe your answer was correct, and get a re-evaluation.
    *   **"Generate More":** Request additional questions of the same type, with the AI trying to avoid repetition.
*   **Persistent Configuration:**
    *   API keys, selected model, education level, and number of questions are saved in browser `localStorage`.
*   **User-Friendly Interface:**
    *   Responsive design for various screen sizes.
    *   Loading indicators and toast notifications for a smooth experience.
*   **Portability:**
    *   Single HTML file – run it anywhere with a modern browser!

### How to Use

1.  **Download:**
    *   Simply download the `code (11).html` file (or whatever you've named it).
2.  **Open in Browser:**
    *   Open the HTML file directly in your web browser (e.g., Chrome, Firefox, Edge, Safari).
3.  **Configure API (First Time):**
    *   The "⚙️ API Configuration and Preferences" section will likely be open.
    *   **Select API Provider:** Choose "OpenRouter" or "Google Gemini".
    *   **Enter API Key:**
        *   For OpenRouter: Paste your OpenRouter API Key.
        *   For Google Gemini: Paste your Google AI Studio API Key.
    *   **Load Models:** The application will attempt to load available models. You can click "🔄 Reload Models" if needed.
    *   **Select Model:** Choose an LLM from the dropdown. Free models from OpenRouter are prioritized.
    *   **Education Level:** Select the target education level for explanations.
    *   **Number of Questions:** Set the default number of questions to generate (1-10).
    *   **Save Configuration:** Click "💾 Save Configuration". Your API key will be stored locally in your browser.
4.  **Upload Markdown File(s):**
    *   Click "📤 Select .md files" and choose the Markdown file(s) containing your syllabus.
    *   The uploaded files will be listed.
5.  **Select a File:**
    *   Click on a file name from the list to select it. This will make it the active document for question generation.
6.  **Generate Questions:**
    *   Once a file is selected, buttons for different question types will appear:
        *   "🧠 P. Development"
        *   "📝 Test (Op. Única)" (Single-Choice Test)
        *   "🧩 Completar Texto" (Fill-in-the-Blanks)
        *   "☑️ Test (Op. Múltiple)" (Multi-Choice Test)
        *   "🎓 Generar Examen Mixto" (Generate Mixed Exam)
    *   Click the desired button. The AI will process your content and generate questions.
    *   For "Generate Mixed Exam", a configuration section will appear to specify the number of questions per type.
7.  **Answer and Check:**
    *   Answer the generated questions.
    *   Click the "📝 Check..." button below each question to see the evaluation or correct answers.
8.  **Interact Further:**
    *   Use "🗘 Explain Again" or "🗣️ Rebut" (for development questions) if needed.
    *   Click "🔄 Generate More of the Same Type" to get additional questions for the currently selected file and question type.

### Technical Details

*   **Frontend:** HTML, CSS, JavaScript (Vanilla JS).
*   **Markdown Parsing:** Uses the `marked.min.js` library for rendering Markdown in explanations.
*   **API Calls:** Uses the `fetch` API to communicate with OpenRouter or Google Gemini endpoints.
*   **No Backend Required:** All logic runs client-side in the browser.

### License

This project is licensed under the MIT License.
```
MIT License

Copyright (c) 2024 Alejandro Barrena Millán

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

```


---

## <a name="documentación-en-español"></a>🇪🇸 Documentación en Español

### Descripción General

El LearnMentor es una potente aplicación web, contenida en un único archivo HTML, diseñada para ayudar a los usuarios a generar varios tipos de preguntas a partir de sus temarios o apuntes basados en Markdown. Utiliza Modelos de Lenguaje Grandes (LLMs) a través de APIs como OpenRouter o Google Gemini para crear materiales de estudio inteligentes y contextualmente relevantes.

Al ser un único archivo HTML, esta aplicación es extremadamente portátil. ¡Puedes ejecutarla directamente en cualquier navegador web moderno en un ordenador de escritorio, portátil, tableta o incluso en un smartphone sin necesidad de configuración del lado del servidor o instalaciones complejas!

### Características

*   **Elección de Proveedor de API:**
    *   Se conecta a **OpenRouter** (acceso a varios modelos gratuitos y de pago).
    *   Se conecta a **Google Gemini** (a través de API REST usando tu Clave API de Google AI Studio).
*   **Selección de Modelo:**
    *   Carga y lista dinámicamente los modelos disponibles (priorizando modelos gratuitos en OpenRouter).
    *   Permite a los usuarios seleccionar su LLM preferido.
*   **Carga de Archivos Markdown:**
    *   Sube uno o más archivos `.md` que contengan el contenido de tu temario.
    *   Selecciona un archivo específico para generar preguntas a partir de él.
*   **Múltiples Tipos de Preguntas:**
    *   **Preguntas de Desarrollo:** Preguntas abiertas que requieren respuestas detalladas.
    *   **Tests de Opción Única:** Preguntas de opción múltiple con una única respuesta correcta, opciones (A, B, C, D) y justificación.
    *   **Completar Texto (Rellenar Huecos):** Pasajes de texto con palabras/frases faltantes para que el usuario las complete.
    *   **Tests de Opción Múltiple:** Preguntas de opción múltiple donde una o más opciones pueden ser correctas.
*   **Número Configurable de Preguntas:**
    *   Especifica cuántas preguntas (1-10) generar para tipos individuales.
*   **Modo Examen:**
    *   Genera un examen mixto especificando el número de preguntas para cada tipo.
    *   El LLM intenta crear contenido que se adapte mejor a cada formato de pregunta solicitado.
*   **Respuesta y Comprobación Interactivas:**
    *   Campos de entrada para respuestas de desarrollo y para rellenar huecos.
    *   Botones de radio para tests de opción única y casillas de verificación para tests de opción múltiple.
    *   **Evaluación Potenciada por IA (para Preguntas de Desarrollo):** Obtén retroalimentación sobre tus respuestas de desarrollo, con la explicación de la IA adaptada a un nivel educativo seleccionado.
    *   **Comprobación Automatizada (para Tests y Rellenar Huecos):** Retroalimentación instantánea con respuestas correctas y justificaciones.
*   **Aprendizaje Iterativo:**
    *   **"Re-Explicar":** Pide a la IA que proporcione una explicación diferente si la inicial no está clara.
    *   **"Rebatir" (para Preguntas de Desarrollo):** Desafía la evaluación de la IA si crees que tu respuesta era correcta y obtén una reevaluación.
    *   **"Generar Más":** Solicita preguntas adicionales del mismo tipo, con la IA intentando evitar la repetición.
*   **Configuración Persistente:**
    *   Las claves API, el modelo seleccionado, el nivel educativo y el número de preguntas se guardan en el `localStorage` del navegador.
*   **Interfaz Amigable:**
    *   Diseño responsivo para varios tamaños de pantalla.
    *   Indicadores de carga y notificaciones "toast" para una experiencia fluida.
*   **Portabilidad:**
    *   ¡Archivo HTML único – ejecútalo en cualquier lugar con un navegador moderno!

### Cómo Usar

1.  **Descargar:**
    *   Simplemente descarga el archivo `code (11).html` (o como lo hayas nombrado).
2.  **Abrir en el Navegador:**
    *   Abre el archivo HTML directamente en tu navegador web (ej. Chrome, Firefox, Edge, Safari).
3.  **Configurar API (Primera Vez):**
    *   La sección "⚙️ Configuración de API y Preferencias" probablemente estará abierta.
    *   **Selecciona Proveedor de API:** Elige "OpenRouter" o "Google Gemini".
    *   **Introduce Clave API:**
        *   Para OpenRouter: Pega tu Clave API de OpenRouter.
        *   Para Google Gemini: Pega tu Clave API de Google AI Studio.
    *   **Cargar Modelos:** La aplicación intentará cargar los modelos disponibles. Puedes hacer clic en "🔄 Recargar Modelos" si es necesario.
    *   **Selecciona Modelo:** Elige un LLM del desplegable. Los modelos gratuitos de OpenRouter se priorizan.
    *   **Nivel Educativo:** Selecciona el nivel educativo objetivo para las explicaciones.
    *   **Número de Preguntas:** Establece el número predeterminado de preguntas a generar (1-10).
    *   **Guardar Configuración:** Haz clic en "💾 Guardar Configuración". Tu clave API se almacenará localmente en tu navegador.
4.  **Subir Archivo(s) Markdown:**
    *   Haz clic en "📤 Seleccionar archivos .md" y elige el/los archivo(s) Markdown que contengan tu temario.
    *   Los archivos subidos se listarán.
5.  **Seleccionar un Archivo:**
    *   Haz clic en el nombre de un archivo de la lista para seleccionarlo. Esto lo convertirá en el documento activo para la generación de preguntas.
6.  **Generar Preguntas:**
    *   Una vez seleccionado un archivo, aparecerán botones para diferentes tipos de preguntas:
        *   "🧠 P. Desarrollo"
        *   "📝 Test (Op. Única)"
        *   "🧩 Completar Texto"
        *   "☑️ Test (Op. Múltiple)"
        *   "🎓 Generar Examen Mixto"
    *   Haz clic en el botón deseado. La IA procesará tu contenido y generará preguntas.
    *   Para "Generar Examen Mixto", aparecerá una sección de configuración para especificar el número de preguntas por tipo.
7.  **Responder y Comprobar:**
    *   Responde a las preguntas generadas.
    *   Haz clic en el botón "📝 Comprobar..." debajo de cada pregunta para ver la evaluación o las respuestas correctas.
8.  **Interactuar Más:**
    *   Usa "🗘 Explicar otra vez" o "🗣️ Rebatir" (para preguntas de desarrollo) si es necesario.
    *   Haz clic en "🔄 Generar Más del Mismo Tipo" para obtener preguntas adicionales para el archivo y tipo de pregunta actualmente seleccionados.

### Detalles Técnicos

*   **Frontend:** HTML, CSS, JavaScript (Vanilla JS).
*   **Análisis de Markdown:** Usa la biblioteca `marked.min.js` para renderizar Markdown en las explicaciones.
*   **Llamadas API:** Usa la API `fetch` para comunicarse con los endpoints de OpenRouter o Google Gemini.
*   **No Requiere Backend:** Toda la lógica se ejecuta del lado del cliente en el navegador.

### Licencia

Este proyecto está licenciado bajo la Licencia MIT. (Ver la sección de licencia en inglés para el texto completo).

---
**Desarrollado por Alejandro Barrena Millán**

