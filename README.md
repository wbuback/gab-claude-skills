# claude-skills

Skills do Grupo Aguia Branca para uso com Claude (Cowork, Claude Code ou API).
Desenvolvidas para apoiar treinamentos de inovação e estratégia comercial no setor automotivo.

---

## Skills disponíveis

### 🧩 `gab-canvas-builder`
**Constrói um Business Model Canvas a partir de ideias brutas ou informações parciais.**

Aceita desde uma descrição informal até um canvas já iniciado com blocos em branco. Para cada um dos 9 blocos do BMC entrega uma Sugestão específica ao contexto, uma Alternativa genuinamente diferente, e quando necessário uma linha "A confirmar" indicando o que precisa ser validado antes de avançar. Modo híbrido: se o contexto for rico preenche direto; se for esparso faz até 3 perguntas cirúrgicas antes de preencher.

**Quando usar:** antes de ter um canvas — para transformar uma ideia em estrutura.

---

### 🔍 `metodo-gab-comercio`
**Analisa um Business Model Canvas já preenchido com profundidade estratégica.**

Aplica 5 camadas de análise (coerência interna, oferta de valor, viabilidade econômica, contexto de mercado automotivo BR, riscos e pontos cegos) e entrega um diagnóstico estruturado em 5 seções: Diagnóstico Rápido com semáforo de coerência (🟢/🟡/🔴), Pontos Fortes, Críticas e Lacunas priorizadas por impacto, Contexto de Mercado com diferenciação entre fato e inferência, e Próximos Passos com ações em até 90 dias e hipótese prioritária de validação. Tom calibrado pelo estágio da ideia (hipótese inicial vs. plano maduro).

**Quando usar:** depois de ter um canvas — para validar, criticar e decidir o que fazer a seguir.

---

## Fluxo recomendado

```
Ideia bruta
    ↓
gab-canvas-builder  →  Canvas com 9 blocos preenchidos (Sugestão + Alternativa por bloco)
    ↓
Revisão com o colaborador  →  Ajusta, complementa, valida premissas
    ↓
metodo-gab-comercio  →  Diagnóstico: semáforo, críticas, mercado, próximos passos
    ↓
Decisão: refinar, pilotar ou descartar
```

---

## Como instalar

### Opção 1 — Via arquivo `.skill` (Cowork)

1. Baixe a pasta da skill desejada deste repositório
2. No Cowork, acesse **Plugins → Instalar skill**
3. Selecione o arquivo `SKILL.md` da pasta correspondente
4. A skill estará disponível na sessão imediatamente

### Opção 2 — Manual (Claude Code)

1. Clone este repositório:
   ```bash
   git clone https://github.com/wbuback/claude-skills.git
   ```
2. Copie a pasta da skill para o diretório de skills do seu ambiente:
   ```bash
   cp -r claude-skills/metodo-gab-comercio ~/.claude/skills/
   cp -r claude-skills/gab-canvas-builder ~/.claude/skills/
   ```
3. Reinicie o Claude Code ou recarregue a sessão

---

## Como usar

### `gab-canvas-builder` — exemplos de entrada

```
Me ajuda a montar um canvas. Tenho uma ideia de [descreva a ideia].
```
```
Quero estruturar minha ideia no canvas. [Descreva o problema, o cliente, como gera receita].
```
```
Preenche o canvas pra mim com base nisso: [cole um canvas parcial ou bullet points].
```

A skill detecta automaticamente se o contexto é rico (preenche direto) ou esparso (faz até 3 perguntas antes de preencher). O output traz os 9 blocos do BMC com Sugestão, Alternativa e — quando necessário — linha "A confirmar" por bloco, seguidos de um próximo passo recomendado.

---

### `metodo-gab-comercio` — exemplos de entrada

```
Analise esse canvas. [Cole o canvas em texto ou anexe a imagem].
```
```
Avalie essa ideia de negócio. É uma hipótese inicial. [Descreva os blocos].
```
```
O que acha desse modelo de negócio? É um plano mais avançado, analise com rigor.
```

Inclua o **estágio da ideia** (hipótese inicial, em desenvolvimento ou plano maduro) — isso calibra o tom e a profundidade da análise. O canvas pode ser enviado como texto estruturado ou como imagem (foto, print, arquivo).

---

## Estrutura do repositório

```
claude-skills/
├── README.md
├── metodo-gab-comercio/
│   ├── SKILL.md          # Instruções completas da skill
│   └── evals/
│       └── evals.json    # Casos de teste e assertions de qualidade
└── gab-canvas-builder/
    ├── SKILL.md
    └── evals/
        └── evals.json
```

---

## Contexto de desenvolvimento

Skills desenvolvidas para os treinamentos de inovação do **Grupo Aguia Branca**, setor automotivo. Testadas com 3 cenários cada (canvas rico, esparso e parcial), com 100% nas assertions de qualidade e delta de +48pp a +64pp em relação ao uso sem skill.

Processo: draft → teste com e sem skill → grading automatizado → análise de falhas → refinamento → empacotamento.
