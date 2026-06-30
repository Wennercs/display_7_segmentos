---
title: "Projeto Display de 7 Segmentos"
author: "Wenner Cruz"
date: "`r Sys.Date()`"
output:
  github_document:
    toc: true
    toc_depth: 3
---

# Display de 7 Segmentos utilizando Logisim

## Introdução

Este projeto foi desenvolvido utilizando o **Logisim Evolution** com o objetivo de implementar um circuito digital capaz de controlar um **display de sete segmentos** a partir de uma entrada binária de **3 bits**.

O circuito converte automaticamente os valores binários em sua representação decimal correspondente, exibindo os números de **0 a 7** no display. Toda a lógica foi implementada utilizando circuitos combinacionais, sem o uso de componentes programáveis ou memória.

---

# Objetivos

Este projeto possui os seguintes objetivos:

- Compreender o funcionamento de circuitos digitais combinacionais.
- Aplicar conceitos de Álgebra Booleana.
- Desenvolver um decodificador para display de sete segmentos.
- Simular circuitos digitais utilizando o Logisim Evolution.
- Representar números decimais através de sinais binários.

---

# Ferramentas Utilizadas

- Logisim Evolution
- Portas Lógicas
  - AND
  - OR
  - NOT
  - XOR (quando necessário)
- Display de Sete Segmentos
- Pinos de Entrada
- Pinos de Saída

---

# Fundamentação Teórica

Os computadores trabalham internamente utilizando o sistema binário, composto apenas pelos dígitos **0** e **1**.

Neste projeto são utilizados **3 bits**, permitindo representar um total de oito combinações diferentes.

O número máximo de combinações possíveis é dado por:

```
2³ = 8
```

Assim, os valores possíveis são:

| Decimal | Binário |
|---------:|:--------:|
|0|000|
|1|001|
|2|010|
|3|011|
|4|100|
|5|101|
|6|110|
|7|111|

Cada uma dessas combinações é convertida pelo circuito em sinais elétricos responsáveis por acionar os segmentos do display.

---

# Funcionamento do Display

O display utilizado possui sete segmentos identificados pelas letras:

```
     A
   -----
F |     | B
  |  G  |
   -----
E |     | C
  |     |
   -----
     D
```

Cada número é formado acendendo determinados segmentos.

Exemplo:

| Número | Segmentos Ligados |
|---------|------------------|
|0|A B C D E F|
|1|B C|
|2|A B D E G|
|3|A B C D G|
|4|B C F G|
|5|A C D F G|
|6|A C D E F G|
|7|A B C|

---

# Entradas do Circuito

O circuito possui três entradas binárias.

| Entrada | Descrição |
|----------|-----------|
|A|Bit mais significativo (MSB)|
|B|Bit intermediário|
|C|Bit menos significativo (LSB)|

Esses três bits determinam qual número será exibido.

---

# Tabela Verdade

| Decimal | A | B | C |
|---------:|:-:|:-:|:-:|
|0|0|0|0|
|1|0|0|1|
|2|0|1|0|
|3|0|1|1|
|4|1|0|0|
|5|1|0|1|
|6|1|1|0|
|7|1|1|1|

---

# Implementação

O circuito foi desenvolvido utilizando apenas lógica combinacional.

Cada segmento do display possui uma expressão booleana própria que determina quando deve permanecer aceso.

A implementação consiste em analisar todas as combinações possíveis das entradas e gerar os sinais corretos para cada segmento.

Essa abordagem elimina a necessidade de programação, utilizando exclusivamente portas lógicas.

---

# Circuito
 

```markdown
*[Circuito](imagens/circuito.png)* 
```

---

# Simulação

Durante a simulação é possível alterar o valor das entradas A, B e C.

O circuito atualiza automaticamente o display conforme a combinação selecionada.

Exemplo:

| Entrada | Número exibido |
|---------|----------------|
|000|0|
|001|1|
|010|2|
|011|3|
|100|4|
|101|5|
|110|6|
|111|7|

---
# Como Executar

1. Execute o **Logisim**.

2. Abra o arquivo

```
circuito.circ
```

3. Modifique as entradas binárias.

4. Observe a alteração do display.

---

# Resultados Obtidos

O circuito apresentou funcionamento correto para todas as oito combinações possíveis das entradas binárias.

Os números de **0 a 7** foram exibidos corretamente no display de sete segmentos, validando a lógica implementada.

---

# Possíveis Melhorias

Algumas melhorias que podem ser implementadas futuramente incluem:

- Exibição de números hexadecimais.
- Utilização de multiplexadores.
- Implementação utilizando ROM.
- Implementação utilizando PLA.
- Adição de contador automático.
- Integração com clock.

---

# Conclusão

O desenvolvimento deste projeto permitiu aplicar conceitos fundamentais da eletrônica digital e da Álgebra Booleana por meio da construção de um circuito combinacional para controle de um display de sete segmentos.

A utilização de apenas três bits de entrada simplificou a implementação e possibilitou representar corretamente os números de **0 a 7**, demonstrando na prática o processo de conversão entre o sistema binário e sua representação visual.

Além de reforçar o entendimento sobre portas lógicas e circuitos combinacionais, o projeto evidenciou a importância da organização e da simplificação das funções booleanas para o desenvolvimento de sistemas digitais eficientes.

---

