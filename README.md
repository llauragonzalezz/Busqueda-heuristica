# Proyecto de Búsqueda y Optimización

**Autora**: Laura González Pizarro  
**Fecha**: Noviembre 2024  

## Descripción

Este proyecto aborda la optimización de tareas en una fábrica mediante algoritmos de búsqueda y heurísticas. El problema consiste en asignar eficientemente un conjunto de tareas de distintos tipos (a, b, c o d) a máquinas especializadas para minimizar el tiempo total de realización. Este tipo de problema es común en sistemas de producción y planificación, donde se busca la asignación óptima de recursos.

## Estructura del Proyecto

1. **Problema**
   - La fábrica recibe un conjunto de tareas a realizar diariamente, donde cada tarea tiene un tipo específico y tiempo de procesamiento asociado.
   - El objetivo es asignar estas tareas a las máquinas disponibles, minimizando el tiempo total de ejecución.

2. **Espacio de Estados**
   - Representa las configuraciones de las máquinas y el estado de la demanda de tareas.
   - La asignación de tareas es la única acción permitida.
   - El coste de la asignación depende del tiempo máximo que toma una máquina para completar todas sus tareas.

3. **Heurísticas**
   - Se definen varias heurísticas para guiar la búsqueda, incluyendo una heurística informada que estima el tiempo necesario en función de la capacidad de procesamiento de cada grupo de máquinas.

## Implementación

El proyecto está desarrollado en Python e incluye clases y funciones para representar el problema, las máquinas, y los estados de la fábrica. Los algoritmos de búsqueda implementados incluyen:

- **Fuerza Bruta**: Evalúa todas las posibles asignaciones, resultando inviable para grandes volúmenes de tareas.
- **A\***: Un algoritmo de búsqueda heurística que prioriza los estados de menor coste estimado.
- **Weighted A\***: Variante de A* que permite ajustar la importancia de la heurística, acelerando la búsqueda a cambio de una solución potencialmente subóptima.
- **Monte Carlo**: Algoritmo de asignación aleatoria eficiente para grandes volúmenes de tareas, aunque menos preciso en escenarios con tiempos variados.

## Experimentos

Se realizaron experimentos para evaluar el rendimiento de los algoritmos, comparando el tiempo de ejecución y el número de nodos expandidos con diferentes volúmenes de tareas y máquinas.

## Conclusiones

- La elección de una heurística informada y estructuras de datos adecuadas mejora significativamente el rendimiento.
- El algoritmo A* con la heurística h1 resultó ser el más eficiente para resolver el problema de forma óptima.
- Weighted A* ofrece un balance útil entre precisión y velocidad.
- La implementación en un entorno distribuido o concurrente podría mejorar el rendimiento en aplicaciones a gran escala.
