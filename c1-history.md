# 1. Contexto
Nascido em 1983, **C++** é uma linguagem de programação desenvolvida por Bjarne Stroustrup em uma empresa chamada Bell Labs, como uma "extensão" da linguagem C. O objetivo de Stroustrup era melhorar uma versão do núcleo Unix, mas ele queria usar funcionalidades mais "modernas" (para a época), de uma linguagem chamada **Simula 67**, que contava com orientação a objetos, funcionalidade essa que C não possuia.

Pra comparação, hello world em Simula 67 era escrito assim:

<img src="https://slideplayer.com.br/slide/353999/2/images/34/Simula67+%28exemplo%29+Begin+while+1+%3D+1+do+begin.jpg" width=480 height=360>


Inicialmente, C++ foi chamado de **C With Classes**, mas foi renomeado para C++. Sua maior vantagem sobre C na época era suportar orientação a objetos (classes) e generics. Hoje em dia, C++ é uma importante linguagem utilizada em muitas área, desde criação de jogos, sistemas operacionais, servidores e muitos outros. C++ é historicamente importante por ter influenciado diversas outras linguagens de programação como Ada, C#, Java, PHP e **Rust**.

Com o tempo, C++ recebeu diversas outras funcionalidades, que para não quebrar código antigo, sofreram diversas gambiarras e receberam regras que com o tempo tornaram C++ uma linguagem extremamente poluída e confusa. Eu chego nisso mais tarde.

# 2. Como funciona?
C++ é uma linguagem **compilada**. Mas o que isso significa?

Existem várias formas como uma linguagem de programação pode funcionar, mas de longe as duas formas mais populares são linguagens **compiladas** ou **interpretadas**.

## Interpretada:
Uma linguagem interpretada é aquela em que um programa externo (chamado de **interpretador**) lê o código, e então em tempo real executa cada instrução. As vantagens de uma linguagem interpretada são a **simplicidade**, porque todo a complexidade é feita pelo interpretador, então código interpretado não precisa se preocupar com coisas como memória, tipos, e outros detalhes. Por outro lado, como cada instrução do código requer trabalho extra do interpretador, linguagens interpretadas são geralmente mais lentas que linguagens compiladas como C++. Algumas linguagens usam técnicas para aumentar a velocidade (como LUA, que usa "JIT", uma mistura de compilação e interpretação), e outras como Python não fazem nenhuma otimização especial e por isso são até **80x mais lentas que C/C++**.

Exemplo de código Python (interpretada):
```py
x = 15; # Cria uma variável chamada "x" com o valor 15 na memória.
x = "Olá"; # Muda o tipo e valor da variável completamente. Código válido em Python por possuir tipos dinâmicos!
print(x); # Mostra o valor de x no terminal 
```

## Compilada:
Linguagens compiladas, por outro lado, são muito mais complicadas e complexas. Uma linguagem compilada é aquela em que um programa externo (chamado de **compilador**) lê o código, e então converte o código todo para **Assembly**. Assembly é uma linguagem de baixo nível, ou seja, muito mais perto do que o computador entende do que da linguagem que humanos entendem. Assembly é tão baixo nível que cada instrução é praticamente binário (100101001100) puro.

Exemplo de código assembly (X86 Intel):
```asm
;; Programa Hello World
section .text
global _start

_start:
        mov     edx, len                             ; Tamanho da mensagem
        mov     ecx, msg                             ; Mensagem a ser escrita
        mov     ebx, 1                               ; Descritor de arquivo (stdout)
        mov     eax, 4                               ; Código do syscall (4 = sys_write, para escrever no terminal)
        int     0x80                                ; Enviar o syscall pro Kernel

        mov     eax, 1                               ; Código do syscall (1 = sys_exit)
        int     0x80                                ; Enviar o syscall pro Kernel

section     .data
        msg     db  'Hello, world!',0xa                 ; Nossa string
        len     equ $ - msg                             ; Tamanho da string
```

Se você não entendeu nada não precisa se preocupar. Assembly é um nível abaixo de C++, então praticamente nunca há a necessidade de diretamente usar Assembly.
Voltando: o compilador lê o código C++ e converte pra o equivalente na monstruosidade que é o Assembly, e então o código assembly é convertido para um executável que o computador executa diretamente.

Como não há nenhum programa externo executando nosso código, já que nosso código é convertido diretamente pra código de máquina otimizado que o computador lê diretamente na velocidade da luz, linguagens compiladas são **extremamente mais rápidas** que linguagens interpretadas. A desvantagem é a complexidade, visto que como código C++ vai ser diretamente convertido pra binário, isso quer dizer que é nossa responsabilidade como programador cuidar da memória do programa e cuidar para não explodir o computador.

O compilador faz mais do que apenas isso, mas vou entrar nisso em capítulos futuros.

# Conclusão
Agora que eu já expliquei o porquê C++ existe e porquê ele é como é, no próximo capítulo vou mostrar como compilar e executar um programa simples em C++.

[Capítulo 2 - Olá Mundo](c2-helloworld.md)
