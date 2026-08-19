# Go Machine Learning Papers (goMLPapers)

> Repositório de papers, links e anotações do grupo.
> Encontros quinzenais aos sábados. Modelo inspirado no [Deep Learning Study Group](https://github.com/mike-bowles/hdDeepLearningStudy) do Hacker Dojo (Mike Bowles), que roda desde 2016.

**Quando:** sábados, a cada 15 dias, horário: 09hAM às 11hAM

**Onde:** https://luma.com/9zdao5rq

**Primeira sessão:** 05/09/2026, sábado

Cobrimos machine learning em sentido amplo — modelos clássicos, deep learning, sistemas em produção e os papers fundacionais que sustentam tudo isso. Não é um grupo só de LLMs.

---

## Como funciona

Não é palestra. É discussão entre pares.

- Alguém precisa ter lido o paper antes. Idealmente três ou quatro pessoas.
- **Você pode vir sem ter lido** e só ouvir. Isso é explicitamente bem-vindo.
- Se ninguém tiver lido, a sessão é curta: assistimos juntos um vídeo de apoio e discutimos. Não cancelamos.
- Pergunta "básica" é o ponto do grupo, não um problema. Não gravamos as sessões justamente para isso.
- Não é preciso ter formação em pesquisa. Quem trabalha com dados no dia a dia costuma trazer as melhores objeções.

Detalhes operacionais em [`GUIA-DA-SESSAO.md`](GUIA-DA-SESSAO.md).

---

## Log de sessões

### Sessão 1 — sábado, 05/09/2026 — Attention Is All You Need

**Paper:** https://arxiv.org/abs/1706.03762 — *Attention Is All You Need* (Vaswani et al., NeurIPS 2017)

**Apoio:**
- The Illustrated Transformer (Jay Alammar) — https://jalammar.github.io/illustrated-transformer/
- The Annotated Transformer (Harvard NLP), o paper inteiro com código intercalado — http://nlp.seas.harvard.edu/2018/04/03/attention.html
- Implementação em PyTorch, mais legível que a original — https://github.com/jadore801120/attention-is-all-you-need-pytorch
- Vídeo de revisão — https://www.youtube.com/watch?v=S0KakHcj_rs

**Roteiro da sessão:** [`sessoes/01-attention-is-all-you-need.md`](sessoes/01-attention-is-all-you-need.md)

**Dúvidas em aberto:** _(preencher depois do encontro)_

---

<!--
TEMPLATE PARA AS PRÓXIMAS — copiar daqui pra cima, mais recente sempre no topo

### Sessão N — sábado, [DATA] — [Título curto]

**Paper:** [link] — *[título completo]* ([autores], [ano])

**Apoio:**
- [link]

**Dúvidas em aberto:**
- [o que ficou sem resposta — vira pauta de sessão futura]
-->

---

## Trilha inicial — detalhe

| # | Paper | Por que está aqui |
|---|---|---|
| 1 | **Attention Is All You Need** (2017) — [1706.03762](https://arxiv.org/abs/1706.03762) | A arquitetura que todo mundo cita e quase ninguém leu. Interesse alto, 8 páginas, material de apoio farto. |
| 2 | **A Few Useful Things to Know About Machine Learning** (Domingos, 2012) — [PDF](https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf) | O paper mais leve da trilha, colocado de propósito na sessão de maior evasão. É o "conhecimento de corredor" de ML que não está em livro-texto: overfitting, maldição da dimensionalidade, por que feature engineering decide o projeto. |
| 3 | **XGBoost: A Scalable Tree Boosting System** (2016) — [1603.02754](https://arxiv.org/abs/1603.02754) | O algoritmo que ainda ganha em dados tabulares. Traz para a sala quem faz ML aplicado e nunca vai treinar um Transformer. |
| 4 | **Hidden Technical Debt in ML Systems** (Sculley et al., 2015) — [PDF](https://proceedings.neurips.cc/paper_files/paper/2015/file/86df7dcfd896fcaf2674f757a2463eba-Paper.pdf) | O paper que fundou MLOps. Praticamente todo mundo que já colocou modelo em produção tem uma história para contar aqui — sessão de discussão altíssima. |
| 5 | **Scaling Laws for Neural Language Models** (2020) — [2001.08361](https://arxiv.org/abs/2001.08361) | Volta ao deep learning para explicar por que a resposta do campo virou "faz maior". Par natural com Chinchilla ([2203.15556](https://arxiv.org/abs/2203.15556)), que corrige este — bom candidato a sessão 7. |
| 6 | **LoRA: Low-Rank Adaptation** (2021) — [2106.09685](https://arxiv.org/abs/2106.09685) | O mais aplicável da lista. Fecha o ciclo com algo que dá para sair e usar na segunda-feira. |

---

## Como sugerir um paper

Manda no grupo de mensagens. O escriba adiciona em [`PapersSugeridos.md`](PapersSugeridos.md).
Sugerir **não** obriga a apresentar nem a ler. Quem já usa Git pode abrir um PR direto, mas isso é opcional.
