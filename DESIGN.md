# Relatório de Pesquisa & Prompt Mestre: Landing Page de Creatina (HTML/CSS/JS)

Este documento reúne uma investigação aprofundada sobre as melhores práticas de conversão para o mercado de suplementos esportivos, o mapeamento das tendências em **MCP (Model Context Protocol) Design Skills** que estão moldando o desenvolvimento web moderno assistido por IA, e um **Prompt Mestre** pronto para uso.

---

## Parte 1: Melhores Práticas de Design para a Indústria de Suplementos e Fitness

As landing pages de saúde, bem-estar e suplementação (especialmente produtos ingeríveis como a **Creatina Monohidratada**) operam sob uma regra central: **construir confiança científica e desejo imediato antes do primeiro scroll**. 

### 1. Transparência Radical e "Ciência Visível"
* **Fim das promessas vagas:** O consumidor moderno de fitness é educado. Em vez de frases genéricas como *"Melhore sua saúde"*, as páginas de alta conversão lideram com métricas exatas e dados clínicos (ex: *"Aumento comprovado de até 15% na força explosiva e ressíntese de $\text{ATP}$"*, *"100% Pura — Zero Carboidratos, Zero Calorias"*).
* **Rótulo e Pureza em Destaque:** Marcas líderes (como *AG1*, *IM8*, *Onnit* e referências de creatina com selo *Creapure®*) expõem a tabela nutricional, o tamanho do *scoop* ($3\text{g}$ a $5\text{g}$) e laudos laboratoriais de forma interativa logo nas primeiras dobras da página.
* **Quebra de Objeções Imediata:** O medo de "retenção hídrica estética/inchaço" ou "problemas renais" deve ser desmistificado com base em estudos científicos através de micro-seções visuais claras antes mesmo do usuário chegar ao FAQ.

### 2. Estética Visual: "Clinical Performance" vs. "Dark Gym"
* **Evolução Estética:** O design antigo de suplementos (fundos pretos poluídos, fontes agressivas rasgadas, chamas e potes gigantes) deu lugar à estética **Bio-Tech / Clinical Performance**.
* **Paleta de Cores Intencional:** Contraste cirúrgico entre fundos escuros profundos (Obsidian `#0A0A0C`) ou *off-white* laboratorial (`#F4F4F6`), combinados com uma única cor de acento de alta energia (como *Volt/Acid Lime* `#CCFF00`, *Electric Cyan* `#00F0FF` ou *International Orange* `#FF4D00`).
* **Contexto de Uso Real:** Mostrar não apenas o pote, mas o momento do uso e a textura (ex: micronização do pó dissolvendo perfeitamente na água sem empelotar).

### 3. Ferramentas Interativas de Conversão (Zero Fricção)
* **Calculadoras no Próprio Fluxo:** Em páginas de creatina, uma **Calculadora de Dosagem Diária** (baseada no peso corporal: $\approx 0.07\text{g/kg}$) ou **Simulador de Fase de Saturação vs. Uso Contínuo** aumenta drasticamente o tempo de permanência na página e a conversão.
* **CTAs Orientados a Benefício:** Evitar botões passivos como *"Comprar"* ou *"Enviar"*. Utilizar chamadas ativas: *"Garantir Minha Força Máxima"*, *"Começar Ciclo de 90 Dias"*.

---

## Parte 2: O que está em alta em Habilidades de Design de MCPs (Model Context Protocol)

O ecossistema de desenvolvimento front-end assistido por agentes (Claude Code, Cursor, Windsurf, etc.) passou por uma revolução com o uso de **MCP Servers** de UI e arquivos de especificação comportamental conhecidos como **Agent Design Skills** (`SKILL.md` e `DESIGN.md`). 

As práticas abaixo representam o que há de mais avançado nesse padrão e foram incorporadas diretamente no seu prompt da Parte 3:

### 1. A Diretriz "Anti-AI Slop" (Habilidade `anthropic/frontend-design` & `superdesign-skill`)
As *Skills* de design mais populares exigem que o código gerado **rejeite os vícios visuais clássicos de IA**:
* **Proibição de clichês:** Nada de gradientes roxo/azul genéricos, nada de destacar uma única palavra do título com texto colorido/itálico sem propósito, e nada de cards genéricos com sombras difusas iguais.
* **Tipografia como Elemento Estrutural:** Uso de escalas tipográficas matemáticas (`clamp()`), combinação deliberada de uma fonte de exibição forte (Display/Grotesque) com uma fonte técnica/monoespaçada para dados laboratoriais e dosagens.
* **Estrutura como Informação:** Números sequenciais (`01 / 02 / 03`), bordas finas de $1\text{px}$ e divisores estilo tabela nutricional só devem ser usados quando comunicam hierarquia real ou etapas de um processo fisiológico.

### 2. Arquitetura Baseada em `DESIGN.md` e Tokens Semânticos
* Em vez de jogar cores aleatórias no CSS, os agentes modernos operam melhor quando orientados a criar **Design Tokens Semânticos em CSS Custom Properties (`:root`)**: definindo papéis claros como `--surface-base`, `--surface-raised`, `--text-primary`, `--text-muted`, `--border-hairline` e `--accent-kinetic`.

### 3. Sub-skills Técnicas do Catálogo `ui-skills` (ibelick / Vercel Guidelines)
Os servidores MCP voltados a UI auditam quatro pilares fundamentais que você pode exigir no código puro:
1. **`baseline-ui`:** Escala consistente de espaçamentos, prevenção de quebras de layout em telas menores e linhas de texto com largura máxima de leitura ($60\text{ch}$ a $75\text{ch}$).
2. **`fixing-motion-performance`:** Proibição de animações que causam *layout thrashing* (animar `top`, `left`, `width`, `height`). Exigência de animar exclusivamente propriedades de composição na GPU (`transform` e `opacity`) e respeito obrigatório a `@media (prefers-reduced-motion: reduce)`.
3. **`fixing-accessibility`:** Conformidade nativa com **WCAG 2.1 AA** — contraste mínimo de $4.5:1$, navegação completa por teclado (`:focus-visible` estilizado), atributos `aria-expanded` em acordeões de FAQ e rótulos semânticos em formulários/calculadoras.
4. **`fixing-metadata`:** Inclusão de dados estruturados (`JSON-LD` para produto/FAQ) e semântica HTML5 rigorosa (`<header>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`).

---

## Parte 3: O Prompt Mestre (Copie e Cole)

Abaixo está o prompt engenheirado com os padrões de **DESIGN.md** e **UI Skills** para que qualquer LLM gere uma landing page extraordinária usando exclusivamente HTML, CSS e JavaScript puros.

```text
Atue como um Principal Frontend Architect e Lead Product Designer especializado em marcas de alta performance esportiva e suplementação científica (referências estéticas: AG1, Onnit, Nike Lab, Momentous).

Sua missão é desenvolver uma Landing Page completa, altamente estruturada, responsiva e interativa sobre o uso de CREATINA MONOHIDRATADA PARA ACADEMIA E ALTA PERFORMANCE, utilizando EXCLUSIVAMENTE HTML5 semântico, CSS3 moderno (Vanilla CSS) e JavaScript puro (ES6+ Vanilla JS). Não utilize frameworks externos (sem Tailwind, sem Bootstrap, sem React, sem bibliotecas JS externas).

====================================================================
1. DIRETRIZES DE DESIGN & "MCP UI SKILLS" (REGRAS ANTI-CLICHÊ)
====================================================================
Siga rigorosamente as restrições das skills modernas de design (`frontend-design`, `baseline-ui`, `fixing-motion-performance` e `fixing-accessibility`):
- ESTÉTICA "CLINICAL BIO-PERFORMANCE": Evite o visual genérico de IA (proibido usar gradientes roxo/azul, sombras pesadas ou layouts de templates comuns). Adote uma direção de arte inspirada em laboratórios esportivos de precisão: linhas divisórias finas de 1px (`hairline borders`), estética de rótulo nutricional suíço (Swiss Grid), alto contraste e dados técnicos em destaque.
- SISTEMA DE TOKENS NO `:root`: Defina variáveis CSS semânticas logo no início:
  * `--bg-base`: #090A0C (Obsidian Deep)
  * `--bg-surface`: #121418 (Carbon Surface)
  * `--bg-elevated`: #1A1D24 (Elevated Card)
  * `--text-primary`: #F4F5F7 (Pure Lab White)
  * `--text-secondary`: #9BA1AE (Muted Metallic)
  * `--accent-primary`: #D4FF00 (Kinetic Acid Volt)
  * `--accent-secondary`: #00E5FF (Bio-Metric Cyan - apenas para dados científicos)
  * `--border-subtle`: rgba(255, 255, 255, 0.09)
  * `--font-display`: 'Syne', 'Oswald', ou 'Impact', system-ui, sans-serif (Importe via Google Fonts: 'Space Grotesk' para títulos, 'Inter' para leitura, e 'JetBrains Mono' para métricas/tabelas/números).
- TIPOGRAFIA FLUIDA: Utilize `clamp()` para todos os títulos e tamanhos de fonte importantes. Limite os blocos de texto corrido a `65ch` para legibilidade ideal.
- PERFORMANCE DE ANIMAÇÃO (60fps): Anime EXCLUSIVAMENTE `transform` e `opacity`. Inclua suporte obrigatório a `@media (prefers-reduced-motion: reduce)`. Não aplique efeitos de fade-in genéricos em todos os elementos; crie uma revelação coordenada e elegante via `IntersectionObserver`.
- ACESSIBILIDADE (WCAG 2.1 AA): Garanta estados de `:focus-visible` nítidos com a cor `--accent-primary`, uso correto de `aria-expanded` e `aria-controls` em elementos interativos, e contraste impecável.

====================================================================
2. ARQUITETURA E SEÇÕES OBRIGATÓRIAS DA LANDING PAGE
====================================================================

1. HEADER FIXO COM BLUR & BARRA DE TELEMETRIA:
   - Barra superior fina informando: "GRAU DE PUREZA 99.9% • TESTADO EM LABORATÓRIO • MICRONIZADA 200 MESH".
   - Navbar com logotipo tipográfico forte ("KINETIC//CREA" ou similar), links de navegação suave (A Ciência, Calculadora, Benefícios, Mitos vs. Verdades, Planos) e um botão CTA rápido ("Calcular Minha Dose").

2. HERO SECTION ASSIMÉTRICA (ACIMA DA DOBRA):
   - Lado Esquerdo:
     * Badge técnico monoespaçado: `[ C4H9N3O2 • RESSÍNTESE DE ATP ]`.
     * Headline forte e orientada a resultado claro (sem clichês): Ex: "Mais Força Explosiva. Recuperação Celular Comprovada."
     * Subheadline explicando o mecanismo real da creatina no músculo e no cérebro.
     * Grupo de CTAs: Botão primário de alto contraste ("Adquirir Creatina Pura") + Botão secundário ("Simular Meus Ganhos").
     * Micro-provas sociais e selos técnicos (Ex: "4.9/5 (2.400+ atletas)", "Zero Calorias", "100% Vegana").
   - Lado Direito:
     * Composição visual rica construída com CSS/SVG (um card técnico interativo estilo "Rótulo Clínico 3D / Molécula & Scoop Precision" com indicadores flutuantes de pureza, solubilidade e aumento de +15% de carga máxima).

3. SEÇÃO: COMO FUNCIONA NO CORPO (TIMELINE / MECANISMO DO ATP):
   - Explique de forma visual e sequencial (Passo 1, Passo 2, Passo 3) o ciclo Fosfocreatina -> ADP -> ATP durante séries pesadas na academia.
   - Inclua um seletor interativo (Tabs em JS) onde o usuário alterna entre os benefícios:
     * [01. Hipertrofia & Força]
     * [02. Recuperação Entre Séries]
     * [03. Neuroproteção & Foco Cognitivo]
   - Cada aba deve atualizar dinamicamente métricas percentuais baseadas em estudos, tempo de ação e explicação fisiológica.

4. FERRAMENTA INTERATIVA PRINCIPAL: CALCULADORA DE DOSAGEM E SATURAÇÃO (JS PURO):
   - Construa um painel interativo onde o usuário insere:
     * Seu peso corporal (Slider + Input numérico em kg, ex: 40kg a 140kg).
     * Seu objetivo ("Manutenção Diária Padrão" vs. "Protocolo de Saturação Rápida 5-7 dias").
     * Nível de treino (Iniciante, Intermediário, Avançado).
   - O JavaScript deve calcular e exibir em tempo real:
     * Dose diária exata recomendada em gramas (fórmula científica: `peso * 0.07g` para manutenção personalizada vs. `0.3g/kg` dividido em 4 tomadas para saturação).
     * Quantidade equivalente em scoops dosadores.
     * Tempo estimado para saturação muscular total (ex: 21-28 dias no modo contínuo vs. 6 dias na saturação).
     * Consumo mensal estimado (em gramas) e qual pote apresenta o melhor custo-benefício.

5. TABELA NUTRICIONAL ESTILO "SWISS DESIGN" & COMPARATIVO DE MERCADO:
   - Um quadro estilizado como um rótulo nutricional de alta precisão (bordas de 1px e 4px no padrão FDA/ANVISA modernizado) mostrando: Porção de 3g, 3000mg de Creatina Monohidratada, 0g Carboidratos, 0g Sódio, 0g Aditivos.
   - Ao lado, uma tabela comparativa direta: "Nossa Creatina 100% Pura Micronizada" vs. "Creatinas Comuns com Maltodextrina/Impurezas".

6. MITOS VS. VERDADES CIENTÍFICAS (CARDS INTERATIVOS):
   - Desmistifique com dados científicos as 3 maiores dúvidas:
     1. "Creatina causa pedra nos rins?" (Verdade: Estudos de longo prazo mostram segurança total em indivíduos saudáveis).
     2. "Creatina engorda ou incha?" (Verdade: A retenção hídrica é EXCLUSIVAMENTE intracelular/intramuscular, deixando o músculo mais denso e volumoso, sem retenção subcutânea).
     3. "Preciso parar de tomar nos dias sem treino?" (Verdade: O efeito da creatina é crônico por saturação de estoque, deve ser tomada todos os dias).

7. VITRINE DE COMBOS / PLANOS COM SELETOR DE COMPRA:
   - 3 opções claras (1 Pote - 300g / Kit 2 Potes - Ciclo 6 Meses [Mais Vendido] / Kit 3 Potes - Performance Anual).
   - Toggle entre "Compra Única" e "Assinatura Inteligente (-15% OFF)".
   - Cálculo dinâmico do preço por dose (R$ por dia) atualizado via JavaScript.

8. PROVA SOCIAL & DEPOIMENTOS VERIFICADOS COM FILTRO:
   - Cards de avaliações reais com nome, modalidade (Musculação, Crossfit, Corrida/Endurance) e filtro simples via JS.

9. FAQ CIENTÍFICO (ACORDEÃO ACESSÍVEL):
   - Acordeão construído com JS puro, animações suaves e atributos `aria-expanded` corretos respondendo dúvidas sobre melhor horário para tomar, combinação com cafeína, creatina com carboidrato (pico de insulina), etc.

10. FOOTER COMPLETO + MODAL/DRAWER DE CHECKOUT SIMULADO:
    - Ao clicar nos botões de compra, abra um Drawer lateral elegante (Carrinho Interativo em JS) que permite ajustar a quantidade, ver o frete grátis destravado e simular a finalização do pedido com feedback visual na tela.

====================================================================
3. REQUISITOS TÉCNICOS DE ENTREGA
====================================================================
- Entregue todo o código (HTML, CSS dentro de `<style>` e JS dentro de `<script>`) perfeitamente organizado, indentado e funcional em um ÚNICO arquivo `.html` pronto para rodar no navegador.
- Todo o código JavaScript deve ser modularizado, livre de erros no console, com validação de inputs na calculadora e interações fluidas.
- Não utilize placeholders vazios como "Lorem Ipsum": escreva todo o copy em Português (Brasil) com vocabulário técnico real, persuasivo e cientificamente embasado sobre hipertrofia e fisiologia do exercício.
```

---

## Parte 4: Dicas Extras de Como Usar e Iterar esse Prompt

1. **Execução Direta:** Você pode copiar o bloco da **Parte 3** e colar diretamente aqui no chat (ou no seu editor com suporte a agentes como Cursor / Claude Code) dizendo: *"Execute este prompt e gere o arquivo HTML completo"*.
2. **Modularização Posterior:** Embora o prompt peça um arquivo único para facilitar a visualização imediata e zero configuração, o código é estruturado de forma limpa em blocos `<style>` e `<script>`, permitindo separar facilmente em `index.html`, `styles.css` e `app.js` caso queira subir em produção.
3. **Personalização de Marca:** Caso já tenha o nome da marca de suplementos, preços reais em Reais ($\text{R\$}$) ou uma cor específica de identidade visual, basta alterar a seção `1. SISTEMA DE TOKENS NO :root` e a seção `7. VITRINE DE COMBOS` antes de enviar o prompt.