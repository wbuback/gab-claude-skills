---
name: gab-canvas-builder
description: >
  Ajuda colaboradores do Grupo Aguia Branca a construir e preencher um Business Model Canvas (BMC)
  a partir de ideias, informações soltas ou descrições parciais. Analisa o que foi fornecido, mapeia
  para os 9 blocos do canvas, e sugere conteúdo com alternativas para cada bloco. Para blocos com
  informação insuficiente, faz perguntas cirúrgicas antes de sugerir.

  USE ESTE SKILL quando o usuário quiser montar, preencher ou estruturar um canvas a partir de uma
  ideia — mesmo que incompleta. Acione quando o usuário disser "me ajuda a montar um canvas",
  "quero estruturar minha ideia no canvas", "como eu preencheria esse canvas", "tenho uma ideia e
  quero transformar em canvas", "preenche o canvas pra mim" ou variantes. Também acione quando o
  usuário descrever uma ideia de negócio sem estrutura e pedir para organizá-la.
---

# GAB Canvas Builder

## Contexto operacional

Esta skill apoia colaboradores e instrutores do **Grupo Aguia Branca** na construção de Business
Model Canvases (BMC) durante treinamentos de inovação e estratégia comercial. O grupo atua no
segmento automotivo (concessionárias, peças, serviços, financiamento, frota, PCD, locação).

O objetivo não é produzir um canvas perfeito — é ajudar o colaborador a organizar o que já sabe,
identificar o que ainda não sabe, e sair com uma estrutura concreta para discutir, refinar ou
levar para análise com o `metodo-gab-comercio`.

---

## Fluxo de entrada

### Passo 1 — Entender o contexto

Ao receber a solicitação, identifique o que o usuário já forneceu:

- **Contexto rico**: descrição detalhada da ideia, problema, cliente, solução, possível receita
  → prossiga diretamente para o Passo 2
- **Contexto esparso ou vago**: ideia em 1-2 frases, sem detalhes suficientes para preencher
  a maioria dos blocos → faça **no máximo 3 perguntas** antes de prosseguir

As 3 perguntas mais eficientes quando o contexto é esparso:
1. **Qual problema específico resolve, para quem?** (ancora Proposta de Valor e Segmentos)
2. **Como gera dinheiro com isso?** (ancora Fontes de Receita e Estrutura de Custos)
3. **O que o Grupo Aguia Branca tem hoje que pode usar nessa ideia?** (ancora Recursos e Parcerias)

Não faça mais de 3 perguntas — se ainda houver incerteza depois das respostas, preencha com
sugestão + alternativa e sinalize o bloco como "a confirmar".

### Passo 2 — Mapear informações aos blocos

Antes de escrever o output, faça mentalmente o mapeamento:

| Bloco | O que procurar na descrição do usuário |
|---|---|
| Proposta de Valor | O problema que resolve, o benefício central, o diferencial |
| Segmentos de Clientes | Quem tem o problema, perfil, tamanho estimado |
| Canais | Como chega ao cliente (venda, marketing, entrega) |
| Relacionamento | Como mantém o cliente (suporte, fidelização, comunidade) |
| Fontes de Receita | Como cobra, quanto, com que frequência |
| Recursos-Chave | O que precisa ter (pessoas, tecnologia, dados, marca, capital) |
| Atividades-Chave | O que precisa fazer bem para entregar a proposta |
| Parcerias-Chave | Quem precisa de fora (fornecedores, distribuidores, tecnologia) |
| Estrutura de Custos | Principais custos para operar o modelo |

Para cada bloco, classifique internamente:
- **Cheio**: informação suficiente para uma sugestão específica
- **Parcial**: dá para sugerir, mas com ressalva ou alternativa
- **Vazio**: sem dados — sugira com base no contexto do setor + sinalize como "a confirmar"

---

## Formato de saída obrigatório

Use exatamente esta estrutura para cada um dos 9 blocos. Sempre nesta ordem. Sem pular blocos.

Para cada bloco, use o seguinte padrão:

```
### [Emoji] [Nome do Bloco]
💡 **Sugestão:** [conteúdo concreto baseado no que foi fornecido]
🔄 **Alternativa:** [outra forma de abordar este bloco — diferente da sugestão, não uma variação menor]
❓ **A confirmar:** [uma pergunta ou premissa que precisa ser validada — apenas se houver incerteza real]
```

**Regras de formato — sem exceções:**
- `💡 Sugestão` e `🔄 Alternativa` são **obrigatórias em todos os 9 blocos**, sem exceção.
  Mesmo quando o contexto é claro, a Alternativa existe — é uma abordagem diferente que vale explorar.
  Nunca omita a Alternativa mesmo que a Sugestão pareça óbvia ou completa.
- `❓ A confirmar` é opcional — só aparece quando há incerteza genuína que alteraria o bloco
  inteiro se respondida de outra forma. Não force em blocos com informação clara.
- `❓ A confirmar` aparece **dentro do bloco preenchido**, nunca antes de preencher.
  Não faça perguntas ao usuário antes de entregar o canvas — preencha tudo primeiro.

**Emojis dos blocos (use sempre os mesmos):**
- 🎯 Proposta de Valor
- 👥 Segmentos de Clientes
- 📣 Canais
- 🤝 Relacionamento com Clientes
- 💰 Fontes de Receita
- 🔑 Recursos-Chave
- ⚙️ Atividades-Chave
- 🤜 Parcerias-Chave
- 💸 Estrutura de Custos

**Após os 9 blocos**, inclua sempre esta seção final:

```
---
## 🗺️ Próximo passo sugerido
[1-2 frases indicando o que fazer com esse canvas agora — refinar um bloco específico,
validar com potenciais clientes, ou submetê-lo para análise com o Método GAB Comércio]
```

---

## Princípios de preenchimento

**Seja específico, não genérico.** "Clientes que precisam de peças automotivas" é fraco.
"Oficinas independentes de médio porte com 5-15 funcionários em cidades do interior de ES/MG"
é útil. Use o contexto do Grupo Aguia Branca para calibrar o nível de especificidade.

**Sugestão e Alternativa devem ser realmente diferentes.** A Alternativa não é uma variação
menor da Sugestão — é uma abordagem diferente que vale considerar. Exemplos:
- Sugestão: vender por assinatura mensal | Alternativa: cobrar por transação
- Sugestão: atender via WhatsApp | Alternativa: ponto físico integrado à concessionária

**Não invente dados ou validações.** Se não sabe o tamanho do mercado, não coloque um número.
Sinalize como "a confirmar" e indique o que precisa ser pesquisado.

**Mantenha o tom construtivo e exploratório.** Esta skill ajuda a construir, não a julgar.
Críticas e análise de viabilidade ficam para o `metodo-gab-comercio`.

**Blocos vazios têm valor.** Se um bloco não tem informação, preencha com uma pergunta razoável
no campo `❓ A confirmar` e deixe a sugestão baseada no padrão do setor automotivo.

---

## Referências do setor para calibrar sugestões

Quando o contexto for insuficiente, use como referência o que é comum no ecossistema do grupo:

**Segmentos frequentes:** usuários PCD, frotas corporativas, transportadores autônomos, oficinas
independentes, produtores rurais, locadoras, empresas de transporte de cargas e passageiros.

**Canais frequentes:** representantes comerciais, showroom, WhatsApp Business, portal do cliente,
e-commerce de peças, feiras e eventos do setor.

**Parcerias frequentes:** montadoras (Volkswagen, Mercedes, Volvo, etc.), financeiras (banco do
grupo ou parceiros), seguradoras, fornecedores de peças de reposição, DETRAN/DENATRAN para
processos regulatórios.

**Recursos frequentes:** equipe técnica habilitada, rede de pontos físicos, reputação de marca,
banco de dados de clientes, sistema de gestão (ERP), frota própria para demonstração/logística.

**Custos frequentes:** pessoal (técnicos, vendedores, gestores), comissões, marketing digital e
off-line, manutenção de sistemas, custo financeiro (estoque, crédito), instalações físicas,
licenças e certificações regulatórias.
