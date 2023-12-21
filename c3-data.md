# 1. Resumo
Hoje você vai entender o que são os **tipos** e **variáveis** em C++!

**Tipos** são indicadores pro compilador saber como lidar com aquele valor. Lembra que em C++ você precisa cuidar da memória por conta própria? Muito dessa trabalho o compilador faz automaticamente pra você, e isso não seria possível sem saber o tipo de todos os valores!

**Variáveis** são locais da memória que o compilador cria pra você guardar valores que possuem um **tipo**!

# 2. Tipos Primitivos
Tipos primitivos são os mais fundamentais e básicos da linguagem C++, e são tratados de forma especial pelo compilador. Abaixo vai a lista de alguns tipos primitivos importantes, para ver todos os tipos leia: https://www.tutorialspoint.com/cplusplus/cpp_data_types.htm

- **bool** -> Guarda apenas dois valores: `true` ou `false`. Usado para operações lógicas em C++. Seu tamanho na memória é geralmente de 1 byte apenas.

- **char** -> Tipo numérico mais simples. É um inteiro de 8 bits, ou seja, requer geralmente apenas 1 byte. É geralmente usado para representar caracteres na tabela ASCII.

- **unsigned char** -> adicionar `unsigned` antes do tipo inteiro remove o seu sinal. Então `unsigned char` representa números de `0 até 255`, diferente de `char` que pode conter negativos e representar números de `-127 até 127 ou 0 até 255`.

- **int** -> Tipo numérico mais comum. É um inteiro de 4 bytes de tamanho geralmente, e pode armazenar valores na ordem de `-2147483648 até 2147483647`

- **unsigned int** -> Versão unsigned de int. Armazena valores de `0 até 4294967295`.

- **short int** -> Int curto. É um inteiro de 2 bytes de tamanho geralmente (int 16 bits), e pode armazenar valores na ordem de `-32768 até 32767`. A versão unsigned `unsigned short int` pode armazenar `0 até 65,535`.

- **long int** -> Int longo. É um inteiro de 8 bytes de tamanho geralmente (int 64 bits), e pode armazenar valores na ordem de `-9223372036854775808 até 9223372036854775807`. A versão unsigned `unsigned long int` pode armazenar `0 até 18446744073709551615`.

- **float** -> Tipo de ponto flutuante. É um número de 4 bytes de tamanho geralmente (float 32 bits). Floats são extremamente mais complexos e instáveis que int, então seu uso deve ser feito com cuidado.

- **double** -> Tipo de ponto flutuante de precisão dupla. É um número de 8 bytes de tamanho geralmente (float 64 bits). Guarda valores maiores e de maior precisão que float. Único tipo de float que possui `long double`, de 12 bytes.

# 3. Variáveis
Variáveis são valores guardados na memória que você pode usar de diferentes formas. Por exemplo:
```c++
int x = 10;
```

O compilador vai alocar um espaço na memória pra você, e colocar o valor `10` ali. Então sempre que você usar a variável `x`, o computador vai acessar essa memória e pegar o valor pra você.

```c++
float x = 0.5;
float z = 0.2;
float resultado = x + z;
```

Usando isso podemos operar em valores guardados em variáveis!

# 4. Tipos definidos
C e C++ te dão a habilidade de definir seus próprios tipos. Existem três formas principais e úteis de fazer isso:

## Typedefs
Typedef é a forma mais simples de todas: Ela não cria um tipo, apenas dá outro nome pra um tipo. Exemplo:

![image](https://github.com/deridev/cpp-lore/assets/148335478/bc8c072f-384c-48bf-9244-5571eed4b92a)

## Enumerações
Enumerações (enums) são uma forma de definir números nomeados, geralmente para melhorar a legibilidade do código. Cada variante da enum é efetivamente apenas um número. A primeira variante é 0, a segunda é 1, e assim vai.

![image](https://github.com/deridev/cpp-lore/assets/148335478/c3b00ba3-40e5-45cc-b50f-1981d585af63)

## Struct/classe
São a forma mais poderosa de definir um tipo. `struct` e `class` fazem a mesma coisa, mas `struct` tudo é público por padrão e `class` tudo é privado (explico melhor a diferença quando chegar em orientação a objetos).

![image](https://github.com/deridev/cpp-lore/assets/148335478/1dd80884-743f-4588-b3ea-114435a4ee75)

# 5. Finalização
Esse capítulo foi um grande resumo porque esse é um tópico fundamental e gigante de todas as linguagens de programação! No próximo capítulo explicarei melhor os ponteiros e como C++ trata memória.
