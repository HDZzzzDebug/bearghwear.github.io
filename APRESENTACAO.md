# Roteiro da apresentação: Beargh Wear

Tempo sugerido: 7 a 10 minutos. Cada bloco é um slide, e você deve fazer a demonstração com o site aberto.

## Slide 1: Capa (30 s)
- Nome do projeto: **Beargh Wear**, seu nome, curso e professor.

## Slide 2: Objetivo do site (1 min)
- Loja fictícia de camisetas e bermudas de bandas de metal.
- Objetivo: mostrar os produtos, deixar o cliente montar um carrinho e entrar em contato.
- Público: fãs de metal que querem peças com estampas exclusivas.

## Slide 3: Tecnologias (1 min)
- **React** (componentes, estado), **Vite** (execução e build), **Bootstrap** (grid responsivo), **HTML, CSS e JavaScript**.
- Por que React? Reaproveitar componentes (`ProductCard` é usado 9 vezes) e a tela atualizar sozinha quando o estado muda.

## Slide 4: Estrutura do projeto (1 min)
- Mostre a árvore de pastas: `components/`, `data/`, `hooks/`, `utils/`.
- Explique: os dados dos produtos ficam em `data/produtos.js`, e para adicionar um produto basta incluir uma linha lá.

## Slide 5: Principais funcionalidades, com demonstração ao vivo (3 min)
1. **Busca:** digite "gojira" e mostre o filtro. Explique: `produtos.filter(...)` com o estado `busca`.
2. **Carrinho:** abra um produto, escolha o tamanho e adicione. Recarregue a página e mostre que o carrinho continua lá. Explique: `useState` e `useEffect` salvando no `localStorage`.
3. **Checkout:** tente confirmar com CEP inválido e depois com dados corretos.
4. **Formulário de contato:** envie vazio, mostre os erros e depois envie corretamente.
5. **Player de música:** arraste, pause, troque de faixa.

## Slide 6: Responsividade e acessibilidade (1 min)
- Mostre no modo celular do DevTools (F12): menu vira botão e cards ficam em coluna.
- Acessibilidade: labels nos campos, `aria-label` nos botões de ícone, Esc fecha as janelas, foco visível (mostre navegando com Tab), música não toca sozinha.

## Slide 7: Testes e correções (1 min)
- Mostre a tabela de testes do README.
- Conte um erro real que você corrigiu (ex.: `npm install` falhando por versões incompatíveis do Vite e do plugin React).

## Slide 8: Conclusão (30 s)
- O que você aprendeu e o que melhoraria (otimizar imagens, quantidade no carrinho, back-end).

---

## Perguntas que o professor pode fazer (prepare as respostas)

- **O que é o `useState`?** Guarda um valor que, ao mudar, faz o componente ser desenhado de novo (ex.: a lista de itens do carrinho).
- **O que o `useEffect` faz no `App.jsx`?** Sempre que o carrinho muda, salva no `localStorage` e atualiza o título da aba.
- **Como funciona a validação?** As regras estão em `utils/validacao.js` e cada função devolve uma mensagem de erro ou texto vazio. O formulário valida ao sair do campo (`onBlur`) e ao enviar (`onSubmit`).
- **Por que `noValidate` no formulário?** Desliga os balões padrão do navegador para usar nossas próprias mensagens, que são acessíveis e padronizadas.
- **O que é `props`?** Dados que um componente pai passa ao filho (ex.: `ProductCard` recebe `produto` e `onVerDetalhes`).
- **Por que o `Button` é um componente?** Para reaproveitar o mesmo botão em vários lugares, mudando só a variante e o texto.
- **Como o site fica responsivo?** Pelo grid do Bootstrap (`col-md-4`) e por media queries no `style.css`.
- **Usou IA?** Se usou, seja honesto e saiba explicar cada parte. O enunciado permite, desde que você entenda o código.
