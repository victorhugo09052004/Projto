#include <stdio.h>
#include <stdlib.h>

int main() {
    // Declaração do ponteiro
    int *ptr;

    // Alocação inicial de memória para guardar oito inteiros
    ptr = (int *)malloc(8 * sizeof(int));
    if (ptr == NULL) {
        printf("Erro: Falha na alocação de memória!\n");
        return 1;
    }

    printf("Memória alocada para 8 inteiros.\n");

    // Realocação de memória para um tamanho que guarde doze inteiros
    ptr = (int *)realloc(ptr, 12 * sizeof(int));
    if (ptr == NULL) {
        printf("Erro: Falha na realocação de memória!\n");
        return 1;
    }

    printf("Memória realocada para 12 inteiros.\n");

    // Liberação de memória
    free(ptr);

    printf("Memória liberada.\n");

    return 0;
}
# Arquivos de compilação e executáveis
*.o
*.out
*.exe

# Arquivos temporários
*~
#include <stdio.h>
#include <stdlib.h>

int main() {
    // Alocação de memória para um vetor de inteiros
    int *ptr = (int *)malloc(5 * sizeof(int));
    if (ptr == NULL) {
        printf("Erro: Falha na alocação de memória!\n");
        return 1;
    }

    printf("Memória alocada com sucesso!\n");

    // Brincadeira
    printf("\nAguarde enquanto o programa carrega...\n");
    printf("Isso pode demorar um pouco...\n");

    for (int i = 0; i < 3; i++) {
        printf("Carregando. ");
        for (int j = 0; j < 3e7; j++) {} // Simulação de um processo demorado
        printf(".");
    }

    printf("\n\nPronto! O programa está carregado e pronto para uso.\n");

    // Liberação de memória alocada
    free(ptr);

    return 0;
}
