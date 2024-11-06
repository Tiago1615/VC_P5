# Visión por Computador: Práctica 5. Detección y caracterización de caras

### Autores

- [@Mauro Gómez Guillén](https://github.com/MGGdesigns)
- [@Santiago Santana Martínez](https://github.com/Tiago1615)

## Tabla de Contenidos

- [Paquetes necesarios](#paquetes-necesarios)
- [Introducción](#introducción)
- [Funcionalidades](#funcionalidades)
- [Resultado](#resultado)
- [Referencias Bibliográficas](#referencias-bibliográficas)

---

## Paquetes necesarios

- **Librerías**:
  - `opencv-python`
  - `deepface`
  - `Pillow`

```bash
pip install opencv-python
```

```bash
pip install deepface
```

```bash
pip install pillow
```

## Introducción:
Este proyecto consiste en un filtro de video en tiempo real que detecta rostros y analiza emociones utilizando DeepFace. Cuando se detecta una expresión de enfado, el filtro superpone efectos visuales como el cabello de Super Saiyan y un aura animada, similar al estilo de Dragon Ball Z.

---

## Funcionalidades

- **Detección de Rostros y Análisis de Emociones**: Utiliza DeepFace para detectar rostros en cada fotograma y analizar la emoción dominante.
- **Superposición de Efectos Visuales:** Cuando la emoción detectada es "enfado", el programa superpone un cabello estilo Super Saiyan, un "scouter" y una animación de aura alrededor del rostro detectado.
- **Animación Dinámica:** El aura y el cabello cambian en función de un contador de fotogramas, simulando diferentes transformaciones de poder.
- **Grabación de Video:** El video con efectos se graba en un archivo de salida en formato MP4.

## Procedimiento

El flujo de procesamiento de cada fotograma es el siguiente:

- Captura de Fotogramas: Se capturan fotogramas en tiempo real desde la cámara.
- Detección de Rostros: Utiliza DeepFace con el detector MTCNN para identificar rostros en el fotograma.
- Análisis de Emoción: Evalúa la emoción dominante del rostro detectado.
  - Aplicación de Efectos:
      - Si la emoción es "enfado":
        - Se superpone el cabello estilo Super Saiyan y un aura.
        - Se actualizan los efectos en función del número de fotogramas procesados.
      - Si la emoción no es "enfado", se aplica solo el cabello de "Goku" sin aura.
  - Grabación y Visualización: Se guardan los fotogramas procesados en un archivo de video y se muestran en pantalla en tiempo real.

#### Resultado

A continuación se muestra el *gif* obtenido al realizar la conversión del vídeo volcado a disco:

![Resultado Filtro](kakaroto.gif)

---

## Referencias Bibliográficas

- [Guión de la práctica](https://github.com/otsedom/otsedom.github.io/tree/main/VC/P5)
- [Documentación OpenCV](https://docs.opencv.org/4.x/)
- [Documentación Deepface](https://pypi.org/project/deepface/)
- [Herramienta para la conversión a *gif*](https://www.adobe.com/es/express/feature/video/convert/mp4-to-gif)

---

