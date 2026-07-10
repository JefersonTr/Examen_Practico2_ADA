# Desafíos de Árboles Binarios en Python

Este repositorio contiene las soluciones optimizadas para dos problemas clásicos de estructuras de datos: **Validación de un BST** y **Rotación Dinámica de Nodos (Swap Nodes)**.

---

## 1. Validación de Árbol de Búsqueda Binaria (BST)

Determina si un árbol binario cumple con las condiciones de ordenamiento de un BST: todos los nodos a la izquierda de la raíz deben ser menores, y todos a la derecha deben ser mayores.

### Cómo usarlo
El código utiliza una función recursiva que valida los límites permisibles ($-\infty$, $+\infty$) para cada nodo:

```python
# Ejemplo de uso conceptual
raiz = Node(10)
raiz.left = Node(5)
raiz.right = Node(15)

# Retorna True si es un BST válido, o False si no lo es
es_valido = check_binary_search_tree_(raiz)
print(f"¿Es un BST válido?: {es_valido}")
