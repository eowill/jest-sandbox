# Mini E-commerce — Laboratório de Testes com Jest

Um e-commerce funcional, em HTML/CSS/JS puro, criado para servir como **playground de testes** para quem está aprendendo Jest. Em vez de exercícios isolados, o aluno explora um sistema real (produtos, carrinho, login, cupons, estoque, pedidos, relatórios...) e escreve seus próprios testes — **sem receber as respostas prontas**.

![status](https://img.shields.io/badge/status-em%20uso-39dc84) ![stack](https://img.shields.io/badge/stack-HTML%20%2F%20CSS%20%2F%20JS-4fd1ff) ![deps](https://img.shields.io/badge/depend%C3%AAncias-zero-ff3f8e)

---

## O que é

Um único arquivo `mini-ecommerce-lab.html`, sem build, sem dependências externas, contendo:

- Uma loja **funcional de verdade**: catálogo de produtos, carrinho, favoritos, cupons, controle de estoque, perfil, pedidos e relatórios de vendas.
- Um **Laboratório de Testes** embutido, com uma página dedicada a cada uma das 26 funções do sistema.
- Uma **Área de Experimentos** (console JS no navegador) para o aluno chamar as funções manualmente antes de escrever o teste.
- **Modo Desafio**, que esconde o código-fonte da função e deixa só o enunciado.
- **Modo Professor**, com painel de progresso por módulo.
- Botão **"Gerar novo cenário"**, que embaralha os dados do catálogo para evitar testes "hardcoded".

> O site nunca mostra a resposta do teste — apenas a lista de matchers possíveis, sem indicar qual usar.

---

## Objetivo pedagógico

Praticar os principais recursos do Jest de forma natural, dentro de um contexto único:

- funções puras e impuras
- arrays e objetos
- mutação vs. imutabilidade
- exceções (`toThrow`)
- Promises (`resolves` / `rejects`)
- mocks e expiração de dados (cupons, estoque)

---

## Módulos disponíveis

| Módulo | Funções |
|---|---|
| Login | `fazerLogin` |
| Produtos | `listarProdutos`, `buscarProduto`, `buscarPorCategoria`, `produtoExiste` |
| Carrinho | `adicionarAoCarrinho`, `removerDoCarrinho`, `calcularTotal`, `limparCarrinho` |
| Favoritos | `adicionarFavorito`, `removerFavorito`, `verificarFavorito` |
| Cupons | `cupomValido`, `aplicarCupom` |
| Estoque | `verificarEstoque`, `reduzirEstoque`, `aumentarEstoque` |
| Perfil | `atualizarNome`, `atualizarEmail`, `atualizarTelefone` |
| Pedidos | `criarPedido`, `cancelarPedido`, `buscarPedido` |
| Relatórios | `calcularVendas`, `produtoMaisVendido`, `ticketMedio` |

---
### Login de teste
```
usuário: aluno
senha:   123456
```

### Cupons de teste
```
BEMVINDO10   → 10% de desconto, válido
FRETEGRATIS  → 5% de desconto, válido
EXPIRADO     → 20% de desconto, mas vencido
```

---

## Como funciona o laboratório

1. Escolha um módulo no menu lateral (ou vá direto em **Laboratório de Testes**).
2. Clique em uma função para abrir o card com:
   - **Objetivo** do teste
   - **Código da função** (oculto no Modo Desafio)
   - **O que observar** — perguntas-guia
   - **Planejamento** — checklist de progresso
   - **Matchers sugeridos** — lista solta, sem indicar a resposta
   - **Área de Experimentos** — console para chamar a função manualmente
3. Escreva o teste correspondente no seu próprio projeto Jest, usando a função copiada/extraída do laboratório.
4. Marque "testei este teste como concluído" para acompanhar seu progresso.

> Todas as funções também ficam expostas no `window`, então dá pra abrir o DevTools do navegador e chamar `listarProdutos()`, `calcularTotal(getCarrinho())` etc. diretamente — exatamente como a Área de Experimentos faz internamente.

---

## Stack

- HTML + CSS + JavaScript puro (vanilla)
- Zero dependências, zero build step
- Progresso salvo em `localStorage`
- Fonte: [JetBrains Mono](https://www.jetbrains.com/lp/mono/) + [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) via Google Fonts

---

## Estrutura

```
mini-ecommerce-lab/
└── mini-ecommerce-lab.html   # aplicação inteira (HTML + CSS + JS embutidos)
```

---


---

## 📄 Licença

Uso livre para fins educacionais.
