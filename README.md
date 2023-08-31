# Tarea-2-Tri-ngulos-Rect-ngulos-
Algoritmos en (Seudocódigo, C++ y Phyton) que solicitan un numero entero e imprimen triángulos


```psc

Algoritmo Tarea2_Triangulos_Rectangulos
    Definir opc, num, i, j Como Entero
    
    Escribir "Hola!, Porfavor ingresa un número entero positivo :D :"
    Leer num
    
    Si num > 0 Entonces
        Escribir "Ahora selecciona el tipo de triángulo rectángulo que deseas:"
        Escribir "#1. Un triángulo rectángulo en la esquina izquiera inferior"
        Escribir "#2. Un triángulo rectángulo en la esquina izquiera superior"
        Escribir "#3. Un triángulo rectángulo en la esquina derecha inferior"
        Escribir "#4. Un triángulo rectángulo en la esquina derecha superior"
        
        Leer opc
        
        Si opc >= 1 y opc <= 4 Entonces
            Para i = 1 Hasta num Hacer
                Si opc = 1 Entonces
                    Para j = 1 Hasta i Hacer
                        Escribir SinSaltar "*";
                    Fin Para
                Fin Si
                
                Si opc = 2 Entonces
                    Para j = 1 Hasta num - i + 1 Hacer
                        Escribir SinSaltar "*";
                    Fin Para
                Fin Si
                
                Si opc = 3 Entonces
                    Para j = 1 Hasta num - i Hacer
                        Escribir SinSaltar " ";
                    Fin Para
                    Para j = 1 Hasta i Hacer
                        Escribir SinSaltar "*";
                    Fin Para
                Fin Si
                
                Si opc = 4 Entonces
                    Para j = 1 Hasta i - 1 Hacer
                        Escribir SinSaltar " ";
                    Fin Para
                    Para j = 1 Hasta num - i + 1 Hacer
                        Escribir SinSaltar "*";
                    Fin Para
                Fin Si
                
                Escribir "";  
            Fin Para
        Fin Si
    Fin Si
    
Fin Algoritmo



```cpp

#include <iostream>
using namespace std;

int main() {
    int opc, num, i, j;
    
    cout << "Hola! Por favor ingresa un número entero positivo :D :";
    cin >> num;
    
    if (num > 0) {
        cout << "Ahora selecciona el tipo de triángulo rectángulo que deseas:" << endl;
        cout << "#1. Un triángulo rectángulo en la esquina izquierda inferior" << endl;
        cout << "#2. Un triángulo rectángulo en la esquina izquierda superior" << endl;
        cout << "#3. Un triángulo rectángulo en la esquina derecha inferior" << endl;
        cout << "#4. Un triángulo rectángulo en la esquina derecha superior" << endl;
        
        cin >> opc;
        
        if (opc >= 1 && opc <= 4) {
            for (i = 1; i <= num; i++) {
                if (opc == 1) {
                    for (j = 1; j <= i; j++) {
                        cout << "*";
                    }
                }
                
                if (opc == 2) {
                    for (j = 1; j <= num - i + 1; j++) {
                        cout << "*";
                    }
                }
                
                if (opc == 3) {
                    for (j = 1; j <= num - i; j++) {
                        cout << " ";
                    }
                    for (j = 1; j <= i; j++) {
                        cout << "*";
                    }
                }
                
                if (opc == 4) {
                    for (j = 1; j <= i - 1; j++) {
                        cout << " ";
                    }
                    for (j = 1; j <= num - i + 1; j++) {
                        cout << "*";
                    }
                }
                
                cout << endl;
            }
        }
    }
    
    return 0;
}

    

```python
print("Hola! Por favor ingresa un número entero positivo :D :")
num = int(input())

if num > 0:
    print("Ahora selecciona el tipo de triángulo rectángulo que deseas:")
    print("#1. Un triángulo rectángulo en la esquina izquierda inferior")
    print("#2. Un triángulo rectángulo en la esquina izquierda superior")
    print("#3. Un triángulo rectángulo en la esquina derecha inferior")
    print("#4. Un triángulo rectángulo en la esquina derecha superior")
    
    opc = int(input())
    
    if opc >= 1 and opc <= 4:
        for i in range(1, num + 1):
            if opc == 1:
                for j in range(1, i + 1):
                    print("*", end="")
            elif opc == 2:
                for j in range(1, num - i + 2):
                    print("*", end="")
            elif opc == 3:
                for j in range(1, num - i + 1):
                    print(" ", end="")
                for j in range(1, i + 1):
                    print("*", end="")
            elif opc == 4:
                for j in range(1, i):
                    print(" ", end="")
                for j in range(1, num - i + 2):
                    print("*", end="")
                
            print()




