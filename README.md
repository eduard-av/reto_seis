# Reto_seis

Se presenta el desarrollo del reto #6:

Desarrolle de manera individual la mayoría de ejercicios en clase. Para cada punto cree un programa individual asimismo cree un notebook con la solución a todos los problemas. Al finalizar suba todo a un repo y subalo al canal reto_6 en slack, los tres primeros puntos deben incluir diagrama de flujo.

Nota: Todo el código de aquí en adelante debe ir debidamente documentado.

1. Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.
2. Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.
3. Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado
4. Imprimir el factorial de un número natural n dado.
5. Implementar un programa que ingrese un número de 2 a 50 y muestre sus divisores.
6. Implementar el algoritmo que muestre los números primos del 1 al 100. Nota: use funciones

Revisar los anexos donde se encontrara el desarrollo del reto.

# Diagramas de Flujo

1.
```mermaid
flowchart TD
    A[Inicio] --> B[Número\Cuadrado]
    B --> D[Iniciar bucle for desde 1 hasta 100]
    D --> E{¿Número <= 100?}
    E -->|Sí| F[Imprimir número y su cuadrado]
    F --> G[Incrementar número]
    G --> D
    E -->|No| H[Fin]

```
2. 
```mermaid
flowchart TD
    A[Inicio] --> B[Números Impares del 1 al 999]
    B --> D[Iniciar bucle para números impares desde 1 hasta 999]
    D --> E{¿Número <= 999?}
    E -->|Sí| F[Imprimir número impar]
    F --> G[Incrementar número en 2]
    G --> D
    E -->|No| H[Números Pares del 2 al 1000]
    H --> J[Iniciar bucle para números pares desde 2 hasta 1000]
    J --> K{¿Número <= 1000?}
    K -->|Sí| L[Imprimir número par]
    L --> M[Incrementar número en 2]
    M --> J
    K -->|No| N[Fin]

```
3.
```mermaid
graph TD
    A[Inicio] --> B[Ingresar un número natural n]
    B --> C{n >= 2?}
    C -- No --> D[Imprimir 'El número debe ser mayor o igual a 2']
    D --> E[Fin]
    C -- Sí --> F[Iniciar bucle for: i desde n hasta 2, paso -1]
    F --> G{i % 2 == 0?}
    G -- Sí --> H[Imprimir i]
    G -- No --> F
    H --> F
    F -->|Fin del bucle| E
```
