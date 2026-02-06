# 👁️ RobotFace: Ojos Digitales Reactivos

> Una interfaz gráfica reactiva que utiliza visión artificial para simular "ojos digitales" que siguen el movimiento del rostro del usuario en tiempo real.

![Vista Previa del Funcionamiento](https://github.com/AcxelCalle/RobotFace/blob/main/demo.GIF)

## 📖 Sobre el Proyecto

Soy estudiante de Física de último año en la **UNMSM** explorando el mundo de la Inteligencia Artificial y la Ingeniería de Software.

Este proyecto nació como un reto personal para entender los desafíos profundos de la **programación concurrente** y los sistemas en tiempo real. El objetivo principal fue resolver el problema del "congelamiento de UI" que ocurre cuando se intenta procesar video pesado y animar una interfaz gráfica en el mismo hilo de ejecución.

La solución implementada separa la lógica en una arquitectura de responsabilidades segregadas:

1.  **Frontend Asíncrono (Flet):** Una ventana corriendo en un bucle `asyncio` que se encarga únicamente de renderizar la animación ligera de los ojos basándose en coordenadas recibidas.
2.  **Backend de Visión (Threading/Nativo):** Un hilo independiente que maneja la cámara, procesa la malla facial (MediaPipe) y gestiona su propia ventana nativa de diagnóstico (OpenCV).

## 🛠️ Stack Tecnológico

* **Lenguaje Principal:** Python 3.x
* **Interfaz Gráfica (UI):** [Flet](https://flet.dev/) (Framework basado en Flutter para Python).
* **Visión Artificial:** OpenCV, MediaPipe.
* **Seguridad/Interacción:** Face_recognition, Pyttsx3 (Text-to-Speech).
* **Ingeniería:** Uso avanzado de `asyncio` y `threading` para la gestión de concurrencia.

## ⚙️ Instalación y Uso

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/AcxelCalle/RobotFace.git](https://github.com/AcxelCalle/RobotFace.git)
    cd RobotFace
    ```

2.  **Instalar dependencias:**
    Es recomendable usar un entorno virtual.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Ejecutar el sistema:**
    ```bash
    python RobotFace.py
    ```
    *Se abrirán dos ventanas: la interfaz de los ojos (Flet) y la ventana de diagnóstico de la cámara (OpenCV).*

## 🤝 Créditos y Reconocimiento

Este proyecto fue un ejercicio de integración y aprendizaje asistido.

* **AI Pair Programming:** Arquitectura y depuración de concurrencia asistida por modelos de IA (Gemini).
* **Inspiración Open Source:** La lógica visual base de los ojos fue adaptada de repositorios diseñados para matrices LED de Arduino (créditos a [AbdulsalamAbbod](https://github.com/AbdulsalamAbbod/Akno)), escalada para alta resolución en Flet.

---
