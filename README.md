# Frijol Vision

Aplicación de escritorio para analizar imágenes de plantas de frijol mediante modelos YOLO. Permite ejecutar predicciones, entrenar modelos y explorar resultados desde una interfaz PyQt6.

## Funcionalidades

- Carga de imágenes y visualización de detecciones.
- Identificación de las clases definidas por el modelo, como hojas, tallos y raíces.
- Configuración del entrenamiento y consulta de resultados.
- Visualización de métricas y matrices de confusión.
- Recorte de regiones detectadas para su inspección.

Las clases y la calidad de las predicciones dependen del dataset y de los pesos utilizados. El proyecto es una herramienta de análisis visual; sus resultados necesitan interpretación y validación.

## Tecnologías

Python, PyQt6, Ultralytics YOLO, PyTorch, OpenCV, NumPy, pandas y Matplotlib.

## Inicio local

Necesitas Python compatible con las dependencias de `UI/requirements.txt`. Para entrenamiento con GPU, prepara una instalación de PyTorch compatible con tu hardware.

Desde la raíz:

```bash
python -m venv .venv
.venv\Scripts\activate
python -m pip install -r UI/requirements.txt
python UI/main.py
```

El comando de activación corresponde a Windows. En Linux o macOS utiliza `source .venv/bin/activate`.

## Configuración y uso

1. Revisa `UI/config.ini` y las rutas de modelos y datos.
2. Selecciona pesos YOLO compatibles con el análisis que deseas realizar.
3. Abre una imagen y ejecuta la predicción.
4. Inspecciona las detecciones y los resultados generados.
5. Para entrenar, prepara las imágenes, etiquetas y configuración del dataset.

## Estructura

- `UI/main.py`: entrada de la aplicación.
- `UI/gui/`: ventanas y pestañas de predicción, entrenamiento y resultados.
- `UI/utils/`: configuración y utilidades.
- `content/`: modelos, datos y resultados de procesamiento.
- [Documentación de la interfaz](UI/README.md)

## Autor

[Sebastian Mejia](https://github.com/SebastianMejia1203) · Ingeniería de Sistemas, Universidad de la Amazonia.
