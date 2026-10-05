def leer_matriz():
    while True:
        try:
            filas = int(input("Ingrese el número de filas: "))
            columnas = int(input("Ingrese el número de columnas: "))
            if filas <= 0 or columnas <= 0 or filas != columnas:
                raise ValueError("La matriz debe ser cuadrada (filas = columnas) y mayor que 0.")
            break
        except ValueError as e:
            print("Error:", e)

    matriz = []
    for i in range(filas):
        fila_actual = []
        for j in range(columnas):
            valor = int(input(f"Elemento [{i}][{j}]: "))
            fila_actual.append(valor)
        matriz.append(fila_actual)
    return matriz


def transponer(matriz):
    n = len(matriz)
    transpuesta = []
    for j in range(n):
        fila_nueva = []
        for i in range(n):
            fila_nueva.append(matriz[i][j])
        transpuesta.append(fila_nueva)
    return transpuesta


def es_simetrica(matriz):
    transpuesta = transponer(matriz)
    return matriz == transpuesta


matriz = leer_matriz()

print("\nMatriz ingresada:")
for fila in matriz:
    print(*fila)

transpuesta = transponer(matriz)
print("\nMatriz transpuesta:")
for fila in transpuesta:
    print(*fila)

if es_simetrica(matriz):
    print("\nLa matriz SÍ es simétrica (A = Aᵀ).")
else:
    print("\nLa matriz NO es simétrica (A ≠ Aᵀ).")
