# Teste-tecnico--Target

1) Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.

### Resposta:

```
function isFibonacci(n) {
    let a = 0, b = 1;
    while (b < n) {
        [a, b] = [b, a + b];
    }
    return b === n || n === 0;
}

const numero = parseInt(prompt("Informe um número: "));
if (isFibonacci(numero)) {
    console.log(`O número ${numero} pertence à sequência de Fibonacci.`);
} else {
    console.log(`O número ${numero} não pertence à sequência de Fibonacci.`);
}
```

#

2) Escreva um programa que verifique, em uma string, a existência da letra ‘a’, seja maiúscula ou minúscula, além de informar a quantidade de vezes em que ela ocorre.

### Resposta:

```
function countA(string) {
    const lowerString = string.toLowerCase();
    let count = 0;
    for (let char of lowerString) {
        if (char === 'a') {
            count++;
        }
    }
    return count;
}

const string = prompt("Informe uma string: ");
const count = countA(string);
console.log(`A letra 'a' aparece ${count} vezes na string.`);
```

#

3) Observe o trecho de código abaixo: int INDICE = 12, SOMA = 0, K = 1; enquanto K < INDICE faça { K = K + 1; SOMA = SOMA + K; } imprimir(SOMA);
Ao final do processamento, qual será o valor da variável SOMA?

### Resposta:
o valor da variável SOMA será 78.

#

4) Descubra a lógica e complete o próximo elemento:
a) 1, 3, 5, 7, ___
b) 2, 4, 8, 16, 32, 64, ____
c) 0, 1, 4, 9, 16, 25, 36, ____
d) 4, 16, 36, 64, ____
e) 1, 1, 2, 3, 5, 8, ____
f) 2,10, 12, 16, 17, 18, 19, ____

### Resposta:

A) 9
B) 128
C) 49
D) 100
E) 13
F) 200

#


5) Você está em uma sala com três interruptores, cada um conectado a uma lâmpada em salas diferentes. Você não pode ver as lâmpadas da sala em que está, mas pode ligar e desligar os interruptores quantas vezes quiser. Seu objetivo é descobrir qual interruptor controla qual lâmpada. Como você faria para descobrir, usando apenas duas idas até uma das salas das lâmpadas, qual interruptor controla cada lâmpada?

### Resposta:
Passo 1, primeiro eu ia liga a lampada e deixa-la esquentar por alguns minutos.
Passo 2, desliga o primeiro inturruptor e ligaria o segundo
Passo 3, Verificaria a sala e veria se a lampada ta quente, acessa ou apagada. Se tiver quente é o prinmeiro interuptor, se tiver acessa é o segundo e se tiver apagada é o terceiro interruptor.
