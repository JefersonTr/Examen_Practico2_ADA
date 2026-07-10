# Desafíos de Árboles Binarios en Python

Este repositorio contiene las soluciones optimizadas para dos problemas clásicos de estructuras de datos: **Validación de un BST** y **Rotación Dinámica de Nodos (Swap Nodes)**.

---

## 1. Validación de Árbol de Búsqueda Binaria (BST)

Determina si un árbol binario cumple con las condiciones de ordenamiento de un BST: todos los nodos a la izquierda de la raíz deben ser menores, y todos a la derecha deben ser mayores.

### Cómo usarlo
El código utiliza una función recursiva que valida los límites permisibles ($-\infty$, $+\infty$) para cada nodo:

# Ejemplo de uso conceptual
# raiz = Node(10)
# raiz.left = Node(5)
# raiz.right = Node(15)

# Retorna True si es un BST válido, o False si no lo es
# es_valido = check_binary_search_tree_(raiz)
# print(f"¿Es un BST válido?: {es_valido}")

## 2. Rotación Dinámica de Nodos (Swap Nodes)

### ¿Para qué sirve?
Este algoritmo permite modificar de forma masiva la estructura de un árbol binario basándose en la profundidad de sus niveles. Su utilidad principal radica en la optimización de consultas: en lugar de recorrer todo el árbol cada vez que se quiere hacer una modificación, el código salta directamente a los niveles que son múltiplos de un valor $k$ e intercambia de posición sus ramas izquierda y derecha. 

Esto es especialmente útil en simulaciones de estructuras dinámicas, problemas avanzados de árboles y competencias de código como HackerRank, ya que reduce drásticamente el tiempo de procesamiento en árboles gigantescos.

# Definición del árbol (Hijos del nodo 1, luego del nodo 2, etc.)
# Representa un árbol con estructura:
#       1
#      / \
#     2   3
mis_indices = [
    [2, 3],   # Hijos del nodo 1
    [-1, -1], # Hijos del nodo 2 (no tiene)
    [-1, -1]  # Hijos del nodo 3 (no tiene)
]

# Queremos aplicar un intercambio en el nivel 1
mis_consultas = [1]

# Ejecutamos la función
resultados = swapNodes(mis_indices, mis_consultas)

# Imprimimos el resultado
print("Resultado del recorrido In-Order después del intercambio:")
print(resultados) 
# Debería imprimir: [[3, 1, 2]]
# Devuelve una lista con los recorridos In-Order después de cada consulta
print(resultados)
