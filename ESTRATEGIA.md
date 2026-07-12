# ESTRATÉGIA COMPLETA — Projeto Roblox de Alto Potencial Comercial

> Documento de estratégia nível estúdio. Objetivo: máximo lucro, viralização, retenção e escala.
> Restrição central de produção: **o jogo será 100% construído por IA** — portanto toda a direção de arte,
> conteúdo e sistemas foi desenhada para ser viável sem modelagem 3D complexa.
>
> Data da análise: Julho/2026.

---

## 1. ANÁLISE DE MERCADO (Roblox, 2025–2026)

### 1.1 Estado da plataforma

| Métrica | Valor (2025/2026) | Implicação estratégica |
|---|---|---|
| DAU global | ~144 milhões (Q4 2025, +69% a/a) | Mercado em plena expansão; espaço para novos entrantes |
| MAU global | ~381 milhões | Escala massiva de topo de funil |
| Receita 2025 | US$ 4,9 bi (+36%) / Bookings US$ 6,8 bi (+55%) | Gasto por usuário crescendo mais rápido que a base |
| Crescimento de gasto fora do Top 10 | 65% do crescimento de Robux veio da "cauda longa" (Q1 2026) | Jogos novos têm chance real — o algoritmo distribui tráfego |
| DevEx | US$ 0,0038/Robux (set/2025); **+42% para gasto de usuários 18+ verificados nos EUA em jogos R15** (jun/2026) | Cada Robux vale mais; público 18+ virou prêmio financeiro direto |
| Demografia | 35% <13 anos, 38% 13–17, 27% 18+ | O núcleo ainda é 8–17, mas o 18+ cresce +50% a/a e gasta ~40% mais por sessão |
| Novidades de plataforma | Assinaturas recorrentes in-experience; venda cross-game de passes desativada (mai/2026); Transfers API | Receita recorrente agora é ferramenta de primeira classe |

### 1.2 O que dominou 2025–2026

Dois arquétipos vencedores coexistem no topo:

1. **Jogos meme-rápidos, mobile-first, de loop simples** — *Grow a Garden* (pico de **21,3M CCU**, +21 bi de visitas no primeiro ano) e *Steal a Brainrot* (**25,8M CCU**, recorde histórico de QUALQUER jogo em QUALQUER plataforma, superando Fortnite). Características: entrada em <30 segundos, progresso offline, raridade/mutações, tensão social (roubo), estética simples, perfeitos para clipes de TikTok.
2. **Jogos de sessão longa e profundidade** — *Blox Fruits* (~300k CCU médio constante), *Fisch*, *99 Nights in the Forest*. Sessões de 45+ minutos, progressão de meses.

Outros dados estruturais:

- **Simuladores** são o gênero mais lucrativo e confiável (~4,3M CCU no gênero). O padrão dos vencedores: **3–4 loops entrelaçados** (coleta → upgrade → prestígio → trading), de modo que "entrei por 5 minutos" sempre encontra um loop prestes a completar. É isso que mantém o D30 anormalmente estável.
- **Tycoons** são o 2º maior gênero em CCU médio. O loop em si fabrica motivos de retorno diário — não dependem de viral.
- **Retenção é A métrica**: o algoritmo da home page do Roblox promove jogos com D1/D7 altos e bom tempo de sessão. Retenção ruim = invisibilidade, independente de marketing.
- **Mobile-first é obrigatório**: a maioria dos jogadores está no celular. *Grow a Garden* explodiu em parte porque roda perfeitamente em qualquer telefone.
- **Clipabilidade**: os hits de 2025/26 nasceram no TikTok. Mecânicas que geram momentos de "NÃO ACREDITO" (mutação ultra-rara, roubo bem-sucedido, evento global) são combustível de viral.

### 1.3 Padrões extraídos do Top 100 (princípios, não cópias)

| Padrão | Por que funciona | Exemplo de origem |
|---|---|---|
| **Progresso offline** | O jogo "trabalha para você" → culpa zero, retorno garantido ("o que cresceu enquanto dormi?") | Grow a Garden |
| **Raridade + mutações RNG** | Recompensa variável = dopamina; cada colheita é uma "caixa de loot" gratuita | Grow a Garden, Pet Sim |
| **Tensão social (roubo/risco)** | Emoção real entre jogadores → clipes, histórias, revanche | Steal a Brainrot |
| **Eventos globais de servidor** | "Está acontecendo AGORA" → picos de CCU sincronizados, FOMO saudável | Grow a Garden (climas) |
| **Trading entre jogadores** | Economia social = metajogo infinito, comunidade, YouTube de "trade" | Adopt Me, Pet Sim 99 |
| **Prestígio/rebirth** | Progressão infinita barata de produzir | Todos os simuladores |
| **Cadência semanal de update** | O algoritmo e a comunidade premiam consistência acima de qualidade pontual | Todos os líderes |
| **Nome-fórmula reconhecível** ("Grow a…", "Steal a…", "…Simulator") | CTR na busca e na home; o jogador já entende o jogo pelo título | Meta 2025/26 |

### 1.4 Oportunidades pouco exploradas (janelas abertas)

1. **"Grow + Steal" híbrido bem balanceado**: Grow a Garden não tem tensão social; Steal a Brainrot não tem profundidade de economia/coleção. Ninguém dominou o meio-termo com roubo *justo* (opt-in/protegível).
2. **Clãs com progressão coletiva** em jogos idle/grow: os líderes do gênero têm sistemas sociais rasos.
3. **Assinatura in-game** (ferramenta nova de 2026): pouquíssimos jogos do gênero a usam bem — receita recorrente é terreno quase virgem.
4. **Público 13–17 + 18+ casual**: o boost de 42% do DevEx para 18+ premia jogos que não parecem "de criancinha" — uma estética neutra (não infantil, não gore) captura os dois mundos.

---

## 2. IDEIAS CANDIDATAS

> Critério de avaliação: potencial comercial, aderência aos padrões vencedores e **viabilidade de construção por IA**
> (geometria simples, sistemas via código, zero dependência de modelagem orgânica/rigging).

### Ideia A — "Grow a Crystal" (fazenda de cristais com roubo e mutações)

Jogadores cultivam **cristais** em uma caverna pessoal. Cristais crescem em tempo real **inclusive offline**, sofrem **mutações RNG** (cores, brilhos, efeitos), podem ser colhidos, vendidos, fundidos ou **roubados** por outros jogadores em janelas de risco controladas. Economia de trading + clãs + eventos globais de clima mágico.

- **Por que tem potencial**: combina os DOIS maiores fenômenos da história da plataforma (crescimento offline + roubo) com a espinha dorsal de retenção dos simuladores (coleção/mutação/prestígio/trading). Cada padrão é comprovado individualmente; a combinação é a lacuna do item 1.4.1.
- **Público-alvo**: núcleo 9–16 anos, mobile; segunda camada 17+ casual (estética "gemas/neon" é neutra e satisfatória para adultos — mesmo apelo visual de jogos tipo "satisfying/ASMR" do TikTok).
- **Diferencial**: roubo **justo e protegível** (escudos, seguro, janelas), profundidade de fusão/crafting que os concorrentes não têm, clãs com metas coletivas.
- **Dificuldade de desenvolvimento (para IA): BAIXA-MÉDIA.** Cristal = 3–8 primitivas rotacionadas com material Neon/Glass + PointLight + partículas. Mutações = trocas de cor/material/partícula **via código**. Zero rigging, zero personagens, zero animação orgânica. É provavelmente o tema de maior apelo visual por unidade de complexidade geométrica que existe.
- **Viralização: ALTA.** Mutações ultra-raras anunciadas no servidor, roubos e vinganças, eventos de clima global = três geradores de clipe.
- **Monetização: ALTA.** Sementes premium, slots, escudos, autocoleta, passe sazonal, assinatura, cosméticos de caverna, pets-espírito.
- **Riscos**: mercado saturado de "Grow a…" (mitigação: diferenciais reais + execução acima da média); balanceamento do roubo pode frustrar (mitigação: design opt-in/protegível detalhado na seção 4).

### Ideia B — "Idle Empire Tycoon" (tycoon idle de império industrial)

Tycoon clássico de esteiras/droppers com camada idle profunda, rebirth infinito e fusão de máquinas.

- **Potencial**: gênero nº 2 em CCU, retorno diário embutido no loop. Público 8–14. Diferencial: fusão de máquinas com RNG.
- **Dificuldade para IA: MUITO BAIXA** (blocos, cilindros, esteiras — o gênero mais "primitivo-friendly" que existe).
- **Viralização: MÉDIA-BAIXA.** Tycoons crescem por retenção, não por clipe. Sem tensão social, sem momentos "inacreditáveis".
- **Monetização: MÉDIA.** Boosts e skips funcionam, mas sem trading/coleção o teto de gasto por baleia é menor.
- **Riscos**: oceano vermelho de tycoons genéricos; difícil furar a bolha sem viral.

### Ideia C — "Caso/Unboxing Colecionável" (jogo de abrir caixas + índice + trading)

Jogo quase 100% UI: abrir "caixas/ovos/geodos" com raridades, completar índice, tradear.

- **Potencial**: gacha é o motor de monetização mais forte que existe; UI pura = trivial para IA.
- **Viralização: MÉDIA.** Clipes de "puxei o item 1/1M" funcionam, mas o formato é raso.
- **Riscos: ALTOS.** Percepção de cassino → risco de moderação da plataforma (Roblox vem apertando políticas de simulated gambling), reputação "pay-to-spin", D30 fraco sem gameplay de sustentação. **Descartada como jogo standalone** — mas o *mecanismo* (abrir geodos raros) entra como subsistema da Ideia A.
- **Público**: 10–16.
- **Dificuldade para IA: MÍNIMA.**
- **Monetização: MUITO ALTA (mas frágil regulatoriamente).**

### Ideia D — "Meme Battler" (arena PvP de personagens-meme)

Surfar a onda brainrot/meme com arena casual.

- **Potencial**: memes = viral nato; foi o que levou Steal a Brainrot ao recorde mundial.
- **Riscos: FATAIS para nosso contexto.** (1) Personagens-meme exigem modelos 3D com personalidade + animação — exatamente o que IA não produz bem; (2) risco de IP/DMCA (a onda brainrot usa personagens de terceiros); (3) memes têm meia-vida curta — o jogo morre com a trend. **Descartada.**
- **Dificuldade para IA: ALTA.** **Viralização: MUITO ALTA.** **Monetização: MÉDIA.** **Público**: 9–15.

### 2.1 DECISÃO — A escolhida: **Ideia A, "Grow a Crystal"** (título de trabalho)

Justificativa em uma linha: **é a interseção máxima entre "padrões comprovados pelos dois maiores fenômenos da plataforma" e "aquilo que uma IA constrói com excelência"** (geometria primitiva + sistemas via código + beleza por material/luz/partícula, não por modelagem).

Sobre o nome: a fórmula "Grow a X" tem CTR comprovado na busca/home (o jogador entende o jogo pelo título). Alternativas a testar em A/B de ícone/título: *Crystal Caves*, *Grow a Gem*, *Mine & Mutate*. Recomendo lançar como **"Grow a Crystal 💎"** e iterar.

---

## 3. O JOGO — GAME DESIGN NÍVEL AAA

### 3.1 Visão geral

**Grow a Crystal** é um jogo de cultivo, coleção e economia social. Cada jogador possui uma **Caverna** pessoal (plot instanciado num servidor compartilhado com ~10–12 cavernas visíveis, como vilas vizinhas). Nela, planta **Sementes de Cristal** que crescem em tempo real — **inclusive offline**. Ao crescer, cada cristal rola **tamanho, qualidade e mutações** (RNG). O jogador colhe e decide: **vender** (moeda), **fundir** (crafting de cristais superiores), **expor** (buff passivo de status na caverna) ou **tradear**. Cristais expostos e maduros não colhidos podem ser **roubados** por outros jogadores em condições justas e protegíveis — a tensão social que gera clipes e retorno.

- **Plataformas**: mobile-first (tudo operável com um polegar), PC, console.
- **Estética**: cavernas escuras + cristais Neon/Glass + luz dinâmica + partículas = visual "satisfying" de alto impacto com geometria trivial. Direção de arte: "bioluminescência mágica", neutra em idade (agrada de 9 a 25 anos).
- **Classificação alvo**: Todas as idades / Leve. Sem violência, sem gore, sem apostas com Robux diretos.

### 3.2 Por que é 100% viável para IA construir

| Elemento | Como a IA produz |
|---|---|
| Cristais (centenas de variantes) | 3–8 primitivas (wedges, blocos rotacionados) agrupadas via script gerador; variação por escala/ângulo/cor/material. **Um gerador procedural em Luau produz o catálogo inteiro.** |
| Mutações | Puro código: troca de `Material`, `Color`, `ParticleEmitter`, `PointLight`, tamanho, som. Custo marginal ≈ zero por mutação nova. |
| Cavernas/mapa | Terrain do Roblox (esculpível via código/editor) + rochas primitivas. |
| Pets ("Espíritos") | Esferas/poliedros flutuantes com partículas e tween de flutuação — **sem rig, sem animação esquelética**. |
| UI (lojas, índice, trade, clãs) | 100% código — ponto forte absoluto de IA. |
| Economia/sistemas | 100% código + DataStores/MemoryStores. |
| Áudio | Biblioteca de áudio do próprio Roblox (licenciada). |
| Ícone/thumbnails | Screenshots in-game com pós-processamento (Bloom, DoF) — cristais fotografam bem; única possível contratação externa barata se necessário. |

**Nada no escopo exige modelagem orgânica, rigging, animação humana ou mesh complexo.**

### 3.3 Gameplay principal (loop primário — ciclo de 5 a 15 minutos)

1. **Plantar** sementes nos slots da caverna (10s).
2. **Cuidar** (opcional, acelera): regar com "Essência", aplicar fertilizantes, posicionar Espíritos.
3. **Crescer**: cada semente tem timer real (5 min a 48 h conforme tier). Durante o crescimento rola qualidade (tamanho ★1–★5) e mutações.
4. **Colher** no toque — momento de dopamina: revelação da qualidade/mutação com efeito visual/sonoro.
5. **Decidir**: vender / fundir / expor / tradear.
6. **Reinvestir**: sementes melhores, slots extras, decoração com buffs, Espíritos.

O jogador SEMPRE sai de uma sessão com sementes plantadas → **razão embutida de retorno**.

### 3.4 Gameplay secundário

- **Expedições de Roubo (PvP leve, seção 3.15)**: infiltrar cavernas alheias para colher cristais "maduros abandonados".
- **Fusão/Crafting (seção 3.8)**: combinar cristais em versões superiores.
- **Geodos**: pedras misteriosas que aparecem nas cavernas/eventos; quebrá-las (mini-jogo de toques) revela sementes raras, Espíritos ou poeira. É o "unboxing" da Ideia C, embutido de forma saudável (geodos são *ganhos*, compráveis apenas com moeda soft ou como conveniência).
- **Decoração da caverna**: móveis/luzes/fontes (primitivas + materiais) com **buffs funcionais** (decoração não é só estética → todo mundo decora → cavernas viram conteúdo social).
- **Pesca de Essência** (mini-loop AFK-friendly): poço de essência com coleta rítmica, para quem quer ficar online "sem fazer nada" (aumenta tempo de sessão e CCU).

### 3.5 Progressão do jogador

- **Nível de Jogador (1→∞)**: XP por colher, fundir, missões. Desbloqueia sistemas gradualmente (trade no nível 7, roubo no 10, clãs no 12) → FTUE limpo, anti-fraude de contas novas.
- **Tier de Caverna (1→10)**: expansões físicas do plot; cada tier abre slots, decoração e biomas de cultivo (cristais de gelo, vulcânicos, abissais — só material/cor/luz diferentes!).
- **Prestígio — "Ressonância" (infinito)**: reseta sementes/moeda comum mantendo coleção, Espíritos e cosméticos; concede **Fragmentos de Ressonância** (moeda de prestígio) e multiplicador permanente. Progressão infinita e barata de manter.

### 3.6 Economia completa e sistema de moedas

| Moeda | Origem | Uso | Papel |
|---|---|---|---|
| **Cristalinas** (soft) | Vender cristais, missões, diárias | Sementes, slots, decoração básica, escudos básicos | Motor do loop; inflação controlada por sinks |
| **Essência** (energia) | Regenera com tempo, poço de pesca, diárias | Regar/acelerar crescimento, expedições de roubo | Limitador de ritmo (energy system suave — nunca bloqueia o loop básico) |
| **Lumens** (hard/premium) | Compra com Robux, conquistas, eventos, passe | Sementes premium, geodos, escudos avançados, cosméticos, skips | Moeda de conversão; **sempre ganhável grátis em pequena quantidade** (percepção de justiça) |
| **Poeira Estelar** (crafting) | Reciclar cristais indesejados | Fusões, rerolls de mutação | Sink de excedente → protege a economia e dá valor ao "lixo" |
| **Fragmentos de Ressonância** (prestígio) | Ressonância | Multiplicadores permanentes, árvore de talentos | Progressão infinita |

**Princípios econômicos**: (1) toda moeda premium tem trilha gratuita; (2) sinks fortes (fusão, rerolls, decoração, clã) para evitar hiperinflação; (3) preços de trade flutuam por raridade real (contador global de existentes por mutação, exibido no índice — escassez transparente cria mercado saudável estilo Adopt Me).

### 3.7 Cristais: raridade e mutações (o coração da retenção)

- **6 raridades de semente**: Comum, Incomum, Rara, Épica, Lendária, Mítica.
- **Qualidade na colheita**: ★1–★5 (tamanho/valor).
- **Mutações (empilháveis, até 3)**: exemplos — *Luminoso* (glow), *Prismático* (arco-íris animado), *Sombrio*, *Gélido*, *Magmático*, *Estelar* (partículas), *Ecoante* (som), *Ancião* (cresceu 24h+ sem colher — recompensa o offline!), *Corrompido* (só durante evento Eclipse), **Puro (1/50.000)** — anunciado globalmente em TODOS os servidores.
- Tabela de chances **pública no índice** (transparência = confiança = menos churn por frustração).
- Combinatória: 40 espécies × 6 raridades × 5 qualidades × ~20 mutações = **dezenas de milhares de variantes colecionáveis a custo de produção ~zero** (tudo é recombinação procedural de cor/material/efeito).

### 3.8 Crafting (Fusão)

- **Fundir 3 cristais iguais** → 1 da raridade acima (com chance de herdar/ganhar mutação).
- **Reroll de mutação** com Poeira Estelar.
- **Receitas descobríveis** (combinações secretas → wiki/YouTube de comunidade — conteúdo gratuito de terceiros).
- **Forja de clã** (seção 3.17): fusões impossíveis solo.

### 3.9 Pets — "Espíritos" (sim, entram — com justificativa)

Pets são o segundo maior motor de retenção/monetização do gênero (colecionáveis + funcionais + tradeáveis). Aqui, **Espíritos** são orbes elementais flutuantes (esferas/poliedros + partículas — perfeitos para IA):

- **Função real** (não só cosmético): cada Espírito equipado dá buff (velocidade de crescimento, chance de mutação, defesa anti-roubo, auto-coleta parcial).
- Obtidos em geodos, eventos, fusão de espíritos e trade.
- Também têm raridades/mutações → segundo eixo de coleção.
- Limite de 3 equipados (evita power creep descontrolado); inventário expansível (monetização).

### 3.10 Missões

- **Tutoriais encadeados** (FTUE): 20 missões que ensinam cada sistema com recompensa imediata.
- **Missões de NPC "Guardião da Caverna"** (um cristal gigante falante — sem modelo humanoide!): arcos semanais de história leve.
- **Contratos**: pedidos rotativos ("entregue 3 cristais Gélidos ★3+") com recompensas escaladas — dá *propósito* ao cultivo além do lucro.

### 3.11 Sistema diário

- **Recompensa de login progressiva** (dia 1→7, reset semanal; dia 7 = geodo raro).
- **Streak de colheita**: colher ao menos 1 cristal/dia mantém streak; streak dá multiplicador de venda (+2%/dia até +30%). **Proteção de streak**: 1 falha perdoada a cada 7 dias (streak sem crueldade = FOMO saudável).
- **3 missões diárias** simples (5–10 min).
- **Clima diário**: cada dia real tem um clima global (ex.: "Névoa Prismática: +15% mutação Prismático hoje") → razão temática de logar HOJE.

### 3.12 Sistema semanal

- **Contrato Semanal Grande** (esforço de 3–4 sessões; recompensa: semente Lendária).
- **Meta de clã semanal** (seção 3.17).
- **Rotação da Loja do Viajante**: mercador com estoque semanal aleatório (sementes/decoração fora de temporada) — FOMO leve e recorrente.
- **Torneio semanal de leaderboard** (seção 3.18).

### 3.13 Eventos e temporadas

- **Eventos-surpresa de servidor (a cada 30–60 min)**: *Chuva de Meteoros* (geodos caem no mapa comum — todos saem das cavernas e socializam), *Eclipse* (10 min; única janela da mutação Corrompido), *Maré de Mana* (crescimento 2x por 15 min). Anunciados com sirene visual → picos de dopamina coletiva e clipes.
- **Eventos de calendário** (Halloween, Natal, verão…): espécie exclusiva + cosméticos limitados + mini-mecânica.
- **Temporadas (8 semanas)**: tema visual novo (bioma = paleta/materiais novos — barato!), passe de temporada free+premium (seção 4), espécies sazonais, leaderboard sazonal com troféus permanentes. **Cristais de temporadas passadas nunca voltam** → valor de colecionador crescente e economia de trade viva (o motor do Adopt Me).

### 3.14 Recompensas, conquistas e níveis

- **Conquistas (200+ no lançamento, geradas por template)**: marcos de coleção/fusão/roubo/social; dão Lumens (trilha grátis da moeda premium) e **títulos exibidos sobre o avatar** (status social = desejo).
- **Índice de Cristais ("Cristalopédia")**: registro permanente de cada variante já colhida, com % global de jogadores que a possuem → colecionismo infinito e comparável.
- **Marcos de índice**: 10/50/100/500 variantes → recompensas crescentes (inclui Espíritos exclusivos intradeáveis — prova de dedicação).

### 3.15 PvP ou PvE? — **PvE com PvP opcional e assimétrico (justificado)**

PvP direto de combate está descartado: exige balanceamento caro, gera toxicidade com público jovem e a IA sofre com animação de combate. Em vez disso, **PvP econômico assimétrico** (o padrão validado por Steal a Brainrot, refinado para ser justo):

- Cristais só ficam **rouváveis** se maduros e não colhidos por 30+ min (janela de negligência) E se a caverna não tiver escudo ativo.
- O ladrão gasta Essência para iniciar uma **Expedição** (custo de oportunidade), entra na caverna-alvo, e tem 60s para extrair 1 cristal — a extração emite luz/som visíveis; o dono (se online) ou seus Espíritos-guardiões podem interromper.
- Vítima recebe **Seguro parcial** (30% do valor) + notificação + botão "vingança" (expedição com desconto contra o ladrão) → transforma frustração em loop de engajamento.
- **Escudos**: grátis por tempo limitado diário, compráveis com soft currency, e convenientes via VIP — proteção nunca é exclusiva de pagante (justiça percebida).
- **Opt-out real**: modo "Caverna Pacífica" disponível — não pode roubar nem ser roubado, com bônus de venda levemente menor (-10%). Ninguém é forçado ao PvP; dados de Steal a Brainrot mostram que a maioria escolherá a tensão.

### 3.16 Matchmaking

Não há matchmaking competitivo. Servidores de 10–12 jogadores com **alocação inteligente**: prioriza amigos > membros do clã > mesmo idioma/região > nível similar. Isso maximiza laços sociais (o maior preditor de retenção de longo prazo).

### 3.17 Social, grupos e clãs

- **Visita livre**: qualquer caverna é visitável (like/estrelinhas em cavernas → ranking de decoração).
- **Presentes diários** entre amigos (1 semente/dia) → razão para adicionar amigos.
- **Clãs (20 membros)**: nome/bandeira/cor; **Caverna do Clã** compartilhada com plots coletivos; **Forja do Clã** (fusões exclusivas que exigem contribuição de vários membros); metas semanais coletivas com recompensa para todos; guerra de clãs *econômica* (qual clã produz mais valor na semana — sem combate).
- **Grupo Roblox oficial**: recompensa in-game por entrar no grupo (+5% venda) → base de notificação e marketing own-channel.
- **Chat de trade e praça central** no hub do servidor.

### 3.18 Ranking

- **Leaderboards globais e semanais**: valor colhido, índice completado, fusões, roubos bem-sucedidos, defesas.
- **Ranking sazonal com recompensas cosméticas** (troféus de caverna permanentes com o ano/temporada gravados — status histórico).
- **Ranking de clãs** com destaque na praça central.

### 3.19 Conteúdo de longo prazo

1. Temporadas de 8 semanas (motor principal — cada uma é ~80% recombinação procedural).
2. Ressonância infinita + árvore de talentos profunda.
3. Índice colecionável praticamente incompletável (novas espécies a cada temporada).
4. Economia de trade com escassez real (itens aposentados valorizam → metajogo de "investidor").
5. Novos biomas de cultivo (tier de caverna 11, 12… cada bioma = paleta nova, custo baixo).
6. Sistemas novos por trimestre no roadmap (seção 7).

---

## 4. ESTRATÉGIA DE MONETIZAÇÃO

> Filosofia: **"pay for convenience, never for power exclusivo"**. Tudo que um pagante consegue, um free player consegue com tempo (exceto cosméticos). Jogos percebidos como justos monetizam MAIS no longo prazo (Adopt Me e Grow a Garden provam).

### 4.1 Gamepasses (compra única — os "best value" percebidos)

| Gamepass | Preço (R$obux) | Efeito | Racional |
|---|---|---|---|
| **VIP** | 399 | +10% venda, tag dourada, escudo diário 2x, fila prioritária | Âncora clássica; melhor custo-benefício percebido |
| **Slots Duplos** | 499 | Dobra slots de plantio | Conveniência pura de maior demanda |
| **Auto-Coleta** | 349 | Espírito coletor automático (com delay — não elimina o gameplay) | O gamepass nº 1 de simuladores |
| **Mochila Infinita** | 249 | Inventário ilimitado | Remove atrito, não dá poder |
| **Teleporte Rápido** | 149 | Teleporte a qualquer caverna/amigo | Barato, alto volume |
| **Fusão Tripla** | 299 | 3 fusões simultâneas na forja | Conveniência de late game |

Regra pós-mai/2026: passes vendem apenas dentro do próprio jogo (venda cross-game foi desativada pela plataforma) → toda a vitrine é interna, com "loja" acessível em 1 toque.

### 4.2 Developer Products (consumíveis — o motor de receita recorrente)

- **Pacotes de Lumens**: 99 / 449 / 799 / 1.699 R$ (curva com bônus crescente; o 2º pacote é o "sweet spot" destacado).
- **Geodos premium** (equivalente a "ovos"): compráveis com Lumens — NUNCA diretamente com Robux (camada de abstração reduz percepção de gacha e risco de política).
- **Escudo 24h / 7 dias**.
- **Skip de crescimento** (proporcional ao tempo restante — nunca barato demais: o skip compete com o retorno amanhã, então é precificado para ser usado só em impaciência pontual).
- **Reroll de mutação premium**.
- **Ressonância instantânea** (para veteranos apressados).

### 4.3 Assinatura (ferramenta nova da plataforma — vantagem de pioneiro)

**"Pacto Lunar" — mensal (~R$ 9,90 equivalente em Robux):**
- 150 Lumens/mês + 1 geodo raro/semana + escudo diário automático + slot de semente exclusivo + aura cosmética de assinante.
- Desenhada para valer ~2x o preço em itens → conversão alta; receita previsível; a plataforma está promovendo ativamente jogos que adotam assinaturas (o boost de payout de 2026 favorece receita recorrente).

### 4.4 Cosméticos

- Skins de caverna (temas visuais completos = paleta/material — produção barata).
- Auras/trilhas de partícula para o avatar e para Espíritos.
- Efeitos de colheita (explosão de confete, raio, etc. — clipável = marketing pago pelo jogador!).
- Molduras de exposição, bases de troféu, pisos animados.

### 4.5 Itens limitados

- **1 cosmético limitado por temporada** (contador global visível de unidades vendidas).
- Espécies sazonais aposentadas para sempre → valorização em trade (FOMO saudável: o item continua existindo no trade, só não é mais *emitido*).

### 4.6 Eventos pagos

Nunca conteúdo bloqueado por pagamento. Eventos são grátis; a monetização do evento é **aceleração e cosmético** (ex.: no Halloween, todos jogam o evento; o pacote pago dá 2x tokens do evento + skin exclusiva).

### 4.7 Boosts e ofertas temporárias

- Boosts de 15 min–24 h (crescimento, sorte de mutação, valor de venda) — compráveis com Lumens E ganháveis grátis (diárias/eventos).
- **Boost de servidor**: um jogador compra, TODOS no servidor ganham +sorte 15 min (o comprador vira herói público → status social como motor de compra; padrão comprovado em Pet Sim).
- Ofertas relâmpago (4–24 h) segmentadas por comportamento.

### 4.8 Bundles e ofertas segmentadas (funil de conversão)

| Segmento | Oferta | Objetivo |
|---|---|---|
| **Novo jogador (D0–D3)** | "Kit do Fundador": 100 Lumens + semente Épica + escudo 3d por preço simbólico (~49 R$) | **Primeira compra é o evento mais importante do funil** — quem compra 1x tem LTV ~10x maior; o kit é deliberadamente o melhor negócio do jogo |
| **Engajado free (D7+, nível 15+, 0 compras)** | Oferta única do Kit + trial de 3 dias de Pacto Lunar | Converter o "quase-pagante" |
| **Pagante recorrente** | Bundles de temporada, limitados, pacotes maiores com bônus | Elevar ARPPU sem tocar no free |
| **Baleia (top 1% gasto)** | Cosméticos de ultra-prestígio, limitados numerados, caverna "penthouse" | Teto de gasto alto via status, não poder |
| **Churn risk (7+ dias ausente)** | Push/notificação + "presente de retorno" grátis ao logar + oferta de recuperação | Reativação |

**Funil**: Free → primeira compra (Kit) → consumíveis ocasionais (Lumens) → assinatura (recorrente) → passe sazonal → colecionador de limitados. Cada degrau tem uma oferta desenhada para o próximo.

### 4.9 Premium Payouts e o boost 18+

- Tempo de sessão de assinantes Roblox Premium gera payout passivo → tudo que aumenta duração de sessão (pesca de essência, eventos de servidor, praça social) também aumenta essa receita.
- Jogo construído em **R15** e com estética não-infantilizada para capturar o **DevEx +42% de gasto 18+ verificado (EUA)** — decisão de arquitetura tomada no dia 1, sem custo extra.

---

## 5. PLANO DE RETENÇÃO

### 5.1 Psicologia aplicada (mapa mecanismo → sistema)

| Princípio psicológico | Implementação no jogo |
|---|---|
| **Recompensa variável (Skinner)** | Toda colheita rola qualidade/mutação; geodos; clima diário. A "caixa de loot" central do jogo é GRÁTIS e infinita — a dopamina não está atrás de paywall |
| **Efeito Zeigarnik (tarefa incompleta)** | Sair do jogo SEMPRE com sementes crescendo; contratos a 80%; fusão na forja em progresso |
| **Aversão à perda (saudável)** | Cristais maduros não colhidos ficam rouváveis → "preciso voltar para colher" (mas com seguro de 30% — a perda nunca é devastadora) |
| **Reciprocidade social** | Presentes diários entre amigos; boost de servidor público |
| **Compromisso e consistência** | Streaks com proteção; metas de clã (não quero decepcionar o grupo) |
| **Status e comparação** | Títulos, troféus sazonais datados, ranking de decoração, % global no índice |
| **Curiosidade** | Receitas de fusão secretas; espécies não descobertas em silhueta no índice |

### 5.2 Metas por horizonte

- **Curto (hoje)**: diárias, colheita do que plantei ontem, clima do dia, streak.
- **Médio (semana)**: contrato semanal, meta de clã, torneio, loja do viajante, passe (níveis).
- **Longo (temporada/meses)**: completar índice da temporada, ranking sazonal, Ressonâncias, coleção de limitados, construção da caverna dos sonhos.

### 5.3 Mecânicas específicas de retorno

1. **Crescimento offline com relatório de retorno**: ao logar, tela "Enquanto você esteve fora: 12 cristais maduros, 1 mutação Estelar!" — o gancho nº 1 do gênero.
2. **Timers escalonados**: sementes de 5 min, 1 h, 8 h e 24 h plantadas juntas → sempre há algo pronto AGORA e algo pronto AMANHÃ.
3. **Eventos-surpresa** em horários semi-aleatórios → checagens espontâneas ("será que tem meteoro agora?").
4. **Notificações Roblox** (opt-in): cristal Mítico maduro, escudo expirando, presente de amigo, evento começando. Máx. 1/dia — notificação irritante = uninstall.
5. **FOMO saudável**: tudo que expira é cosmético/emissão (nunca poder); rotação volta em ciclos anunciados; streak tem perdão. FOMO cruel gera burnout e churn em 60 dias — nosso alvo é D180.
6. **Progressão infinita** via Ressonância + índice + trade (não existe "zerei o jogo").

### 5.4 Alvos de métricas

| Métrica | Alvo | Benchmark de decisão |
|---|---|---|
| D1 | ≥ 35% | <25% no soft launch = reformular FTUE antes de escalar |
| D7 | ≥ 18% | Gênero premia 15%+ |
| D30 | ≥ 8% | Simuladores top mantêm D30 "anormalmente flat" — nosso design copia essa estrutura |
| Sessão média | ≥ 25 min | Eventos de servidor + pesca AFK puxam isso |
| Sessões/dia | ≥ 2,5 | Timers escalonados são o driver |

---

## 6. PLANO DE CRESCIMENTO

### 6.1 Motor orgânico (algoritmo da home page)

O algoritmo do Roblox promove por: **D1/D7, tempo de sessão, taxa de conversão de impressão→play (ícone/título) e monetização por usuário**. Estratégia:

1. **Soft launch silencioso** (2–3 semanas): iterar FTUE até D1 ≥ 30% com tráfego pequeno. NÃO gastar tráfego/marketing com retenção ruim — é queimar a única primeira impressão do algoritmo.
2. **A/B contínuo de ícone e título** (o Roblox tem ferramenta nativa): cristais brilhantes + rosto de reação + 1 palavra de mutação rara. CTR do ícone é alavanca de crescimento tão importante quanto o jogo.
3. **Updates semanais SEMPRE no mesmo dia** (ex.: sexta 17h BRT/US after-school): a comunidade cria ritual; o algoritmo premia o pico recorrente.
4. **Compatibilidade total mobile + performance em celular fraco** (geometria primitiva ajuda!): a maioria dos jogadores está em telefones medianos.

### 6.2 Convites e viralidade embutida

- **Sistema de indicação**: convidado e convidante ganham (semente Épica para ambos quando o convidado atinge nível 10 — meta de nível evita fraude).
- **Presentes diários entre amigos** → razão mecânica para importar a lista de amigos.
- **Clãs recrutam sozinhos**: metas coletivas fazem membros chamarem amigos de fora (crescimento por pressão social positiva).
- **Boost de servidor público**: comprador vira herói → screenshot → share.

### 6.3 Máquina de conteúdo para criadores (TikTok/YouTube)

Momentos clipáveis **por design**:
1. Revelação de mutação rara (efeito visual explosivo + anúncio global com nome do jogador — o jogador filma a si mesmo ficando famoso).
2. Roubo e vingança (narrativa pronta de 60 segundos).
3. Eclipse/Chuva de Meteoros (evento coletivo caótico).
4. Trade de item aposentado valioso ("troquei meu cristal de 2026...").
5. Tours de caverna decorada (conteúdo calmo/ASMR para outra audiência).

Suporte ativo:
- **Programa de creator codes**: criador tem código; quem usa dá % de Lumens ao criador → exército de vendedores comissionados.
- **Kit de mídia** público (logos, fontes, efeitos de som) + servidor Discord com canal de criadores e acesso antecipado a updates.
- **Modo cinematográfico in-game** (esconder UI, câmera livre) — custo trivial, adorado por YouTubers.
- Semear 10–20 micro-influencers de Roblox (10k–100k inscritos, baratos) no lançamento em vez de 1 grande — mais horas totais de vídeo por custo.

### 6.4 Canais próprios

- Grupo Roblox (bônus por entrar) → anúncios de update para todos os membros.
- Discord da comunidade (eventos, sneak peeks, votações de espécies novas — cocriação gera lealdade).
- TikTok oficial do jogo com clipes das mutações "Puras" da semana (conteúdo gerado pelos próprios jogadores, re-postado).

---

## 7. ANÁLISE DE CONCORRÊNCIA

| Concorrente | Pontos fortes | Pontos fracos | Oportunidade que deixa aberta | Como superamos |
|---|---|---|---|---|
| **Grow a Garden** (21M CCU pico) | Loop offline perfeito; mobile; simplicidade; marca da fórmula "Grow a" | Zero tensão social; profundidade rasa (sem clã forte, crafting raso); dependente de novidade | Jogador que ama o loop mas quer *mais jogo* | Mesmo conforto de cultivo + roubo justo + fusão + clãs + trade profundo |
| **Steal a Brainrot** (25,8M CCU recorde) | Tensão social geradora de clipes; meme-power; simplicidade brutal | Frustração de perder sem proteção; base em IP de meme (risco legal/moda); economia rasa; meia-vida de trend | Roubo *justo* e sustentável, desacoplado de memes de terceiros | Roubo com escudos/seguro/vingança + IP próprio atemporal (cristais) |
| **Pet Simulator 99 / BIG Games** | Execução impecável; economia de trade madura; eventos constantes; máquina de updates | Complexidade acumulada intimida novatos; percepção de gacha pesado; exige equipe gigante | Entrada simples com teto profundo | FTUE de 60 segundos; gacha só periférico (geodos ganháveis); nossa cadência procedural barateia updates |
| **Adopt Me** | Economia de trade lendária; escassez que valoriza; audiência fiel | Envelhecido; loop principal fraco (o trade É o jogo); crescimento estagnado | Trade forte APOIADO num loop de gameplay forte | Trade + escassez sazonal sobre um loop de cultivo/roubo vivo |
| **Blox Fruits** | Profundidade de meses; sessões longas; base fiel 13–17 | Exige combate/animação complexos (impossível para IA); onboarding hostil; pesado em mobile | — (arquétipo diferente) | Não competimos; capturamos o mesmo 13–17 com sessões longas via economia, não combate |
| **Fisch / 99 Nights** | Sessão longa, vibe "chill/deep" que cresceu em 2026 | Nicho de ritmo lento; menos viral | Público "chill" também joga jogos de cultivo | Nossa pesca de essência e decoração servem o jogador chill dentro do mesmo jogo |

**Síntese**: nenhum líder combina (a) cultivo offline, (b) roubo justo, (c) coleção/fusão profunda, (d) trade com escassez e (e) clãs coletivos. Cada um domina 1–2 desses eixos. Nossa aposta é a interseção — com custo de produção estruturalmente menor (procedural + IA).

---

## 8. ROADMAP

### MVP (semanas 1–6) — "o loop tem que viciar sozinho"
- Caverna pessoal + 12 espécies × 4 raridades, crescimento com timers reais + **offline**.
- Colheita com qualidade ★ e 6 mutações; venda; loja de sementes; Cristalinas + Essência.
- FTUE (10 missões); diárias + streak; 1 clima diário global.
- DataStore robusto (sessão-lock, backup — perda de save mata jogos deste gênero).
- UI mobile-first completa. **Nada de trade/roubo/clã ainda.**
- *Meta interna: D1 ≥ 25% com playtest fechado.*

### Alpha (semanas 7–10) — retenção profunda
- Fusão + Poeira Estelar; geodos + Espíritos (8 tipos); Cristalopédia; conquistas v1.
- Slots/tiers de caverna 1–5; decoração com buffs v1.
- Eventos de servidor (Meteoros, Maré de Mana); Lumens + primeiras ofertas (Kit do Fundador, 3 gamepasses core).
- *Soft launch silencioso, 1–2k jogadores; iterar FTUE até D1 ≥ 30%.*

### Beta (semanas 11–16) — social e economia
- **Roubo (Expedições) + escudos + seguro + vingança + modo Pacífico.**
- Trade seguro (confirmação dupla, log anti-scam); presentes entre amigos; sistema de indicação.
- Clãs v1 (caverna coletiva, meta semanal); leaderboards; Ressonância (prestígio) v1.
- Assinatura Pacto Lunar; passe de temporada (infra).
- *Meta: D7 ≥ 15%, sessão ≥ 20 min, primeiras compras validando funil.*

### Lançamento (semana 17–18)
- Temporada 1 completa (tema + passe + limitado + espécies sazonais + Eclipse/Corrompido).
- Campanha: 10–20 micro-influencers + creator codes + Discord aberto + A/B de ícone rodando.
- Updates semanais travados no calendário a partir daqui. **Sempre.**

### Meses 1–3 pós-lançamento
- Temporada 2; guerra econômica de clãs; ranking de decoração; torneios semanais.
- Loja do Viajante; ofertas segmentadas por comportamento (funil completo da seção 4.8).
- Balanceamento econômico guiado por dados (sinks/sources); ferramentas anti-exploit/anti-dupe (crítico para a economia de trade).
- Localização: PT-BR, ES, ID, TH, FIL (mercados mobile gigantes e baratos de atingir; tradução é tarefa perfeita para IA).

### Meses 4–6
- Biomas 2 e 3 (tiers de caverna 6–10); árvore de talentos de Ressonância; forja de clã plena.
- Evento de plataforma (participar de eventos oficiais Roblox quando abrirem — tráfego grátis).
- Programa formal de creators; mercado de trade com histórico de preços (transparência = confiança).
- *Meta: estabilizar 15–30k CCU médio.*

### Ano 1
- 4–5 temporadas concluídas; espécies nº 100+; sistema de "exposições/museus" públicos de coleção.
- Segundo modo AFK-friendly (jardins zen de essência) para tempo de sessão.
- Explorar Transfers API para economia inter-jogadores dentro das regras da plataforma.
- Avaliar spin-off da marca (mesma IP de cristais) SOMENTE se CCU estável > 50k — antes disso, todo recurso no jogo principal.

---

## 9. AVALIAÇÃO HONESTA (0–10)

| Critério | Nota | Justificativa fria |
|---|---|---|
| **Potencial de lucro** | 8,5 | Gênero comprovadamente nº 1 em receita; funil completo (passes+consumíveis+assinatura+temporadas); teto real depende de execução da economia de trade |
| **Potencial de viralização** | 7,5 | Três geradores de clipe por design; mas viral nunca é garantido — o plano NÃO depende dele (retenção carrega o crescimento orgânico) |
| **Facilidade de desenvolvimento** | 8,5 | Deliberadamente desenhado para IA: primitivas + materiais + código. O risco técnico real é backend (DataStores, anti-dupe, segurança de trade) — difícil, mas é *código*, o forte da IA |
| **Escalabilidade** | 9 | Conteúdo procedural (espécies/mutações/temporadas = recombinação); custo marginal de update baixíssimo; servidores pequenos escalam horizontalmente |
| **Retenção** | 9 | Copia a arquitetura exata dos jogos com D30 mais estável da plataforma (loops empilhados + offline + social) e corrige as frustrações deles |
| **Monetização** | 8,5 | "Pay for convenience" com funil segmentado + assinatura pioneira; perde 1,5 ponto por recusar deliberadamente as práticas mais agressivas (gacha hard) — troca consciente de teto por longevidade |
| **Longevidade** | 8 | Temporadas + escassez + trade + prestígio infinito = estrutura de anos; risco: fadiga da fórmula "grow" no mercado (mitigada por profundidade que os trend-games não têm) |

**Riscos honestos que podem matar o projeto** (e mitigação):
1. **FTUE ruim** → soft launch obrigatório com gate de D1 ≥ 30% antes de qualquer marketing.
2. **Exploit/dupe na economia de trade** → trade só na Beta, com logs, confirmação dupla e validação server-side de tudo desde o dia 1.
3. **Perda de saves** → sessão-lock + backups versionados antes do soft launch (inegociável).
4. **Roubo frustrar demais** → todos os diais (janela, seguro, escudo) em config remota para ajuste sem deploy; modo Pacífico desde o início.
5. **Saturação do gênero** → nossa vantagem não é a ideia, é o custo estrutural: updates semanais procedurais que estúdios manuais não sustentam.

---

## 10. RESUMO EXECUTIVO

Construir **"Grow a Crystal"**: um jogo de cultivo offline de cristais com mutações RNG, roubo justo opt-in, fusão, trading com escassez sazonal, clãs cooperativos e temporadas de 8 semanas — mobile-first, R15, estética neon/bioluminescente feita de primitivas + materiais + partículas (100% construível por IA), monetizado por conveniência (gamepasses core + Lumens + assinatura Pacto Lunar + passes sazonais) com funil segmentado do free ao colecionador. Lançar via soft launch com gate de retenção, crescer pelo algoritmo (D1/sessão) + máquina de clipes por design + creator codes, e sustentar com updates semanais de custo marginal baixo. A tese: **a interseção dos padrões dos dois maiores fenômenos da história da plataforma, executada com a estrutura de retenção dos simuladores mais lucrativos, a um custo de produção que só produção procedural via IA permite.**
