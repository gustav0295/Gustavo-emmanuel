# Gustavo-emmanuel
#include <stdio.h>
#include <math.h>

void verificaFatorial(){
    
    int fat, n;
    printf("Insira um valor para o qual deseja calcular seu fatorial: ");
    scanf("%d", &n);
    
    for(fat = 1; n > 1; n = n - 1)
    fat = fat * n;
    
    printf("\nFatorial calculado: %d\n", fat);
    
}

void verificaNumPrimo(int num){
 
 int i, resultado = 0;
 
 for (i = 2; i <= num / 2; i++) {
    if (num % i == 0) {
       resultado++;
       break;
    }
 }
 
 if (resultado == 0)
    printf("O número (%d) digitado é PRIMO \n", num);
 else
    printf("O número (%d) digitado não é PRIMO \n", num);
}

void verificaCadeiaDeNumPrimo(){
    
    int n, i;
    printf("Quantos números deseja verificar: ");
    scanf("%d", &n);
    
    int numeros [n];
    
    for(i=1; i<=n; i++){
        
        printf("Digite o número %d ", i);
        scanf("%d", &numeros[i]);
    }
    
    for(i=1;i<=n; i++){
        
        verificaNumPrimo(numeros[i]);
    }
      
}

void verificaPotencia(){
    
    int exp;
    float  potencia, base;
    
    printf("Digite a base? ");
    scanf("%f", &base);
    printf("Digite o expoente? ");
    scanf("%d", &exp);
    potencia = pow(base,exp);
        
    printf("\nPotencia é %.1f \n", potencia);
}

void verificaRaiz(){
    
    int red;
    float raiz, indice;
    
    printf("Digite o indice da raiz? ");
    scanf("%f", &indice);
    printf("Digite o radicando? ");
    scanf("%d", &red);
    raiz = pow(red,1.0/indice);
        
    printf("\nA Raiz é %.1f \n", raiz);
}

void VerificaAnoBissexto(){
    
    int ano;
    printf("Digite o ano para verificação? ");
    scanf("%d", &ano);
    
    if (ano % 4 == 0 && (ano % 400 == 0 || ano % 100 != 0)) {
    printf("\nAno digitado é bissexto.\n");
  
    }else {
    printf("\nAno digitado não bissexto.\n");
  
  }
    
}

void verificaMediaNota(){
    
    float nota1, nota2, media;
    
    printf("Digite a primeira nota? ");
    scanf("%f", &nota1);
    printf("Digite a segunda nota? ");
    scanf("%f", &nota2);
    
    if(nota1 < 0 || nota1 > 10 || nota2 < 0 || nota2 > 10){
        printf("\nVocê digitou valores não permitidos!\n");
    }else{
        media = (nota1 + nota2)/2;
        printf("\nA média das notas é %.1f\n" , media);
    }
}

void verificaMediaPonderada(){
    
    float nota[3], peso[3], media = 0, totalPeso = 0, totalMedia = 0;
    int i;
    
    for(i=1; i<=3; i++)
    {    
    printf("Digite a %d nota? ", i);
    scanf("%f", &nota[i]);
    
    if(i == 3)
    {
        totalMedia += (nota[i] * 3);
        totalPeso += 3;
    }else{
        totalMedia += (nota[i] * 2);
        totalPeso += 2;
    }
 
    }
    
    media = totalMedia/totalPeso;
    printf("A média ponderada é: %.1f\n", media);
    
    if(media >= 6){
        printf("Aluno APROVADO!\n");
    }else{
        printf("Aluno REPROVADO!\n");
    }
}

void verificaMatricula(){
    
    int mat;
    char nome[100];
    
    printf("Digite seu nome? ");
    scanf("%s", &nome);
    printf("Digite sua matricula? ");
    scanf("%d", &mat);
    printf("\n Nome: %s \n" , nome );
    printf("\nMatricula em Hexa: %x\n", mat);
    
    
}
