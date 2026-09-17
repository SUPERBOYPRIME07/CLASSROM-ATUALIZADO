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



























