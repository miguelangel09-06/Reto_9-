# Reto_9-
### Se adjunta un archivo en .ipynb con el desarrollo del codigo
## Los algoritmos de sorting
Los algoritmos de sorting son herramientas utilizadas en programacion para ordenadar los elementos de una lista o un arreglo en cierto orden (Ascendente o descendente).
Los algoritmos de ordenamiento se dividen en dos grandes categorías:

### Ordenamiento simple (basado en comparaciones)
Son fáciles de entender pero menos eficientes en listas grandes.

-Bubble Sort (Ordenamiento de burbuja)

-Selection Sort (Ordenamiento por selección)

-Insertion Sort (Ordenamiento por inserción)

### Ordenamiento eficiente (división y conquista o técnicas avanzadas)
Más rápidos y usados en la práctica para grandes volúmenes de datos.

-Merge Sort (Ordenamiento por mezcla)

-Quick Sort (Ordenamiento rápido)

-Heap Sort (Ordenamiento por montículos)

-Radix Sort (Ordenamiento por base, no usa comparaciones)

#### Bubble sort
Para este caso Bubble sort  es un algoritmo de ordenamiento simple , que funciona comparando elementos adyacentes y los intercambia si están en el orden incorrecto,recorre la lista de izquierda a derecha y compara de tal manera que 
si están en el orden correcto, los deja como están y
si están en el orden incorrecto, los intercambia,
,después de cada pasada, el número más grande "burbujea" hacia el final y
se repite el proceso hasta que no haya más intercambios.

Tiene algunas ventajas ya que es fácil de entender e implementar ademas de ser estable, aunque tiene desventajas ya que al enfrentarse a desafios grandes se vuelve lento, ademas de que en su mayoria es utilizado en el campo academico.

#### Impplementacion en python

# Optimized Python program for implementation of Bubble Sort
def bubbleSort(arr):
    n = len(arr)
    
    # Traverse through all array elements
    for i in range(n):
        swapped = False

        # Last i elements are already in place
        for j in range(0, n-i-1):

            # Traverse the array from 0 to n-i-1
            # Swap if the element found is greater
            # than the next element
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
        if (swapped == False):
            break

    if __name__ == "__main__":
      arr = [64, 34, 25, 12, 22, 11, 90]

    bubbleSort(arr)

    print("Sorted array:")
    for i in range(len(arr)):
        print("%d" % arr[i], end=" ")
