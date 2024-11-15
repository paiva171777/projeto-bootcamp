# projeto-bootcamp
//Ideia para o projeto: Calculadora Simples
//Uma calculadora simples é um ótimo cimeço para um projeto em C, pois abrange conceitos básicos como:

Entrada e saída de dados: Para receber os números e operações do usuário.
Operadores aritméticos: Para realizar as operações matemáticas.
Estrutura condicional: Para escolher a operação a ser realizada.
Laços de repetição: Para permitir que o usuário realize várias operações.

(USEI C PORQUE É A LINGUAGEM QUE TRABALHEI NESSE SEMESTRE E TENHO MAIS FACILIDADE)








#include <stdio.h>

int main() {
    char operacao;
    double num1, num2, result;

    printf("Digite a operacao (+, -, *, /): ");
    scanf(" %c", &operacao);

    printf("Digite dois numeros: ");
    scanf("%lf %lf", &num1, &num2);

    switch (operacao) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            if (num2 == 0) {
                printf("Erro: Divisao por zero!\n");
                return 1;
            }
            result = num1 / num2;
            break;
        default:
            printf("Operador invalido!\n");
            return 1;
    }

    printf("%.2lf %c %.2lf = %.2lf\n", num1, operaçao, num2, resultado);

    return 0;
}

