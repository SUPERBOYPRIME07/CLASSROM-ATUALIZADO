# CLASSROM-ATUALIZADO

int main()
{
    
    EXERCÍCIO 1
    //ANA,IDADE: 25,ALTURA:1.68,CNH, TRUE//
    
    char Nome[]="Ana";
    int Idade = 18;
    float Altura = 1.68;
    bool possuiCNH = {Idade >=18};
    
    
    printf("Nome %s,Idade %d,Altura %.2fm,possuiCNH%s",
    Nome,Idade,Altura,possuiCNH? "true": "false");
    
   }
    
    EXERCÍCIO 1:2
    
    // //troca de valores//
    
     {    
    int A = 5,B = 10;
    int temp;
    
    
    // //LOGÍCA DA INVERSÃO
    
    temp = A; 
    A = B;    
    B = temp; 
    
    
    printf("A: %d, B: %d\n", A, B); // Saída: A: 10, B: 5
     return 0;
     
     
     EXERCÍCIO 3
     int main()
{

int N1,N2,R;
printf("Informar o valor de N1\n");
scanf("%d", &N1);

printf("Informar o valor de N2\n");
scanf("%d",&N2);

R=N1+N2;

se(R%2==1)
printf("IMPAR");
outro
printf("PAR");
retornar 0; }

EXERCÍCIO 3:2

// Solicita a nota ao usuário
    printf("Digite a nota do aluno (0 a 10): ");
    scanf("%f", &nota);

    // Valida se a nota está dentro do intervalo permitido
    if (nota < 0.0 || nota > 10.0) {
        printf("Nota inválida! Digite um valor entre 0 e 10.\n");
    }
    // Classifica a situação do aluno
    else if (nota > 7.0) {
        printf("Situação: Aprovado\n");
    }
    else if (nota >= 5.0) { // Cobre a faixa de 5.0 até 7.0
        printf("Situação: Recuperação\n");
    }
    else { // Notas menores que 5.0
        printf("Situação: Reprovado\n");
    }

    return 0;


 EXERCÍCIO 4:1
    #include <stdio.h>

int main() {
    int dia;

    // Entrada de dados
    printf("Digite um numero de 1 a 7: ");
    scanf("%d", &dia);

    // Mapeamento e tratamento de erro com switch-case
    switch (dia) {
        case 1:
            printf("Domingo\n");
            break;
        case 2:
            printf("Segunda-feira\n");
            break;
        case 3:
            printf("Terca-feira\n");
            break;
        case 4:
            printf("Quarta-feira\n");
            break;
        case 5:
            printf("Quinta-feira\n");
            break;
        case 6:
            printf("Sexta-feira\n");
            break;
        case 7:
            printf("Sabado\n");
            break;
        default:
            printf("Opcao invalida! Digite um numero de 1 a 7.\n");
            break;
    }

    return 0;
}

	EXERCÍCIO 4:2
	#include <stdio.h>

int main() {
    float num1, num2, resultado;
    char operacao;

    // Entrada dos números e da operação
    printf("Digite o primeiro numero: ");
    scanf("%f", &num1);

    printf("Digite a operacao (+, -, *, /): ");
    // O espaco antes de %c ignora eventuais caracteres de nova linha (\n) do buffer
    scanf(" %c", &operacao);

    printf("Digite o segundo numero: ");
    scanf("%f", &num2);

    // Estrutura switch para processar a operacao
    switch (operacao) {
        case '+':
            resultado = num1 + num2;
            printf("Resultado: %.2f + %.2f = %.2f\n", num1, num2, resultado);
            break;
        case '-':
            resultado = num1 - num2;
            printf("Resultado: %.2f - %.2f = %.2f\n", num1, num2, resultado);
            break;
        case '*':
            resultado = num1 * num2;
            printf("Resultado: %.2f * %.2f = %.2f\n", num1, num2, resultado);
            break;
        case '/':
            // Verificacao de divisao por zero
            if (num2 != 0) {
                resultado = num1 / num2;
                printf("Resultado: %.2f / %.2f = %.2f\n", num1, num2, resultado);
            } else {
                printf("Erro: Divisao por zero nao e permitida!\n");
            }
            break;
        default:
            printf("Erro: Operacao invalida! Use apenas +, -, * ou /.\n");
            break;
    }

    return 0;
}

	EXERCÍCIO 5:2
	#include <stdio.h>

int main() {
    int numero, i;

    // Entrada de dados
    printf("Digite um numero para ver sua tabuada: ");
    scanf("%d", &numero);

    printf("\n--- Tabuada do %d ---\n", numero);

    // Laco for para multiplicar o numero de 1 ate 10
    for (i = 1; i <= 10; i++) {
        printf("%d x %2d = %d\n", numero, i, numero * i);
    }

    return 0;
}
    
    EXERCÍCIO 6:1
    #include <stdio.h>
#include <string.h>

int main() {
    char senha[50];
    const char senha_correta[] = "1234";

    do {
        printf("Digite a senha: ");
        scanf("%s", senha);

        // strcmp retorna 0 quando as duas strings sao iguais
        if (strcmp(senha, senha_correta) != 0) {
            printf("Senha incorreta! Tente novamente.\n\n");
        }
    } while (strcmp(senha, senha_correta) != 0);

    printf("Acesso permitido!\n");

    return 0;
}

	EXERCÍCIO 6:2
	#include <stdio.h>

int main() {
    int contador = 10;

    while (contador >= 0) {
        printf("%d\n", contador);
        contador--; // Subtrai 1 do contador a cada repeticao
    }

    printf("Lançamento!\n");

    return 0;
}



	EXERCÍCIO 7:1
	#include <stdio.h>

int main() {
    int opcao;
    float saldo = 0.0;
    float deposito;

    do {
        printf("=== MENU DO BANCO ===\n");
        printf("1. Ver Saldo\n");
        printf("2. Fazer Depósito\n");
        printf("3. Sair\n");
        printf("Escolha uma opção: ");
        scanf("%d", &opcao);

        switch (opcao) {
            case 1:
                printf("\nSeu saldo atual é: R$ %.2f\n\n", saldo);
                break;
            case 2:
                printf("\nDigite o valor do depósito: R$ ");
                scanf("%f", &deposito);
                if (deposito > 0) {
                    saldo += deposito;
                    printf("Depósito realizado com sucesso!\n\n");
                } else {
                    printf("Valor inválido!\n\n");
                }
                break;
            case 3:
                printf("\nSaindo... Obrigado por usar nosso banco!\n");
                break;
            default:
                printf("\nOpção inválida! Tente novamente.\n\n");
                break;
        }
    } while (opcao != 3);

    return 0;
}



		
        
        
        
        
        
        
        //EXERCÍCIO 7:2
		
		
		#include <stdio.h>





int main() {
    const int numero_secreto = 7;
    int palpite;

    do {
        printf("Tente adivinhar o número secreto: ");
        scanf("%d", &palpite);

        if (palpite != numero_secreto) {
            printf("Número incorreto! Tente novamente.\n\n");
        }
    } while (palpite != numero_secreto);

    printf("\nParabéns! Você acertou o número secreto (%d)!\n", numero_secreto);

    return 0;
}
	
























