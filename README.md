# Proyecto de Búsqueda y Optimización

**Autora**: Laura González Pizarro  
**Fecha**: Noviembre 2024  
**Nota**: 9.4/10

## Descripción
Una fábrica recibe todas las mañanas un pedido con las tareas que debe realizar durante el día. Cada una de las tareas pertenece a uno, y sólo uno de
los tipos a, b, c o d, y se sabe el tiempo exacto de procesamiento requerido para su realización. Para ello, la fábrica dispone de una cantidad arbitraria
de máquinas dispuestas en paralelo, una o más de cada uno de los tipos indicados, de modo que cada máquina sólo puede realizar tareas de su tipo.
Se desea determinar el orden y asignación de tareas a máquinas de tal modo que el tiempo total de realización de todas las tareas sea el mínimo.

## Estructura del Proyecto

1. **Espacio de Estados**
   - Representa las configuraciones de las máquinas y el estado de la demanda de tareas.
   - La asignación de tareas es la única acción permitida.
   - El coste de la asignación depende del tiempo máximo que toma una máquina para completar todas sus tareas.

2. **Heurísticas**
   - Se definen varias heurísticas para guiar la búsqueda que estima el tiempo necesario en función de la capacidad de procesamiento de cada grupo de máquinas. Se realiza una comparación entre ellas para identificar cuál es más informada, es decir, que expande menos nodos para encontrar la solución optima.

3. **Experimentos realizados**

## Implementación

El proyecto está desarrollado en Python con un diseño de programación orientada a objetos donde las tareas, maquinas, fabrica y demanda son represnetada por clases que tienen funciones para la resolución del problema. Los algoritmos de búsqueda implementados incluyen:

- **Fuerza Bruta**: Evalúa todas las posibles asignaciones de las tareas en las máquinas.
- **A\***: Un algoritmo de búsqueda heurística que prioriza los estados de menor coste estimado.
- **Weighted A\***: Variante de A* que permite ajustar la importancia de la heurística, acelerando la búsqueda a cambio de una solución potencialmente subóptima.
- **Monte Carlo**: Algoritmo de asignación aleatoria de las tareas a las máquinas.

## Experimentos
Se realizaron experimentos para validar la eficiencia de las heurísticas y la precisión de los algoritmos. Los análisis incluyeron:

1. **Comparación de Heurísticas**: Se evaluó qué heurística era más informada y reducía mejor el tiempo de ejecución.
2. **Parámetros de Weighted A\***: Se analizó el parámetro de peso para obtener el mejor compromiso entre nodos expandidos y error cometido.
3. **Rendimiento de los Algoritmos**: Se compararon el tiempo de ejecución y el número de nodos expandidos de cada algoritmo, variando el volumen de tareas y máquinas.

