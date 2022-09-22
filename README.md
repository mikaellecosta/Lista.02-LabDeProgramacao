<p align="center">
  <a href="#questão-1">1</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-2">2</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-3">3</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-4">4</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-5">5</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-6">6</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-7">7</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-8">8</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-9">9</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-10">10</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-11">11</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-12">12</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-13">13</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-14">14</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-15">15</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-16">16</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-17">17</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-18">18</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-19">19</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-20">20</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-21">21</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-22">22</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-23">23</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-24">24</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-25">25</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-26">26</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-27">27</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#questão-28">28</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
</p>

# 📚 Lista 02 - Programação em C
Lista de exercícios submetida na cadeira de Laboratório de Programação.

## Questão 1:
Implemente um programa que tenha como entrada um numero (1-7) que corresponde a um dos dias da semana e imprima na tela o nome do dia correspondente (domingo, segunda, terça, quarta, quinta, sexta, sabado). 
Se o numero lido nao estiver no intervalo 1-7, imprima: “Numero de dia nao valido”. O programa deve permanecer executando ate que o usuario tecle o numero 0. (Utilize obrigatoriamente teste no inıcio).
``` c
#include <stdio.h>

int main() {
  int n;
  printf("Digite um número de 1-7: ");
  scanf("%d",&n);
  
  while (n < 1 && n > 7) {
    if (n == 0){
      break;
    }
    printf("Número de dia não válido.");
    return main();
  }

  switch(n){
    case 1:
    printf("Segunda");
    return main();

    case 2:
    printf("Terça");
    return main();

    case 3:
    printf("Quarta");
    return main();

    case 4:
    printf("Quinta");
    return main();

    case 5:
    printf("Sexta");
    return main();

    case 6:
    printf("Sábado");
    return main();

    case 7:
    printf("Domingo");
    return main();
  }
  return 0;
}
``` 

## Questão 2:
Refaça o programa da Questao 1, utilizando a estrutura de repeticao com teste no final.
``` c
#include <stdio.h>

int main() {
  int n;
  printf("Digite um número de 1-7: ");
  scanf("%d",&n);

  switch(n){
    case 1:
    printf("Segunda\n");
    return main();

    case 2:
    printf("Terça\n");
    return main();

    case 3:
    printf("Quarta\n");
    return main();

    case 4:
    printf("Quinta\n");
    return main();

    case 5:
    printf("Sexta\n");
    return main();

    case 6:
    printf("Sábado\n");
    return main();

    case 7:
    printf("Domingo\n");
    return main();

    case 0:
    break;
  }
  
  do {
    if (n ==0){
      break;
    }
    printf("Número de dia não válido.\n");
    return main();
  } while (n < 1 && n > 7);  
    return 0
  }

``` 

## Questão 3:
Escreva um programa que leia um numero inteiro e positivo F e calcule o fatorial deste numero.
``` c
#include <stdio.h>

int main() {
  int f, fat=1;
  printf("Número: ");
  scanf("%d",&f);

  for (int i = 1; f > i ; f--){
    fat = f * fat;  
  } 
  printf("Fatorial: %d", fat);
  return 0;
}
``` 

## Questão 4:
Implementar um programa para resolver o seguinte problema: Jose tem 150 centımetros e cresce 2 centımetros por ano. 
O Pedro tem 110 centımetros e cresce 3 centımetros por ano. 
- Em quantos anos Pedro sera maior que Jose?
``` c
#include <stdio.h>

int main() {
  int jose = 150;
  int pedro = 110;
  
  for (int i = 1; ; i++){
    jose = jose + 2;
    pedro = pedro + 3;
    if (pedro > jose){
      printf("Pedro = %d. José = %d. %d anos", pedro,jose,i);
      break;
    }
  }
  
  return 0;
}
``` 

## Questão 5:
Fazer um programa que receba um valor n no teclado e determine o maior e o menor termo fornecido. 
A condicao de termino do programa é quando o usuario digitar zero
``` c
#include <stdio.h>

int main() {
  int i, m[20],menor=0,maior=0; 
  
  for(i = 0; ; i++){
    
  printf("Número %d: ",i);
  scanf("%d",&m[i]);
    
  if (m[i] == 0){
    break;
  }   
    
  if(i == 0){maior=m[i]; menor=m[i];}
      if(m[i] > maior){
        maior = m[i];
      }
      else{
        if(m[i]<menor){
            menor=m[i];
        }
      }
      
 }
printf("Maior número: %d. Menor número: %d",maior, menor);
}
``` 

## Questão 6:
Escreva um programa que transforme o computador numa urna eletronica para eleiçao para presidente de um certo pais, as quais concorrem os candidatos: 5)Paulo e 7)Renata.
Cada voto deve ser dado pelo numero do candidato, permitindo-se ainda o voto:
- 0 para voto em branco. Qualquer voto diferente dos ja citados  é considerado nulo; em qualquer situaçao, o eleitor deve ser consultado quanto a confirmacao do seu voto. No final da eleicao o programa deve emitir um relatorio contendo as porcentagens de votaçao de cada candidato, votos em branco, votos nulos e o candidato eleito. 
- Obs: O codigo para finalizar a urna (votaçao) é o usuario digitar algum numero negativo.
``` c
#include <stdio.h>
#include <stdlib.h>

int main() {
  int voto, branco=0, nulo=0, paulo=0, renata=0;
  float total;
  char conf;
  
  for(int i = 0; ; i++){
  
  printf("Seu voto: ");
  scanf("%d",&voto);
    
  if (voto < 0){
    break;
  }

  switch(voto){
    case 7:
    printf("Deseja votar em renata? s ou n?");
    scanf("%s",&conf);
    if (conf=='s'){
      renata = renata + 1;
    } else {
      continue;
    }
    break;

    case 5:
    printf("Deseja votar em paulo? s ou n?");
    scanf("%s",&conf);
    if (conf=='s'){
      paulo = paulo + 1;
    } else {
      continue;
    }
    break;

    case 0:
    printf("Deseja votar branco? s ou n?");
    scanf("%s",&conf);
    if (conf=='s'){
      branco = branco + 1;
    } else {
      continue;
    }

    default:
    printf("Deseja votar nulo? s ou n?");
    scanf("%s",&conf);
    if (conf=='s'){
      nulo = nulo + 1;
    } else {
      continue;
    }
  }
}

total = renata + paulo + branco + nulo;
printf("Total de votos: %0.f\n",total);
  
printf("Porcentagem de votação:\n");
printf("Paulo: %0.1f %%. Renata: %0.1f %%. Branco: %0.1f %%. Nulo: %0.1f %%", paulo/total*100, renata/total*100, branco/total*100, nulo/total*100);
  
}
``` 

## Questão 7:
Escreva um programa para ler 2 valores e imprimir o resultado da divisao do primeiro pelo segundo. 
- Obs: o programa deve validar a leitura do segundo valor (que nao deve ser nulo). Enquanto for fornecido um valor nulo a leitura deve ser repetida.
``` c
#include <stdio.h>
#include <stdlib.h>
int main() {
  float a,b;

  printf("Número 1: ");
  scanf("%f",&a);

  printf("Número 2: ");
  scanf("%f",&b);
  
  system ("clear");
  
  while (a <= 0 || b <= 0){
    printf("Número menor ou igual a 0! Tente novamente.\n");
    return main ();
  }

printf("Divisão do 1° pelo 2°: %0.1f", a/b);
  
  return 0;
}
``` 

## Questão 8:
Uma loja vende seus produtos no sistema entrada mais duas prestaçoes, sendo a entrada maior do que ou igual as duas prestaçoes; estas devem ser iguais, inteiras e as maiores possıveis.
Escreva um programa que receba o valor da mercadoria e forneça o valor da entrada e das duas prestaçoes, de acordo com as regras acima.
``` c
#include <stdio.h>
#include <math.h>

int main(void) {
  float entrada, valor;
  int presta, teste;
  
  printf("Valor da mercadoria: ");
  scanf("%f",&valor);

  teste = valor;
  
  if (valor == teste){
    printf ("Inteiro\n");
    presta = teste / 3;
    entrada = (teste % 3) + presta;
  } else {
    printf("Decimal\n");
    presta = valor / 3;
    entrada = fmod(valor, 3) + presta;
  }
  printf("Entrada = %0.1f | Presta = %d", entrada, presta);
  return 0;
}
``` 

## Questão 9:
A serie de Fibonacci é formada pela seguinte sequencia: 1, 1, 2, 3, 5, 8, 13, 21, 34, 55... etc. 
Escreva um algoritmo que gere a serie de Fibonacci ate o vigesimo termo.
``` c
#include <stdio.h>
  int fibo [20];
 
  int main() {
    for (int i = 2; i < 20; i++){
      fibo[0] = 0;
      fibo[1] = 1;
      
      fibo [i] = fibo[i-1] + fibo [i-2];
      printf("%d\n",fibo[i]);
  }
}
``` 

## Questão 10:
Elabore um programa que apresente os quadrados dos numeros inteiros multiplos de 4 existentes na faixa de valores de 15 a 90.
``` c
#include <stdio.h>
#include <math.h>
  
int main() {
  int x, num=4, tab;
  
  for(int i = 1; ; i++){
    tab = num * i;
    x = pow(tab, 2);
    
    if (x >= 15 && x <=90){
      printf("%d\n",x);
    } else{
       break;
    }
  }
   }
``` 

## Questão 11:
Refaça a questaao 11, considerando que os limites da faixa (A e B) sejam fornecidos pelo usu ́ario. O programa deve funcionar tanto para A > B quanto para B > A.
``` c
#include <stdio.h>
#include <math.h>

int main() {
  int menor,maior, num=4, tab, a,b, inter;
  
  printf("Número inicial: ");
  scanf("%d",&a);
  printf("Número final: ");
  scanf("%d",&b);

  a > b? maior = a, menor = b: (menor = a, maior = b);
  
  for(int i = 1; ; i++){
    tab = num * i;
    inter = pow(tab, 2);
    
    if (inter >= menor && inter <= maior){
      printf("%d\n",inter);
    } else{
       break;
    }
  }
}
``` 

## Questão 12:
Elaborar um programa que mostre os resultados da tabuada de um numero inteiro qualquer, a qual deve ser apresentada de acordo com sua forma tradicional.
``` c
#include <stdio.h>

int main() {
  int num, tab;
  printf("Qual número deseja receber a tabuada? ");
  scanf("%d",&num);

  for (int i = 1; i <= 10; i++){
    tab = num * i;
    printf("%d * %d = %d\n", num, i, tab);
  }
}
``` 

## Questão 13:
Elabore um programa que calcule o somatorio de todos os numeros pares pertencentes a faixa A,B especificada pelo usuario. 
O programa deve funcionar tanto para A > B quanto para B > A.
``` c
#include <stdio.h>

int main() {
  int a, b, menor, maior, soma=0;
  printf("Número inicial: ");
  scanf("%d",&a);
  printf("Número final: ");
  scanf("%d",&b);

  a > b? maior = a, menor = b: (menor = a, maior = b);
  
  for(int i = 1; ; i++){
    if (i % 2 == 0){
      soma = soma + i;
    if (i >= menor && i <= maior){
      printf("%d + %d = %d\n",i, soma-i,soma);
    } else {
      break;
    }
      }
    }
  }
``` 

## Questão 14:
Elabore um programa que apresente a quantidade de numeros divisıveis por 3 pertencentes a faixa A,B especificada pelo usuario. 
O programa deve funcionar tanto para A > B quanto para B > A.
``` c
#include <stdio.h>

int main() {
  int a, b, menor, maior, cout=0;
  printf("Número inicial: ");
  scanf("%d",&a);
  printf("Número final: ");
  scanf("%d",&b);
  
  a > b? maior = a, menor = b: (menor = a, maior = b);

  for (int i = 1; ; i++){
    
    if (i % 3 == 0){
        cout = cout + 1;
      if (i >= menor && i <= maior){
        printf("%d número %% por 3 = %d\n",cout,i);
        }
      else { 
        break;
        }
      }
    }
  }
``` 

## Questão 15:
Elaborar um programa que apresente os resultados das potencias do valor de base 3, elevado a um expoente que varie do valor 0 a 7.
``` c
#include <stdio.h>
#include <math.h>
#define BASE 3

int main() {
  int valor;
  for (int i = 0; i < 7; i++){
    valor = pow(BASE,i);
     printf("%d ^ %d = %d\n", BASE, i, valor);
  }
 }
``` 

## Questão 16:
Escreva um programa que apresente o somatorio de todos os numeros divisıveis por 3 pertencentes ao intervalo [0,100] e o somatorio de todos os numeros divisıveis por 5 pertencentes ao intervalo ]100,200].
- Obs: Utilize apenas um laco de repeticao.
``` c
#include <stdio.h>

int main() {
  int soma3=0, soma5=0;
  for (int i = 0; i<=200; i++){
    if (i < 100 && i % 3 == 0){
        soma3 += i;
      }
     else if (i > 100 && i<=200){
        if (i % 5 == 0){
          soma5 += i;
      }
    }
  }
  printf("Soma dos números %% por 3 [100, 200] = %d\n", soma3);
  printf("Soma dos números %% por 5 ]0, 200] = %d\n", soma5);
}
``` 

## Questão 17:
Elaborar um programa que apresente os valores de conversao de graus Celsius em graus Fahrenheit, de 10 em 10 graus, iniciando a contagem em dez graus Celsius e finalizando em cem graus Celsius. 
O programa deve apresentar os valores das duas temperaturas.
``` c
#include <stdio.h>

int main() {
  float conv;
  for(int i = 10; i <= 100; i++){
    if (i % 10 == 0){
      conv = (1.8 * i) + 32;
      printf("Celcius %i -- Fahrenheit %0.1f\n",i,conv);
    }
  }
}
``` 

## Questão 18:
Escrever um programa que calcule e apresente o somatorio do numero de graos de trigo que se pode obter num tabuleiro de xadrez, obedecendo a seguinte regra: 
- colocar um grao de trigo no primeiro quadro e nos quadros seguintes o dobro do quadro anterior. Ou seja, no primeiro quadro coloca-se um grao, no segundo quadro
- colocam-se dois graos (tendo neste momento tres graos), no terceiro quadro colocam-se quatro graos (tendo neste momento sete graos), no quarto quadro colocam-se oito graos (tendo-se entao quinze graos) ate atingir o sexagesimo quarto quadro. 
``` c
#include <stdio.h>
#include <stdlib.h>
#include <stdio.h>
#include <unistd.h>

int main(void) {
  unsigned long int graos[66], soma;
  for (int i = 2; i < 66; i++){
    graos[1] = 1;
    graos[i] = graos[i-1] * 2;
    soma += graos[i];
    printf("%d° quadro = %lu grãos\n", i-1, graos[i-1]);
  }
  sleep(5);
  system("clear");
  printf("Somatório = %lu grãos", soma);
}
``` 

## Questão 19:
Elaborar um programa que apresente a media aritmetica dos numeros inteiros existentes entre uma faixa especificada pelo usuario.
``` c
#include <stdio.h>
#include <string.h> 
int main() {
  int a, b, menor, maior, soma=0, cout=0;
  float media;
  printf("Número inicial: ");
  scanf("%d",&a);
  printf("Número final: ");
  scanf("%d",&b);

  a > b? maior = a, menor = b: (maior = b, menor = a);

  for (int i = menor; i <= maior; i++){
    soma += i;
    cout = (maior-menor) +1 ;
    media = soma / (float) cout; 
}
   printf("Soma = %d\n", soma);
   printf("Média = %0.1f\n", media);
  }
``` 

## Questão 20:
Construir um programa que apresente como resultado o fatorial dos valores ımpares situados na faixa numero de 1 a 10.
``` c
#include <stdio.h>

int main(){
int fatorial, i=1;

for(i = 1; i < 11; i++){
    if(i % 2){
      fatorial = 1;
      for(int j = 1; j <= i; j++){
        fatorial = fatorial * j;
       } 
      printf("Fatorial de %d = %d\n",i,fatorial);
    }
 }   
  }
``` 

## Questão 21:
Um palındromo é um numero, ou frase textual, que pode ser lido da mesma forma da esquerda para a direita e vice-versa. 
Escreva um programa que leia um inteiro de cinco dıgitos e determine se ele é ou nao um palındromo. 
``` c
#include <stdio.h>

int main() {
  unsigned int num[5];
  
  for (int i = 0; i < 5; i++){
    printf("%d° digito: ",i+1);
    scanf("%d",&num[i]);
  }
  for (int i = 0; i < 5; i++){
    if (num[0] == num[4]){
      if (num[1] == num[3]){
        printf("\nÉ um palindromo");
        break;
      } 
      }
    else{
        printf("\nNão é um palindromo");
        break;
    }
  }
  return 0;
}
``` 

## Questão 22:
Escreva um programa que leia um numero inteiro e determine e imprima quantos dıgitos no inteiro sao algarismos 7.
``` c
#include <stdio.h>
#include <stdlib.h>

int main() {
  int n, v[10],count=0;
  printf("Número: ");
  scanf("%d",&n);
  do {
    n /= 10;
    ++count;
  } while (n != 0);

  for (int i = 0; i < count; i++){
    printf("Digito %d: ",i);
    scanf("%d",&v[i]);
  }
  for (int i = 0; i < count; i++){
    if(v[i]==7){
      printf("%d = 7 \n",v[i]);
      }
    else{
      printf("%d != 7\n",v[i]);
    }
    }
}
``` 

## Questão 23:
Escreva um programa que mostre a diferenca entre pre-incrementar e pos-incrementar usando o operador.
``` c
#include <stdio.h>

int main() {
 for (int i = 10; i > 1;){
     printf("%d",i--);
 }
    printf("\n");
  
    for (int i = 10; i > 1;){
     printf("%d",--i);
 }
}
``` 

## Questão 24:
Um triangulo retangulo pode ter lados que sao valores inteiros. O conjunto de tres valores inteiros para os lados de um triangulo retangulo  é chamado de tripla de Pitagoras. Esses tres lados precisam satisfazer o relacionamento de que a soma do quadrado de dois catetos  é igual ao quadrado da hipotenusa. 
Ache todas as triplas de Pitagoras nao superiores a 500 para cateto1, cateto2 e hipotenusa.
``` c
#include <stdio.h>
#include <math.h>
#define LIM 500

int mdc(int x, int y){
  int resto;
  do{
    resto = x % y;
    x = y;
    y = resto;
  } while(resto != 0);
  return x;
}

int main(void){
  int mdc1, mdc2, c1, c2, save;
  float hipo;

  for(c1 = 1; c1 <= LIM; c1++){
    for(c2 = c1; c2 <= LIM; c2++){
      hipo = sqrt(pow(c1, 2) + pow(c2, 2));
      save = hipo;
      if(save == hipo && save <= LIM){
        mdc1 = mdc(c1, c2);
        mdc2 = mdc(hipo, mdc1);
        if(mdc1 == 1 && mdc2 == 1){
          printf("A: %d\tB: %d\tC: %d\n", c1, c2, save);
        }
      }
    }
  }
  return 0;
}
``` 

## Questão 25:
Calcule o valor de π a partir da série infinita:
π = 4 − 4/3 + 4/5 + 4/7 + 4/9 + 4/11 ...
Imprima uma tabela que mostre o valor de π aproximado por um termo dessa s ́erie, e depois por dois
termos, três termos, e assim por diante.
``` c
#include <stdlib.h>
#include <stdio.h>

int main(void){
int i = 1;
double pi = 0, aux1 = 1;
  for(i = 1;i <= 119;i++){
    if(i%2 !=0)
      pi = pi + 4/aux1;
    else
      pi = pi - 4/aux1;
      aux1 = aux1+2;
  printf("%.10f\n",pi);
        }
printf("\nValor de pi em 119x = %.10f",pi);
return 0;
}
``` 

## Questão 26:
Escreva um programa que imprima uma tabela dos equivalentes binário, octal e hexadecimal dos
números decimais no intervalo de 1 a 256.
``` c
#include <stdio.h>

void binario(n){ 
  if(n == 0)
    printf("%d",n);
  else{
    binario(n/2);
    printf("%d", n % 2);     
      }
}
  
int main() {

   printf("NUMERO \t  BINARIO\t  HEXA \t OCTAL\t\n");
   
  for (int i = 1; i <= 256; i++){
    printf(" %d\t\t\t",i);
    binario(i);
    printf("\t\t%x\t\t",i);
    printf("%o\n",i);
}
  }
``` 

## Questão 27:
Escreva um programa que receba varios numeros inteiros (em uma estrutura de laço) e apresente o produto do maior pelo menor numero apresentado. 
- A condicao de saıda do laco é o usuario digitar um numero negativo e par.
- Obs: Nao utilize vetores.
``` c
#include <stdio.h>

int main() {
  int n,i;
  int maior=0, menor=0;
  for (i = 0; ; i++){
    printf("Número: ");
    scanf("%d",&n);
    
    if (n < 0 && n % 2 == 0){
      break;
    }
    
    if(i == 0){maior=n; menor=n;}
    if (n > maior && n > 0){
      maior = n;
            }
    else{
      if(n<menor){
        menor=n;
        }
      }
  }
    printf("Número menor -> %d\nNúmero maior -> %d",menor,maior);
  return 0;
  }
``` 

## Questão 28:
Escreva um programa que receba dois valores num ́ericos X e Y (unsigned char) e esconda todos os bits de X em cada um dos bits menos significativos dos 4 elementos imediatamente anteriores e posteriores a Y. 
- Obs: Não utilizar valores para Y menores que 5.
``` c
#include <stdio.h>
#include <math.h>

int main(void){
  char x, y;
  int pos=-4, termo, concat, xbit;

  printf("Valor de X: ");
  scanf("%hhu", &x);
  printf("Valor de Y: ");
  scanf("%hhu", &y);

  if (y < 4){
    printf("Valor de Y < 4. Insira outro número.");
    scanf("%hhu", &y);
  }

  for(int i = 0; i < 8; i++){
    termo = y + pos;
    
    if(termo == y){
      pos++;
      i--;
      continue;
    }
    
    if((x & (int)pow(2, i)) > 0)
      xbit = 1;
    else
      xbit = 0;
    
    if((termo % 2) < xbit)
      concat = termo + 1;
    else if((termo % 2) > xbit)
      concat = termo - 1;
    else
      concat = termo;
    
    printf("número com base em Y = %d --- após bit de X = %d\n", termo, concat);
    pos++;
  }
  return 0; 
  }
``` 

