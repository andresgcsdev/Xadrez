# Xadrez

> Segunda implementação de xadrez que fiz em 2023, desta vez para a web. Desenvolvida durante o CEFET-MG como projeto de conclusão de disciplina e depois expandida por conta própria. O código reflete meu nível de conhecimento na época e é mantido aqui como registro de evolução.

---

## Sobre

Jogo de xadrez completo feito com HTML, CSS e JavaScript puro, sem frameworks. Suporta todas as regras oficiais do jogo, incluindo roque e detecção de xeque. Duas pessoas podem jogar no mesmo navegador.

---

## Como jogar

1. Abra `index.html` no navegador
2. Clique em uma peça para ver os movimentos possíveis destacados em vermelho
3. Clique em um quadrado destacado para mover
4. As peças brancas começam

---

## Regras implementadas

- Movimentos legais de todas as peças
- Detecção de xeque — movimentos que deixam o próprio rei em xeque são bloqueados
- Roque (kingside e queenside) para ambos os lados
- Detecção de xeque-mate e afogamento

---

## PeacockBass

O projeto inclui uma tentativa de motor de xadrez chamada `PeacockBass` — o nome não tem explicação oficial.

A ideia era implementar um algoritmo de busca com lookahead que avaliasse posições considerando:

- Controle de casas no tabuleiro
- Valor material das peças capturadas
- Xeque-mate (+10000 pts) e afogamento (-5000 pts)

A função `foresight` implementa uma busca recursiva que tenta prever movimentos futuros tanto das peças pretas quanto das brancas. O motor nunca chegou a funcionar corretamente — problemas de performance do JavaScript para este tipo de busca e alguns bugs de lógica na avaliação fizeram o projeto ser abandonado antes de ser concluído.

A estrutura está lá se alguém tiver curiosidade. Os `debugger` statements espalhados pelo código são evidência arqueológica de onde a depuração parou.

---

## Contexto

Esta foi minha segunda implementação de xadrez — a primeira foi em VisuAlg durante o primeiro ano do CEFET e está perdida. Depois desta versão web vieram implementações em C++, Java, Rust e outras linguagens, cada uma servindo como forma de aprender a linguagem usando um problema que já conhecia bem.

O motor de xadrez desta versão foi eventualmente refeito do zero em C++ com arquitetura adequada, onde a performance deixou de ser um limitante.
