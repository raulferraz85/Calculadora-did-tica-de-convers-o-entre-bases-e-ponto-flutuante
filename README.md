# Calculadora-did-tica-de-convers-o-entre-bases-e-ponto-flutuante
Calculadora didática de conversão entre bases e ponto flutuante de precisão simpes e dupla
#include <stdio.h>


void decToBin(int n) {
    int bin[32];
    int i = 0;
    while (n > 0) {
        bin[i] = n % 2;
        n = n / 2;
        i++;
    }
    printf("Passo a passo da conversão para base 2:\n");
    for (int j = i - 1; j >= 0; j--) {
        printf("%d", bin[j]);
    }
    printf("\n");
}

int main() {
    int n;

    printf("Digite um número em base 10: ");
    scanf("%d", &n);

    decToBin(n);

    return 0;
}
