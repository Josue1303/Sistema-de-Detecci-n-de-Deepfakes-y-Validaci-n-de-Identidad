Sistema de Detección de Deepfakes y Validación de Identidad

Sistema de verificación de identidad en tiempo real diseñado para detectar intentos de suplantación mediante deepfakes. Integra visión por computadora, aprendizaje profundo y verificación documental automatizada, todo a partir de una experiencia guiada en video.

## 📌 Funcionalidades

- **Detección de Deepfakes** en video usando modelos fine-tuneados sobre EfficientNet con el dataset Celeb-DF v2.
- **Prueba de vida (liveness detection)** basada en gestos como parpadeo y movimientos de cabeza.
- **Captura automática de selfie** tras la validación de vida.
- **OCR y validación oficial de CURP** comparando la INE con los registros oficiales mediante scraping con Selenium.
- **Recorte facial desde la INE** usando Mediapipe.
- **Comparación biométrica entre selfie e INE** con `face_recognition` para asegurar coincidencia facial.

## 🧱 Estructura del Proyecto

- `retodevida.ipynb`: Implementación de la prueba de vida (detección de movimientos/parpadeo).
- `sistema_completo.ipynb`: Pipeline completo unificado, desde la prueba de vida hasta validación de identidad facial y textual.
- `preprocesamiento_mediapipe.ipynb`: Extracción de rostros y preprocesamiento del dataset para entrenamiento.
- `construccion_modelo_mediapipe.ipynb`: Construcción y entrenamiento del modelo de detección de deepfakes.
- `prueba_modelo_mediapipe.ipynb`: Evaluación del modelo con métricas como Accuracy y F1-score.

## 📂 Dataset

- **Base**: FaceForensics++ para robustez adicional
- Archivos organizados por tipo de manipulación con CSVs de metadatos.

## ⚙️ Tecnologías y Librerías

- Python 3.x, OpenCV, MediaPipe, face_recognition, Selenium, PyTorch, EfficientNet, EasyOCR
- Selenium + ChromeDriver para validación oficial de CURP

## 🚀 Requisitos

- GPU compatible con CUDA
- Entorno virtual `.venv` configurado
- Acceso al dataset Celeb-DF v2 y a los modelos fine-tuneados
