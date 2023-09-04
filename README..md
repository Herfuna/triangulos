Universidad Mariano Galves de Guatemala
Juan de Jesus Fuentes Hernandez
Diferentes tipos de Trinagulos

Seudocodigo:
    //Programa que imprime 4 tipos de triangulos diferentes
     Algoritmo triangulo_inverso
        Definir numero,tipo como Entero
	Escribir "Escriba uno de los 4 tipos de triangulo que quiera: ";
	Escribir "1.Triangulo hacia la derecha con angulo inferior";
	Escribir "2.Triangulo hacia la izquierda con angulo inferior";
	Escribir "3.Triangulo hacia la derecha con angulo superior";
	Escribir "4.Triangulo hacia la izquierda con angulo inferior";
	leer tipo;
        Escribir "Ingrese un número:"
        Leer numero;
	   Si tipo == 4 Entonces
	        	Para i <- 0 Hasta numero - 1 Con Paso 1 Hacer
		        	Para j <- 0 Hasta i Con Paso 1 Hacer
				Escribir Sin Saltar "  "
			    Fin Para
			   Para j <- 0 Hasta numero - i - 1 Con Paso 1 Hacer
				Escribir Sin Saltar "* "
			    Fin Para
			   Escribir ""
	        	Fin Para
	 SiNo
           Si tipo == 2 Entonces
			   Para i <- 0 Hasta numero - 1 Con Paso 1 Hacer
				   Para j <- 0 Hasta numero - 1 Con Paso 1 Hacer
					   Si j < numero - i - 1 Entonces
						   Escribir Sin Saltar "  "
					Sino
						Escribir Sin Saltar "* "
					  Fin Si
				  Fin Para
				   Escribir ""
			  Fin Para
		  SiNo
			   Si tipo == 1 Entonces
				   Para i <- 0 Hasta numero - 1 Con Paso 1 Hacer
					   Para j <- 0 Hasta i Con Paso 1 Hacer
						  Escribir Sin Saltar "* "
					   Fin Para
					  Escribir ""
				  Fin Para
			    Sino
                                   Si tipo == 3 Entonces
				          	Para i <- 0 Hasta numero - 1 Con Paso 1 Hacer
					        	Para j <- 0 Hasta numero - i - 1 Con Paso 1 Hacer
						        	Escribir Sin Saltar "* "
	                    					Fin Para
			              			Escribir ""
					       Fin Para
				         SiNo
				         	esscribir "esta opcion no existe"
				     Fin Si
			    Fin Si
		     Fin Si
	     Fin Si

     FinAlgoritmo


C++
//Programa que imprime 4 tipos de triangulos diferentes

#include <iostream>

using namespace std;

int main() {
    int numero, tipo;
    
    cout << "Escriba uno de los 4 tipos de triangulo que quiera: " << endl;
    cout << "1.Triangulo hacia la derecha con angulo inferior" << endl;
    cout << "2.Triangulo hacia la izquierda con angulo inferior" << endl;
    cout << "3.Triangulo hacia la derecha con angulo superior" << endl;
    cout << "4.Triangulo hacia la izquierda con angulo inferior" << endl;
    cin >> tipo;
    
    cout << "Ingrese un número:" << endl;
    cin >> numero;
    
    if (tipo == 4) {
        for (int i = 0; i < numero; i++) {
            for (int j = 0; j < i; j++) {
                cout << "  ";
            }
            for (int j = 0; j < numero - i; j++) {
                cout << "* ";
            }
            cout << endl;
        }
    } else if (tipo == 2) {
        for (int i = 0; i < numero; i++) {
            for (int j = 0; j < numero; j++) {
                if (j < numero - i - 1) {
                    cout << "  ";
                } else {
                    cout << "* ";
                }
            }
            cout << endl;
        }
    } else if (tipo == 1) {
        for (int i = 0; i < numero; i++) {
            for (int j = 0; j <= i; j++) {
                cout << "* ";
            }
            cout << endl;
        }
    } else if (tipo == 3) {
        for (int i = 0; i < numero; i++) {
            for (int j = 0; j < numero - i; j++) {
                cout << "* ";
            }
            cout << endl;
        }
    } else {
        cout << "Esta opción no existe" << endl;
    }
    
    return 0;
}


python

numero = int(input("Ingrese un número: "))
tipo = int(input("Escriba uno de los 4 tipos de triángulo que quiera:\n1. Triángulo hacia la derecha con ángulo inferior\n2. Triángulo hacia la izquierda con ángulo inferior\n3. Triángulo hacia la derecha con ángulo superior\n4. Triángulo hacia la izquierda con ángulo inferior\n"))

if tipo == 4:
    for i in range(numero):
        for j in range(i):
            print("  ", end="")
        for j in range(numero - i):
            print("* ", end="")
        print()
elif tipo == 2:
    for i in range(numero):
        for j in range(numero):
            if j < numero - i - 1:
                print("  ", end="")
            else:
                print("* ", end="")
        print()
elif tipo == 1:
    for i in range(numero):
        for j in range(i + 1):
            print("* ", end="")
        print()
elif tipo == 3:
    for i in range(numero):
        for j in range(numero - i):
            print("* ", end="")
        print()
else:
    print("Esta opción no existe")
