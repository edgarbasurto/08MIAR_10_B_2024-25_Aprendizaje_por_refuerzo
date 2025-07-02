# Proyecto Práctico - DQN en SpaceInvaders

**Máster en Inteligencia Artificial - Aprendizaje por Refuerzo**  
Universidad Internacional de Valencia (VIU)

## Descripción del Proyecto

Este proyecto consiste en el desarrollo e implementación de un agente inteligente basado en el algoritmo Deep Q-Network (DQN) para jugar el entorno `ALE/SpaceInvaders-v5` de OpenAI Gym. El objetivo principal es que el agente alcance una **recompensa media superior a 20 puntos** en modo de test, lo cual se considera el criterio mínimo de éxito.

## Autores

- Basurto Cruz Edgar Daniel
- Bravo Esquivias Gustavo Roger
- Manjarrez Jinez Paúl Alexander
- Pardo Hortua Eduar Uriel

## Estructura del Proyecto

### 1. Instalación y entorno
El proyecto fue diseñado para ejecutarse tanto en **Google Colab** como en un entorno local. Se incluyen instrucciones específicas para montar Google Drive y gestionar la persistencia de archivos. En caso de ejecutarse en local, se recomienda el uso de un entorno virtual con Python 3.10 o inferior.

### 2. Implementación del algoritmo DQN
El agente implementa las siguientes características:
- Red neuronal convolucional para procesar imágenes de entrada (84x84 píxeles)
- Replay buffer para experiencia
- Política epsilon-greedy para exploración
- Actualización del modelo de destino (`modelo_final.pth`) de forma periódica
- Preprocesamiento de frames (grayscale + resize + stack)

### 3. Entrenamiento del agente
El entrenamiento del agente se realiza durante varios miles de episodios, recolectando recompensas y ajustando la red de valor para aprender una política óptima. Se almacenan los modelos entrenados para permitir la evaluación en modo test.

### 4. Evaluación
Se incluye una rutina de evaluación para probar el agente entrenado sin exploración, evaluando su capacidad en un entorno determinista.

## Requisitos

Instalar las siguientes dependencias (en un entorno con Python 3.10):

```bash
pip install gym[atari]
pip install opencv-python
pip install numpy
pip install torch
pip install matplotlib
```

## Resultados
- El agente logró superar la media de 20 puntos de recompensa en modo test, cumpliendo con los requisitos del proyecto.
- Se analizaron las recompensas acumuladas y se visualizaron episodios para validar el comportamiento aprendido.

## Consideraciones
- El entorno SpaceInvaders-v5 requiere renderizado por frames, lo cual puede no ser soportado directamente en Google Colab.
- Se recomienda ejecutar las pruebas visuales en local para una experiencia más fluida.

