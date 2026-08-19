# Sessão 1 — Attention Is All You Need

**Paper:** Vaswani et al., *Attention Is All You Need*, NeurIPS 2017 — https://arxiv.org/abs/1706.03762
**Data:** sábado, 05/09/2026
**Âncora:** [preencher]
**Escriba:** [preencher]

---

## Por que este paper primeiro

É o paper que qualquer pessoa que aparecer no grupo já ouviu falar e provavelmente nunca leu. Isso é exatamente o que se quer numa primeira sessão: interesse alto, barreira de entrada baixa (8 páginas de corpo), e uma enxurrada de material de apoio para quem travar.

Dois avisos úteis para o âncora:

**O paper é mais seco do que a fama sugere.** É um paper de tradução automática, com tabelas de BLEU — não é um manifesto sobre LLMs. Quem chega esperando epifania sai frustrado se não for avisado antes. Diga isso na abertura; converte frustração em expectativa calibrada.

**Como o grupo é de machine learning em sentido amplo, vai ter gente na sala que trabalha com dados tabulares e nunca treinou uma rede neural.** Não deixe a conversa assumir familiaridade com seq2seq, embeddings ou treino de redes. Cinco minutos de contexto na abertura — "antes disso, modelos de sequência processavam palavra por palavra, em ordem" — evita perder metade da sala nos primeiros vinte minutos. A sessão 2 (Domingos) foi colocada logo em seguida justamente para reequilibrar.

---

## Leitura mínima

Para quem tem 30 minutos: seções 1, 3.1, 3.2 e 3.5. É o núcleo.
Para quem tem 15 minutos: o Illustrated Transformer do Jay Alammar, e só.

**Apoio:**
- The Illustrated Transformer — https://jalammar.github.io/illustrated-transformer/
- The Annotated Transformer (Harvard NLP), o paper inteiro com código intercalado — http://nlp.seas.harvard.edu/2018/04/03/attention.html
- Implementação PyTorch legível — https://github.com/jadore801120/attention-is-all-you-need-pytorch
- Vídeo de revisão — https://www.youtube.com/watch?v=S0KakHcj_rs

---

## Perguntas-guia por seção

Não precisa cobrir todas. São iscas de discussão, não checklist.

**Seção 1–2 — Motivação**
- O que exatamente foi *removido* em relação aos modelos seq2seq com recorrência? E o que se ganhou com essa remoção — a resposta central é sobre paralelização no treino, não sobre qualidade.
- O título é uma provocação. Ele se sustenta? O que ainda tem no modelo além de atenção?

**Seção 3.2.1 — Scaled Dot-Product Attention**
- Por que dividir por √d_k? O que acontece com o softmax se você não dividir? (O paper explica em uma nota de rodapé — vale ler em voz alta.)
- Q, K e V vêm todos da mesma entrada na self-attention. Se são a mesma coisa, por que três projeções diferentes?

**Seção 3.2.2 — Multi-Head Attention**
- Por que h cabeças de dimensão d/h em vez de uma cabeça de dimensão d? O custo computacional é parecido — então o argumento é sobre o quê?
- O argumento do paper aqui é essencialmente uma intuição, não uma demonstração. Ele convence vocês?

**Seção 3.5 — Positional Encoding**
- Por que o modelo precisa disso? O que na arquitetura faz a ordem das palavras desaparecer?
- Eles testaram encoding aprendido e ficaram com o senoidal fixo. Qual foi a justificativa? Ela envelheceu bem?

**Seção 4 e Tabela 1 — Complexidade**
- Self-attention por camada é O(n²·d); recorrente é O(n·d²). Para que valores de n e d cada um ganha?
- Esse n² é a origem de praticamente toda a literatura de long-context da década seguinte. Vale parar aqui alguns minutos.

**Seção 5 — Treino**
- Quanto do resultado é a arquitetura e quanto é a receita de treino (warmup do learning rate, dropout, label smoothing)? O paper permite separar isso?
- O modelo grande foi treinado em poucos dias em 8 GPUs. Compare mentalmente com um treino de fronteira hoje. O que essa diferença diz sobre o que mudou desde 2017?

**Duas perguntas de fechamento**
- Este é um modelo **encoder-decoder** para tradução. Praticamente tudo que a gente usa hoje é **decoder-only**. Em que momento e por quê o campo jogou metade da arquitetura fora? _(Ninguém vai saber responder direito. Ótimo — vira dúvida em aberto no log.)_
- Pergunta para o pessoal de ML aplicado na sala: em que tipo de problema você **não** usaria isso, e por quê? _(Ponte direta para as sessões 3 e 4, e sinaliza desde o primeiro dia que o grupo não é um clube de LLM.)_

---

## Armadilhas conhecidas

- **A discussão trava na matemática da atenção e nunca sai de lá.** O âncora deve cortar aos 45 min e forçar a passagem para positional encoding e complexidade, mesmo com gente insatisfeita. O que ficou sem resolver vai para o log.
- **Alguém quer discutir ChatGPT/Claude em vez do paper.** Deixe rolar 5 minutos, depois traga de volta — e registre como sugestão para a fila.
- **A tabela de BLEU dá vontade de pular.** Não pule inteira: é o único lugar onde se vê que a alegação do paper foi de fato testada contra alternativas da época.
- **Silêncio nos primeiros 10 minutos.** Normal numa primeira sessão. O âncora quebra dirigindo uma pergunta concreta a uma pessoa específica, não à sala.

---

## Depois da sessão

O escriba preenche no `README.md`:
- Dúvidas em aberto
- Papers que surgiram na conversa → vão para `PapersSugeridos.md`
- Se decidiram esticar para uma segunda sessão

E confirma no grupo: **próxima em 19/09/2026, com o paper do Domingos** — que é curto e leve de propósito, para segurar quem achou este aqui pesado.
