# Simulación Cadenas de Markov

## 📋 Contenido del Cuaderno

El cuaderno está estructurado en secciones principales para guiar el aprendizaje desde los fundamentos probabilísticos hasta la abstracción de software:

### 1. Fundamentos: Estados y Matrices de Transición
* **Enfoque:** Introducción teórica a los procesos estocásticos que cumplen con la propiedad de Markov (la falta de memoria).
* **Conceptos:** Definición del espacio de estados y construcción de la matriz de transición de probabilidades ($P$), asegurando que las filas sumen 1.

### 2. Simulación de Trayectorias (Caminatas Aleatorias)
* **Enfoque:** Implementación del algoritmo paso a paso para simular la evolución del sistema a lo largo del tiempo.
* **Visualización:** Gráficos que muestran la evolución temporal del estado (trayectorias), ilustrando cómo el sistema salta de un estado a otro basándose en las probabilidades condicionales.

### 3. Distribución Estacionaria y Comportamiento a largo plazo
* **Enfoque:** Análisis de qué sucede cuando la cadena de Markov evoluciona durante un gran número de pasos (si es ergódica).
* **Cálculo:** Uso de álgebra lineal (cálculo de autovectores y autovalores) y multiplicación iterativa de matrices para encontrar la distribución límite ($\pi$).
* **Visualización:** Gráficos de barras comparando la distribución de estados simulada empíricamente frente a la teórica a largo plazo.

### 4. Estados Absorbentes y Tiempos de Llegada (Opcional)
* **Enfoque:** Análisis de cadenas con estados de los cuales no se puede salir (estados absorbentes).
* **Cálculo:** Estimación del tiempo medio de absorción y la probabilidad de terminar en un estado específico partiendo desde diferentes estados iniciales.

### 5. Refactorización con Programación Orientada a Objetos (POO)
* **Enfoque:** Transformación del código procedural en una arquitectura limpia, modular y reutilizable.
* **Arquitectura:** Diseño de una clase `MarkovChain`:
  * Almacena y valida la matriz de transición y el espacio de estados.
  * Métodos integrados para simular trayectorias (`simulate(steps)`).
  * Métodos para calcular propiedades matemáticas como la distribución estacionaria (`get_stationary_distribution()`).

---

## 🛠️ Tecnologías y Librerías Utilizadas

El código está escrito en **Python 3** y utiliza las siguientes librerías:

* **NumPy (`numpy`):** Herramienta central para la manipulación de matrices de transición, álgebra lineal (cálculo de autovectores) y la generación eficiente de números aleatorios usando distribuciones discretas.
* **Matplotlib (`matplotlib.pyplot`):** Utilizada para la visualización de las trayectorias en el tiempo y gráficos de distribución de estados.
* **Random / Math:** Para operaciones probabilísticas básicas si no se emplea NumPy en las primeras etapas.
