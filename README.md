# SistemaDeCadatsroELogin
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

void modulo_pessoal();
void modulo_financeiro();
void modulo_academico();
void modulo_utilidades();

int main() {
    // 1. Cadastro e Login
    char usuario[20];
    char senha[20];
    int validacao = 0;
    int tentativas = 0;
    int max_tentativas = 3;
    int opcao;

    printf("=== SISTEMA DE CADASTRO E LOGIN ===\n");
    printf("Digite o usuario: ");
    scanf("%s", usuario);

    while (validacao == 0 && tentativas < max_tentativas) {
        printf("Digite a senha: ");
        scanf("%s", senha);
        tentativas++;
        system ("cls");
        if (strlen(senha) < 6) {
            printf("Senha fraca! Use pelo menos 6 caracteres.\n");    
        }
        else if (strcmp(senha, "123456") == 0) {
            printf("Senha invalida! Tente novamente.\n");
        } 
        else {
            printf("===== LOGIN VALIDO! BEM-VINDO =====\n");
            validacao = 1; 
            break;
        }
    }

    if (validacao == 0) {
        printf("Numero maximo de tentativas excedido!\n");
        return 0;  // Encerra o programa se nÃ£o conseguiu logar
    }

    printf("========= MENU PRINCIPAL =========\n");
    printf("1 - PESSOAL\n");
    printf("2 - FINANCEIRO\n");
    printf("3 - ACADEMICO\n");
    printf("4 - UTILIDADES\n");
    printf("0 - SAIR\n");
    printf("Escolha uma opcao: ");
    scanf("%d", &opcao);

    switch(opcao){
        case 0:
            printf("Saindo do sistema...\n");
            break;
        case 1:
            modulo_pessoal();
            break;
        case 2:
            modulo_financeiro();
            break;
        case 3:
            modulo_academico();
            break;
        case 4:
            modulo_utilidades();
            break;
        default:
            printf("Opcao invalida! Tente novamente.\n");
            break;
    }

    return 0;
}

void modulo_pessoal(){
    int mod_opcao;

    do {
        printf("===== MODULO PESSOAL =====\n");
        printf("1 - CLASSIFICACAO DE IDADE\n");
        printf("2 - CALCULADORA DE IMC\n");
        printf("0 - VOLTAR AO MENU PRINCIPAL\n");
        printf("Escolha uma opcao: ");
        scanf("%d", &mod_opcao); 

        switch(mod_opcao){
            case 0:
                printf("Voltando ao menu principal...\n");
                break;
            case 1:
                {
                    int idade;
                    printf("------ CLASSIFICACAO DE IDADE ------\n");
                    printf("Digite sua idade: ");
                    scanf("%d", &idade);

                    if (idade < 16){
                        printf("MENOR DE IDADE | NAO ELEITOR\n");
                    } else if (idade >= 16 && idade < 18){
                        printf("%d ANOS | VOTO OPCIONAL\n", idade);
                    } else if (idade >= 18 && idade < 65){
                        printf("ADULTO MAIOR DE IDADE | VOTO OBRIGATORIO\n");
                    } else {
                        printf("IDOSO | VOTO OPCIONAL\n");
                    }
                    break;
                }
            case 2: 
                {
                    float peso, altura, imc;
                    int validacao = 0;
                    int tentativas = 0;
                    int max_tentativas = 3;

                    while (validacao == 0 && tentativas < max_tentativas) {
                        printf("------ CALCULADORA DE IMC ------\n");
                        printf("Digite seu peso (kg): ");
                        scanf("%f", &peso);
                        printf("Digite sua altura (m): ");
                        scanf("%f", &altura);
                        tentativas++;
                        system("cls"); 

                        if (peso <= 0 || altura <= 0) {
                            printf("Valor invalido! informe novamente seu peso e altura.\n");
                        } else {
                            imc = peso / (altura * altura);
                            printf("Seu IMC eh: %.2f\n", imc);
                            validacao = 1; 
                        }
                    }
                    break;
                }
                default:
                    printf("Opcao invalida! Tente novamente.\n");
                    break;
        }
    } while (mod_opcao != 0);
}
//Parei finalizando o modulo pessoal, tem algum erro de compilaÃ§Ã£o dentro dele, 
//continuar os outros mÃ³dulos que faltamm
void moodulo (){
    printf("===== MODULO PESSOAL =====\n");
    

}
