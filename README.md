# Calculadora-did-tica-de-convers-o-entre-bases-e-ponto-flutuante
Calculadora didática de conversão entre bases e ponto flutuante de precisão simpes e dupla
#include <stdio.h>


#include <stdio.h>
#include <stdlib.h>

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

void decToOctal(int n) {
    int octal[32];
    int i = 0;
    while (n > 0) {
        octal[i] = n % 8;
        n = n / 8;
        i++;
    }
    printf("Passo a passo da conversão para base 8:\n");
    for (int j = i - 1; j >= 0; j--) {
        printf("%d", octal[j]);
    }
    printf("\n");
}
void decToHex(int n) {
    char hex[32];
    int i = 0;
    while (n > 0) {
        int temp = n % 16;
        if (temp < 10) {
            hex[i] = temp + 48;
        } else {
            hex[i] = temp + 55;
        }
        n = n / 16;
        i++;
    }
    printf("Passo a passo da conversão para base 16:\n");
    for (int j = i - 1; j >= 0; j--) {
        printf("%c", hex[j]);
    }
    printf("\n");
}

void decToBCD(int n) {
    int bcd[32];
    int i = 0;
    printf("Passo a passo da conversão para BCD:\n");
    while (n > 0) {
        int digit = n % 10;
        for (int j = 0; j < 4; j++) {
            bcd[i + j] = (digit >> j) & 1;
        }
        i += 4;
        n = n / 10;
    }
    for (int j = i - 1; j >= 0; j--) {
        printf("%d", bcd[j]);
    }
    printf("\n");
}
