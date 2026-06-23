# Actividad: Modelos de IA en JavaScript con TensorFlow.js

**Alumno:** Duarte Natanael Obed

Esta actividad consiste en utilizar el **Modelo de Toxicidad** y el **Modelo Alerta Camión** en JavaScript, a partir del código del Capítulo 2 del libro *Learning TensorFlow.js* (Gant Laborde, O'Reilly).

Todos los proyectos usan **TensorFlow.js** cargado desde un CDN, por lo que no requieren instalación con npm: son páginas HTML que se ejecutan directamente en el navegador.

## Cómo ejecutar los proyectos

Conviene levantar un servidor local (abrir el HTML con doble clic puede bloquear la descarga de los modelos):

```bash
cd chapter2/simple
python -m http.server 8000
```

Luego abrir cada proyecto en el navegador y revisar la consola con `F12` → pestaña *Console*.

## Proyectos

Los proyectos están en la carpeta [`chapter2/simple`](chapter2/simple):

### 1. `simplest-example` — Ejemplo más simple
[Ver código](chapter2/simple/simplest-example/index.html) · http://localhost:8000/simplest-example/

Es el "Hola Mundo" de TensorFlow.js: solo carga la librería e imprime en consola la versión de TensorFlow.js que se está usando. Sirve para verificar que la librería se cargó correctamente.

### 2. `simple-toxicity` — Modelo de Toxicidad
[Ver código](chapter2/simple/simple-toxicity/index.html) · http://localhost:8000/simple-toxicity/

Usa el modelo **Toxicity** para analizar texto y detectar contenido tóxico u ofensivo. Clasifica tres frases de ejemplo (`'You are a poopy head!'`, `'I like turtles'`, `'Shut up!'`) y muestra en la consola, para cada categoría (insulto, amenaza, obscenidad, etc.), si el resultado supera el umbral de confianza definido (`0.5`).

### 3. `chapter-challenge` — Modelo Alerta Camión
[Ver código](chapter2/simple/chapter-challenge/index.html) · http://localhost:8000/chapter-challenge/

Usa el modelo **MobileNet** para clasificar una imagen (`truck.jpg`). Recorre las predicciones y, si detecta que la imagen contiene un camión (`"truck"`), muestra una alerta `"TRUCK DETECTED!"`. Las predicciones completas se imprimen en la consola.

---

*Basado en el repositorio [learn-tfjs](https://github.com/GantMan/learn-tfjs) de Gant Laborde.*
