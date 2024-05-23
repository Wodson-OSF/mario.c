# mario.c
#include <cs50.h>  // Inclui a biblioteca cs50 para funções adicionais
#include <stdio.h>  // Inclui a biblioteca padrão de entrada e saída (stdio.h)

int main(void) {  // Função principal do programa

    // Declara uma variável 'p' do tipo 'int' para armazenar o peso da pirâmide
    int p;

    // Loop 'do-while' para garantir que o usuário digite um valor válido para o peso
    do {
        // Solicita ao usuário que digite o peso da pirâmide
        p = get_int("Peso: ");

        // Condição para loop: repete enquanto 'p' for menor que 1 ou maior que 8
    } while (p < 1 || p > 8);

    // Criação da pirâmide de asteriscos
    for (int i = 0; i < p; i++) {  // Loop para cada linha da pirâmide
        for (int j = 0; j < p; j++) {  // Loop para cada coluna da pirâmide
            // Verifica se a posição atual (i, j) está na parte inferior esquerda da pirâmide
            if (i + j < p - 1) {
                // Se estiver, imprime um espaço em branco
                printf(" ");
            } else {
                // Se não estiver, imprime um asterisco
                printf("#");
            }
        }
        // Quebra de linha para ir para a próxima linha da pirâmide
        printf("\n");
    }

    return 0;  // Indica que o programa foi executado com sucesso
}
  
