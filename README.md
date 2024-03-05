# Teste

## Questão 1

Observe o trecho de código abaixo:
int INDICE = 13, SOMA = 0, K = 0;
enquanto K < INDICE faça
{
K = K + 1;
SOMA = SOMA + K;
}
imprimir(SOMA);
Ao final do processamento, qual será o valor da variável SOMA?

- Resposta = 91
- Codigo

```javascript
let indice = 13;
let soma = 0;
let k = 0;

while (k < indice) {
  k++;
  soma += k;
}
console.log(soma);
```

## Questão 2

Dado a sequência de Fibonacci, onde se inicia por 0 e 1
e o próximo valor sempre será a soma dos 2 valores anteriores(exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...),
escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci
e retorne uma mensagem avisando se o número informado pertence ou não a sequência.

IMPORTANTE:
Esse número pode ser informado através de qualquer entrada de sua preferência ou pode ser previamente definido no código;

Codigo de resposta:

```javascript
const fibonacci = (num) => {
  let a = 0;
  let b = 1;
  let c;

  while (b < num) {
    c = a + b;
    a = b;
    b = c;
  }

  return b === num ? "pertence" : "não pertence";
};
```

## Questão 3

Descubra a lógica e complete o próximo elemento:

a) 1, 3, 5, 7, \_\_\_

- Resposta = 9
- Logica: adiciona o ultimo elemento do array com um valor impar sequencial

```javascript
const incremento = 2;
const arrayA = [1, 3, 5, 7];
arrayA.push(arrayA[arrayA.length - 1] + incremento);
console.log(arrayA); //Resposta = 9
```

b) 2, 4, 8, 16, 32, 64, \_\_\_\_

- Resposta = 128
- Logica: multiplica o ultimo elemento por 2

```javascript
  const fatorMult = 2;
  const arrayB = [2, 4, 8, 16, 32, 64];
  arrayB.push(arrayB[arrayB.length - 1] \_ fatorMult);
  console.log(arrayB);//Resposta = 128
```

c) 0, 1, 4, 9, 16, 25, 36, \_\_\_\_

- Resposta = 49
- Logica: incrementa os valores com um valor impar sequencial

```javascript
const incrementoC = [1];
const arrayC = [0, 1, 4, 9, 16, 25, 36];
while (incrementoC.length < arrayC.length) {
  incrementoC.push(incrementoC[incrementoC.length - 1] + 2);
}
arrayC.push(arrayC[arrayC.length - 1] + incrementoC[incrementoC.length - 1]);
console.log(arrayC); //Resposta = 36
```

d) 4, 16, 36, 64, \_\_\_\_

- Resposta = 100
- Logica: cada numero da sequencia é o quadrado de uma sequencia de numeros pares

```javascript
const pares = [2];
const arrayD = [4, 16, 36, 64];
while (pares.length < arrayD.length) {
  pares.push(pares[pares.length - 1] + 2);
}
arrayD.push(Math.pow(pares[pares.length - 1] + 2, 2));
console.log(arrayD); //Resposta = 100
```

e) 1, 1, 2, 3, 5, 8, \_\_\_\_

- Resposta = 13
- Logica: soma o ultimo numero da sequencia com o penultimo

```javascript
const arrayE = [1, 1, 2, 3, 5, 8];
arrayE.push(arrayE[arrayE.length - 1] + arrayE[arrayE.length - 2]);
console.log(arrayE); //Resposta = 13
```

f) 2,10, 12, 16, 17, 18, 19, \_\_\_\_

- Resposta = 20
- Logica: continuar a sequencia de somar 1

## Questão 4

- Você está em uma sala com três interruptores, cada um conectado a uma lâmpada em uma sala diferente.
- Você não pode ver as lâmpadas da sala em que está, mas pode ligar e desligar os interruptores quantas vezes quiser. Seu objetivo é descobrir qual interruptor controla qual lâmpada.
- Como você faria para descobrir, usando apenas duas idas até uma das salas das lâmpadas, qual interruptor controla cada lâmpada?

- Resposta:

1. Ligaria um interruptor e aguardaria um tempo
2. Em seguida apagaria o interruptor ligado e ligaria o segundo
3. Iria até uma sala de lampada
   1. Se a lampada estiver quente entao o primeiro interruptor controla a lampada
   2. Se estiver acesa entao o segundo interruptor controla a lampada
   3. Se estiver apagada e fria entao o terceiro interruptor controla a lampada
4. Após a primeira assossiação retorno a sala de interruptores e ativo outro e vou outra sala de lampadas
   1. Se a lampada estiver acessa entao o interruptor controla a lampada
   2. Se estiver apagada entao o interruptor controla a lampada da outra sala.
5. Dessa forma consigo assossiar as lampadas de todas as salas de lampadas e descobrir qual interruptor controla cada uma delas.

## Questão 5

Escreva um programa que inverta os caracteres de um string.
IMPORTANTE:
a) Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código;
b) Evite usar funções prontas, como, por exemplo, reverse;

```javascript
function inverterString(str) {
  let stringInvertida = "";
  for (let i = str.length - 1; i >= 0; i--) {
    stringInvertida += str[i];
  }
  return stringInvertida;
}
console.log(inverterString("teste"));
```
