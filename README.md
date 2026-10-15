# AEDS-Lista-6
Um dos exercícios de AEDs pois foi um dos únicos projetos que fiz.

Projeto codificado em C.
O Objetivo do projeto é criar um arquivo com texto escrito pelo usuário e falar quantas vezes o caractere 'a' aparece.
Copie o código e o coloque no code blocks e execute.

#include <stdio.h>
#include <stdlib.h>

int main() {
    FILE *fp = fopen("Lista6Exercicio2.txt", "w");
    char c[255];
    int charA = 0;

    fgets(c, 255, stdin);
    fputs(c, fp);

    fclose(fp); // Cria Arquivo

    fp = fopen("Lista6Exercicio2.txt", "r");
    char caracter;

    while ((caracter = fgetc(fp)) != EOF) {
        if (caracter == 'a') {
            charA++;
        }
    }

    fclose(fp);

    printf("%d Caracteres", charA);

    return 0;
}
