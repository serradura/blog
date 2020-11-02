---
title: "[Em construção] Introdução a testes automatizados (TDD) com Ruby"
hidden: true
last_modified_at: 2020-11-01T23:58:00-03:00
categories:
  - Blog
tags:
  - ruby
  - tdd
---

Olá, se tem uma coisa que pessoas e equipes de auto desempenho possuem é **confiança**. Sendo que em desenvolvimento de software é muito importante ter certeza que o teu código funciona na medida que o mesmo é modificado. A técnica mais comum e intuitiva para aumentar confiança na medida que se promove mudanças é a escrita de roteiros de testes, que serão realizados manualmente. Ou seja, um ser humano, executará uma série de ações em sequência afim de avaliar se os resultados esperados foram obtidos.

Testes realizados por seres humanos são válidos, mas é um processo lento e caro se comparado há um processo automatizado. Por conta disso, nossa industria desenvolveu técnicas e ferramentas que permitem que boa parte desse processo seja o mais automático possível.

Para me auxiliar a introduzir o tema testes automatizados, irei abordar o uso de TDD (**T**est **D**riven **D**evelopment), traduzindo: **desenvolvimento orientado a testes**. Que é uma técnica utilizada para escrever apenas o código necessário para atender um determinado requisito, ou seja você primeiro escreve o teste e então o código necessário para fazer o mesmo passar.

Esse post será dívidido em duas partes, a primeira: Abordará o que é e por que utilizar TDD, e a última: Te ensinará como usar na medida que te ensina a como escrever a sua própria lib de testes 💪.

## O que é TDD?

Tdd é um ciclo de desenvolvimento no qual você primeiro escreve um teste antes de escrever a implementação do seu código. Sendo essas as suas etapas:

### Primeiro passo: <span style="font-weight: normal;">escrever um teste que irá falhar</span>.

{% include figure image_path="/assets/images/3-tdd/1_Red.png" alt="Tdd: Red = Teste falhando" caption="Tdd: Red = Teste falhando." %}

Primeiro, você tem o <span style="color: red;">*red mode*</span>, no qual é escrito um teste que falha. Nele você descreverá o comportamento que o código deverá ter. Seja uma série de ações ou apenas uma parte/unidade do comportamento que se é esperado.

### Próximo passo: <span style="font-weight: normal;">fazer o teste passar</span>.

{% include figure image_path="/assets/images/3-tdd/2_Red-Green.png" alt="Tdd: Red + Green = Fazer o teste passar com o mínimo de código necessário" caption="Tdd: Red + Green = Fazer o teste passar com o mínimo de código necessário." %}

Nessa etapa, você escreverá apenas a quantidade necessária para fazer o teste ficar verde, ou seja, entrar no <span style="color: green;">*green mode*</span>.

### Próximo passo: <span style="font-weight: normal;">refatorar o código produzido</span>.

{% include figure image_path="/assets/images/3-tdd/3_Red-Green-Refactor.png" alt="Tdd: Red + Green + Refactor = Refinar a estrutura do código sem quebrar o comportamento." caption="Tdd: Red + Green + Refactor = Refinar a estrutura do código sem quebrar o comportamento." %}

Nessa etapa, se torna possível <span style="color: blue;">refinar o código</span> ao mesmo tempo que se tem garantias de que o mesmo funciona. Ou seja, o teste tem que continuar verde.

> <span style="font-style: normal;">**Dica:** Só refine o código se for realmente necessário! 🙂</span>

**Significado de refatoração**: É o processo de melhorar a estrutura de um código/sistema enquanto se preserva o comportamento existente.

### Por fim: <span style="font-weight: normal;">repitir o ciclo</span>.

{% include figure image_path="/assets/images/3-tdd/4_Red-Green-Refactor-Cycle.png" alt="Tdd: Red + Green + Refactor (Cycle) = Repita o ciclo para a próxima implementação." caption="Tdd: Red + Green + Refactor (Cycle) = Repita o ciclo para a próxima implementação." %}

Repita o ciclo para a próxima funcionalidade/comportamento ser entregue.
1. Escreva um <a style="color: red;" href="#primeiro-passo-escrever-um-teste-que-irá-falhar">teste que falha</a>.
2. Faça o <a style="color: green;" href="#próximo-passo-fazer-o-teste-passar">teste passar</a>.
3. <a style="color: blue;" href="#próximo-passo-refatorar-o-código-produzido">Refatore o código</a> sempre que necessário.

A idéia é repetir esse ciclo para cada funcionalidade que o sistema recebar, até que ele seja considerado finalizado.

## Por que fazer TDD?

Ao fazer isso você você e sua equipe obterá os seguintes benefícios:
1. **Erradicar o medo de modificar o sistema/código fonte.**
  Pelo fato dos testes estarem verdes, será possível alterar a lógica de negócio e comportamentos da aplicação uma vez que as especificações estejam garantidas.
2. **Refatoração se torna algo fácil e seguro de ser feita.**
  Caso algum teste falhe durante um *refactoring* será possível identificar o problema e então corrigí-lo.

A curto prazo tudo isso pode parecer desnecessário, já que você irá escrever mais código do que o necessário para chegar no resultado desejado. Mas no longo prazo será um diferencial ter essa confiança para modificar o sistema conforme for preciso.

## Como fazer TDD?

To-do...

---

Já ouviu falar do **ada.rb - Arquitetura e Design de Aplicações em Ruby**? É um grupo focado em práticas de engenharia de software com Ruby. Acesse o <a href="https://t.me/ruby_arch_design_br" target="_blank">canal no telegram</a> e junte-se a nós em nosso <a href="https://www.meetup.com/pt-BR/design-e-arquitetura-de-aplicacoes-ruby/events/" target="_blank">meetup mensal</a> (100% on-line).
