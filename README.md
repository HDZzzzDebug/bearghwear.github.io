# Beargh Wear

Este é o meu projeto integrador do curso de Programador Front-End. É um site de uma loja fictícia chamada Beargh Wear, que vende camisetas e bermudas com estampas de bandas de metal.

## O que o site faz

Na página inicial tem uma apresentação da loja e um menu para ir até as seções Produtos, Sobre e Contato. Dá para buscar produtos pelo nome da banda ou do álbum, ver os detalhes de cada um, escolher o tamanho e adicionar no carrinho. O carrinho continua salvo mesmo se a página for recarregada. Também dá para finalizar a compra, mas é só uma simulação, não existe pagamento de verdade. Tem ainda um formulário de contato e um player de música.

## Tecnologias

React, Vite, Bootstrap, HTML, CSS e JavaScript.

## Como rodar

Precisa ter o Node.js instalado. Depois, no terminal:

```
cd beargh-wear-react
npm install
npm run dev
```

Aí é só abrir no navegador o endereço que aparecer no terminal, normalmente http://localhost:5173.

## Como o projeto está organizado

- `public/`: imagens e músicas
- `src/components/`: as partes do site (menu, cards, carrinho, formulários)
- `src/data/`: lista de produtos e de músicas
- `src/hooks/`: código para fechar as janelas com a tecla Esc
- `src/utils/`: regras de validação dos formulários
- `src/App.jsx`: página principal
- `src/style.css`: estilos do site

## Validação dos formulários

Os formulários de contato e de compra conferem os campos antes de enviar e mostram uma mensagem quando algo está errado. O nome precisa ter pelo menos 3 letras, o e-mail precisa ser válido, a mensagem precisa ter pelo menos 10 caracteres e o CEP precisa ter 8 números. Endereço e cidade são obrigatórios.

## Acessibilidade

Todos os campos têm rótulo, os botões que só têm ícone têm descrição para leitores de tela, as janelas fecham com Esc e a música não toca sozinha.

## Testes

Testei buscando bandas e termos que não existem, adicionando e removendo itens do carrinho, recarregando a página para ver se o carrinho continuava lá, enviando os formulários vazios, com dados errados e com dados corretos, fechando as janelas com Esc e vendo o site em tela de celular. Também conferi se `npm install` e `npm run build` rodam sem erro.

## Erros que corrigi

- O `npm install` dava erro por causa da versão do Vite, então ajustei a versão.
- O formulário não mostrava mensagens de erro, então criei uma validação própria.
- A música tocava sozinha, e agora só toca quando a pessoa aperta play.

## Autor

Seu nome aqui
