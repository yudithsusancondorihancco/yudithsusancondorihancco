#include <iostream>
#include <vector>
#include <cstdlib>
#include <ctime>

using namespace std;

// Definición de la gramática
vector<string> generarFrase() {
    vector<string> gramatica = {"0", "1"};

    return gramatica;
}

// Generar frase aleatoria según la gramática
string generarLenguaje() {
    vector<string> gramatica = generarFrase();
    string lenguaje = "";

    for (int i = 0; i < 5; i++) {
        int indice = rand() % gramatica.size();
        lenguaje += gramatica[indice];
    }

    return lenguaje;
}

int main() {
    // Semilla para números aleatorios
    srand(time(NULL));

    // Generar y mostrar lenguajes
    for (int i = 0; i < 5; i++) {
        string lenguaje = generarLenguaje();
        cout << lenguaje << endl;
    }

    return 0;
}
