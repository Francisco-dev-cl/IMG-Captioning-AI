# AI Image Captioning Tool (BLIP & Gradio)

Este repositorio contiene una aplicación avanzada de **Visión por Computadora e Inteligencia Artificial Generativa** que analiza imágenes de forma automática y genera subtítulos o descripciones contextuales altamente precisas (*Image Captioning*). El proyecto implementa el modelo de Deep Learning **BLIP (Bootstrapping Language-Image Pre-training)** provisto por Hugging Face y despliega una interfaz web interactiva.

## 🎯 Características y Objetivos del Proyecto
*   **Inferencia de Deep Learning:** Implementación del modelo pre-entrenado `Salesforce/blip-image-captioning-base` para la descripción condicional e incondicional de imágenes.
*   **Procesamiento de Datos Multimodal:** Conversión y normalización de matrices numéricas (`NumPy arrays`) e imágenes tradicionales a tensores de PyTorch compatibles con arquitecturas de Transformers.
*   **Interfaz Web Interactiva:** Creación de una Web UI moderna mediante **Gradio** que permite a cualquier usuario arrastrar y soltar imágenes para recibir subtítulos en tiempo real.
*   **Automatización y Pruebas Locales:** Scripts desacoplados listos para ejecutar pruebas en local y flujos automatizados independientes de la interfaz gráfica.

## 📁 Componentes Técnicos Clave
*   **`image_captioning_app.py`**: Archivo principal que levanta el servidor web de **Gradio**. Recibe la imagen de la interfaz como una matriz NumPy, la convierte al espacio de color RGB mediante `Pillow` e invoca el modelo para retornar el texto final.
*   **`image_cap.py`**: Script de pruebas *offline* que carga el procesador y el modelo de Salesforce para generar descripciones con prefijos específicos utilizando la imagen local de prueba (`Hotaru_Tomoe_Black.png`).

## 🛠️ Tecnologías Utilizadas
*   **Framework de IA:** Hugging Face Transformers (`AutoProcessor`, `BlipForConditionalGeneration`)
*   **Deep Learning Engine:** PyTorch (Tensores orientados a inferencia)
*   **Interfaz de Usuario:** Gradio
*   **Manipulación de Imágenes:** Pillow (PIL) y NumPy
*   **Lenguaje:** Python 3.x

## 🚀 Instalación y Ejecución Local

### 1. Clonar el repositorio
```bash
git clone https://github.com
cd IMG-Captioning-AI
```

### 2. Instalar las dependencias de Machine Learning
Asegúrate de contar con las librerías necesarias ejecutando:
```bash
pip install transformers torch gradio pillow numpy requests
```

### 3. Ejecutar la Aplicación Web (Interfaz Gradio)
Levanta el servidor interactivo local:
```bash
python image_captioning_app.py
```
Abre en tu navegador la dirección local generada en la terminal (por defecto `http://127.0.0.1:7860`).

### 4. Ejecutar Prueba por Consola (Script de Prueba)
Si deseas validar el comportamiento del modelo directamente en tu terminal utilizando la imagen de muestra integrada en el repositorio:
```bash
python image_cap.py
```

## 📈 Competencias Demostradas (Para Reclutadores Técnicos)
*   **MLOps y Prototipado Rápido:** Habilidad para transformar un modelo complejo de Deep Learning en un producto web funcional y fácil de probar en minutos.
*   **Manipulación de Pipelines Multimodales:** Correcto manejo de flujos donde convergen datos de tipo imagen (Visión) y tipos de texto (Procesamiento de Lenguaje Natural).
*   **Clean Code:** Modularización clara del código separando la capa del cliente de la lógica pura del modelo.
