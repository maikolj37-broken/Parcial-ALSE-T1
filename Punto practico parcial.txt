#include <iostream>
#include <cmath>
using namespace std;

struct Point {
    double x;
    double y;
};

double calcularDistanciaMasCercana(
    Point puntos[],
    int n,
    const Point &pUsuario,
    int &indiceMasCercano
){
    if (n <= 0) {
        indiceMasCercano = -1;
        return -1;
    }

    double distanciaMin = sqrt(
        pow(puntos[0].x - pUsuario.x, 2) +
        pow(puntos[0].y - pUsuario.y, 2)
    );

    indiceMasCercano = 0;

    for (int i = 1; i < n; i++) {
        double distancia = sqrt(
            pow(puntos[i].x - pUsuario.x, 2) +
            pow(puntos[i].y - pUsuario.y, 2)
        );

        if (distancia < distanciaMin) {
            distanciaMin = distancia;
            indiceMasCercano = i;
        }
    }

    return distanciaMin;
}

int main() {
    int n;
    cout << "Cantidad de puntos: ";
    cin >> n;

    Point puntos[100]; // arreglo fijo simple

    for (int i = 0; i < n; i++) {
        cout << "Punto " << i+1 << " (x y): ";
        cin >> puntos[i].x >> puntos[i].y;
    }

    Point usuario;
    cout << "Punto de referencia (x y): ";
    cin >> usuario.x >> usuario.y;

    int indice;
    double distancia = calcularDistanciaMasCercana(puntos, n, usuario, indice);

    cout << "\nPunto mas cercano: ("
         << puntos[indice].x << ", "
         << puntos[indice].y << ")\n";

    cout << "Distancia: " << distancia << endl;

    return 0;
}