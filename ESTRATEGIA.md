# ESTRATÉGIA COMPLETA — "Steal a Crystal" (título de trabalho)

> Documento de estratégia nível estúdio. Objetivo: máximo lucro, viralização, retenção e escala.
> Restrição central de produção: **o jogo será 100% construído por IA** — portanto toda a direção de arte,
> conteúdo e sistemas foi desenhada para ser viável sem modelagem 3D complexa.
>
> Data da análise: Julho/2026 · **Revisão 2** (pivô de design: de "cultivo de sementes" para
> "mineração ativa + galeria de renda + roubo pegar-e-correr", por direção do product owner).

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
- **Clipabilidade**: os hits de 2025/26 nasceram no TikTok. Mecânicas que geram momentos de "NÃO ACREDITO" (drop ultra-raro, roubo bem-sucedido, evento global) são combustível de viral.

### 1.3 Padrões extraídos do Top 100 (princípios, não cópias)

| Padrão | Por que funciona | Exemplo de origem |
|---|---|---|
| **Progresso offline** | O jogo "trabalha para você" → culpa zero, retorno garantido ("quanto rendeu enquanto dormi?") | Grow a Garden |
| **Raridade + mutações RNG** | Recompensa variável = dopamina; cada mineração é uma "caixa de loot" gratuita | Grow a Garden, Pet Sim |
| **Tensão social (roubo/risco)** | Emoção real entre jogadores → clipes, histórias, revanche | Steal a Brainrot |
| **Renda por item exposto + coleta física na base** | Loop tátil de "voltar para coletar"; a riqueza fica VISÍVEL (status + alvo) | Steal a Brainrot |
| **Eventos globais de servidor** | "Está acontecendo AGORA" → picos de CCU sincronizados, FOMO saudável | Grow a Garden (climas) |
| **Trading entre jogadores** | Economia social = metajogo infinito, comunidade, YouTube de "trade" | Adopt Me, Pet Sim 99 |
| **Prestígio/rebirth** | Progressão infinita barata de produzir | Todos os simuladores |
| **Cadência semanal de update** | O algoritmo e a comunidade premiam consistência acima de qualidade pontual | Todos os líderes |
| **Nome-fórmula reconhecível** ("Grow a…", "Steal a…", "…Simulator") | CTR na busca e na home; o jogador já entende o jogo pelo título | Meta 2025/26 |

### 1.4 Oportunidades pouco exploradas (janelas abertas)

1. **"Steal" com loop de aquisição PRÓPRIO**: em Steal a Brainrot, itens vêm de uma esteira de compra (RNG passivo de loja). Ninguém combinou o roubo com um **loop ativo e habilidoso de obtenção** (mineração com profundidade) — que dá ao jogador orgulho do que ele exibe e dor real quando perde.
2. **Clãs com progressão coletiva** nesse gênero: os líderes têm sistemas sociais rasos.
3. **Assinatura in-game** (ferramenta nova de 2026): pouquíssimos jogos do gênero a usam bem — receita recorrente é terreno quase virgem.
4. **Público 13–17 + 18+ casual**: o boost de 42% do DevEx para 18+ premia jogos que não parecem "de criancinha" — a fantasia de "roubo de diamantes/assalto a galeria" é universalmente compreendida (filmes de heist) e não é infantil nem violenta.

---

## 2. IDEIAS CANDIDATAS

> Critério de avaliação: potencial comercial, aderência aos padrões vencedores e **viabilidade de construção por IA**
> (geometria simples, sistemas via código, zero dependência de modelagem orgânica/rigging).

### Ideia A — Mineração de cristais + galeria de renda + roubo (título de trabalho: "Steal a Crystal")

Jogadores mineram minérios numa **caverna compartilhada em camadas**, com chance aleatória de extrair **joias** de raridades e mutações diferentes. As joias são exibidas em **pedestais na base pessoal (galeria)** e geram **renda por segundo**, coletada pisando numa **plaquinha**. Joias expostas podem ser **roubadas** por outros jogadores no estilo pegar-e-correr — com escudos, armadilhas e alarmes como defesa. Fusão, lapidação, trade, clãs e temporadas completam o metajogo.

- **Por que tem potencial**: combina os DOIS maiores fenômenos da história da plataforma (renda por item exposto + roubo, do recordista mundial; progresso offline e mutações, do maior jogo atual) e corrige a fraqueza central do recordista: lá, os itens vêm de compra passiva — aqui, o jogador **conquista** cada joia minerando, o que multiplica o apego (e a dor do roubo, e o clipe da vingança).
- **Público-alvo**: núcleo 9–16 anos, mobile; segunda camada 17+ casual (fantasia de heist + visual de gemas é neutro em idade).
- **Diferencial**: loop ativo de mineração com profundidade (camadas + picaretas), lapidação/fusão, trade com escassez, clãs — nada disso existe nos "Steal a X".
- **Dificuldade de desenvolvimento (para IA): BAIXA-MÉDIA.** Cristal/minério = 3–8 primitivas rotacionadas com material Neon/Glass + PointLight + partículas. Mutações = trocas de cor/material/partícula **via código**. Zero rigging, zero personagens, zero animação orgânica.
- **Viralização: ALTA.** Roubos e perseguições, drops ultra-raros anunciados globalmente, eventos de caverna = três geradores de clipe.
- **Monetização: ALTA.** Picaretas/mochilas/pedestais (conveniência), escudos, poções de sorte, passe sazonal, assinatura, cosméticos, Espíritos.
- **Riscos**: meta "Steal a X" saturada de clones rasos (mitigação: profundidade real que clones não sustentam); frustração de perder item raro (mitigação: seção 3.7); balanceamento rico-vs-novato (mitigação: servidores por faixa de patrimônio + proteção de novato).

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
- **Riscos: ALTOS.** Percepção de cassino → risco de moderação da plataforma (Roblox vem apertando políticas de simulated gambling), reputação "pay-to-spin", D30 fraco sem gameplay de sustentação. **Descartada como jogo standalone** — mas o *mecanismo* (geodos raros que caem minerando) entra como subsistema da Ideia A.
- **Público**: 10–16.
- **Dificuldade para IA: MÍNIMA.**
- **Monetização: MUITO ALTA (mas frágil regulatoriamente).**

### Ideia D — "Meme Battler" (arena PvP de personagens-meme)

Surfar a onda brainrot/meme com arena casual.

- **Potencial**: memes = viral nato; foi o que levou Steal a Brainrot ao recorde mundial.
- **Riscos: FATAIS para nosso contexto.** (1) Personagens-meme exigem modelos 3D com personalidade + animação — exatamente o que IA não produz bem; (2) risco de IP/DMCA (a onda brainrot usa personagens de terceiros); (3) memes têm meia-vida curta — o jogo morre com a trend. **Descartada.**
- **Dificuldade para IA: ALTA.** **Viralização: MUITO ALTA.** **Monetização: MÉDIA.** **Público**: 9–15.

### 2.1 DECISÃO — A escolhida: **Ideia A, "Steal a Crystal"** (título de trabalho)

Justificativa em uma linha: **é a interseção máxima entre "padrões comprovados pelos dois maiores fenômenos da plataforma" e "aquilo que uma IA constrói com excelência"** (geometria primitiva + sistemas via código + beleza por material/luz/partícula, não por modelagem) — com um loop de aquisição ativo que nenhum "Steal a X" tem.

**Validação de colisão (verificada em jul/2026):** já existe **"Grow Crystals! 💎"** (Fun Growing Games, criado em dez/2024, 50M+ visitas) — um clone direto de Grow a Garden com tema de cristais: plantar, crescimento offline e mineradores passivos. É um jogo de porte médio (tem cobertura de sites de códigos, mas não aparece em nenhum ranking de topo). Duas consequências:

1. **O nome "Grow a Crystal" está queimado** — lançaríamos como "clone do clone", competindo pelos mesmos termos de busca contra um incumbente com SEO estabelecido.
2. **A demanda pelo tema está validada** — e a rasidão do incumbente (sem roubo, sem trade, sem fusão, sem clãs, sem temporadas) confirma exatamente a nossa tese de diferenciação.

**Decisão de nome: posicionar no eixo diferenciador — "Steal a Crystal 💎"** (título de trabalho). A fórmula "Steal a X" tem CTR comprovado pelo maior recorde de CCU da história e, na verificação de jul/2026, **o nicho "Steal a Crystal" está livre**. A fantasia de "roubar diamantes" é culturalmente famosa (filmes de assalto) — o título explica o jogo sozinho. Alternativas para A/B de ícone/título: *Steal a Gem*, *Steal a Diamond*, *Crystal Heist*. **Regra de processo: revalidar a disponibilidade do nome na semana do lançamento** — ondas de clones se movem rápido nesta meta.

---

## 3. O JOGO — GAME DESIGN NÍVEL AAA

> Decisões de design travadas com o product owner (jul/2026):
> **(1)** roubo estilo **pegar-e-correr** (pega do pedestal e corre para a própria base);
> **(2)** caverna de mineração **compartilhada, com camadas de profundidade** travadas por tier de picareta;
> **(3)** renda da galeria **acumula offline com teto** expansível;
> **(4)** defesa por **empurrão + armadilhas + perks compráveis** (alarme, etc.).

### 3.1 Visão geral

**Steal a Crystal** é um jogo de mineração, coleção, renda passiva e roubo social. Cada jogador tem uma **base-galeria** num mapa compartilhado: joias expostas em **pedestais** geram **renda por segundo**, coletada pisando numa **plaquinha de coleta**. As joias vêm da **Caverna** — uma área do mesmo mapa, distante das bases, acessada por teleporte ao encostar na entrada — onde o jogador minera nós de minério com chance aleatória de extrair joias de diferentes espécies, raridades e mutações. **Toda joia exposta pode ser roubada** por outro jogador, que precisa pegá-la do pedestal e correr de volta à própria base para ficar com ela. Expor rende; guardar protege — **a tensão entre renda e risco é o coração do jogo**, e minerar na caverna significa deixar a galeria momentaneamente sem vigia.

- **Plataformas**: mobile-first (tudo operável com um polegar), PC, console.
- **Estética**: rochas escuras + joias Neon/Glass + luz dinâmica + partículas = visual "satisfying" de alto impacto com geometria trivial. Direção de arte: "heist de luxo subterrâneo", neutra em idade (agrada de 9 a 25 anos).
- **Classificação alvo**: Todas as idades / Leve. Sem violência com dano (empurrão/armadilhas cômicas), sem gore, sem apostas com Robux diretos.

### 3.2 Por que é 100% viável para IA construir

| Elemento | Como a IA produz |
|---|---|
| Joias/cristais (centenas de variantes) | 3–8 primitivas (wedges, blocos rotacionados) agrupadas via script gerador; variação por escala/ângulo/cor/material. **Um gerador procedural em Luau produz o catálogo inteiro.** |
| Nós de minério | Rochas (esferas/blocos deformados) com cristais embutidos; quebram em estágios via troca de mesh/escala + partículas. |
| Mutações | Puro código: troca de `Material`, `Color`, `ParticleEmitter`, `PointLight`, tamanho, som. Custo marginal ≈ zero por mutação nova. |
| Mapa (bases + caverna em camadas) | Terrain do Roblox + primitivas; camadas são regiões em profundidades diferentes do mesmo place, conectadas por portais/túneis. |
| Bases/pedestais/plaquinha | Blocos, cilindros, neon, SurfaceGui — o layout "fileira de bases" é o mais simples do gênero. |
| Armadilhas (jaula, laser, piso lento) | Primitivas + Touched events + tweens. Cômicas por design — não exigem animação. |
| Picaretas | Ferramenta = cabo (cilindro) + cabeça (wedges); "animação" de golpe via tween de CFrame — padrão consagrado, sem rig. |
| Espíritos (pets) | Esferas/poliedros flutuantes com partículas e tween de flutuação — **sem rig, sem animação esquelética**. |
| UI (lojas, índice, trade, clãs) | 100% código — ponto forte absoluto de IA. |
| Economia/sistemas | 100% código + DataStores/MemoryStores. |
| Áudio | Biblioteca de áudio do próprio Roblox (licenciada). |
| Ícone/thumbnails | Screenshots in-game com pós-processamento (Bloom, DoF) — joias fotografam bem. |

**Nada no escopo exige modelagem orgânica, rigging, animação humana ou mesh complexo.**

### 3.3 O mapa

- **Distrito das bases**: um "quarteirão" retangular compacto — **10–12 bases** em fileira dupla ao longo de uma rua central (layout validado pelo gênero: qualquer base está a segundos de corrida de qualquer outra — essencial para o pegar-e-correr funcionar). Cada base: galeria de pedestais, plaquinha de coleta, bancada de lapidação/fusão, armazém, slots de armadilha e painel de upgrades.
- **Entrada da Caverna**: portal no fim da rua; **encostar teleporta** o jogador para a região da mina — mesmo place/servidor, geograficamente distante (sem loading, sem troca de servidor; o ladrão e a vítima coexistem sempre no mesmo mundo).
- **Praça central**: spawn, loja, mural de rankings, NPC de contratos (um golem de pedra/cristal — sem modelo humanoide).

### 3.4 Loop principal (ciclo de 5–15 minutos)

1. **Minerar** na Caverna: quebrar nós de minério (toques/cliques) → drops de minério comum + chance de **joia bruta** (RNG de espécie/raridade/mutação — o momento-dopamina nº 1).
2. **Mochila enche** (capacidade limitada, upgradável) → voltar à base.
3. **Decidir por joia**: **lapidar** (bancada: valoriza e define qualidade ★) → **expor** no pedestal (gera renda/s, mas fica roubável) / **guardar** no armazém (segura, rende zero) / **fundir** (3 iguais → tier acima) / **vender** / **tradear**.
4. **Coletar renda** pisando na plaquinha (som de moedas + números voando — tátil e satisfying).
5. **Reinvestir**: picareta melhor (destrava camada mais funda), mochila, pedestais, armadilhas, perks, Espíritos.
6. **Roubar/defender** (a qualquer momento): a rua está viva — oportunidades e ameaças constantes.

O jogador SEMPRE sai de sessão com renda acumulando (teto offline) e metas de picareta/camada → **razão embutida de retorno**.

### 3.5 Mineração em detalhe

- **Nós de minério**: rochas com HP; cada golpe de picareta tira HP e solta partículas/fragmentos; ao quebrar, dropam minério + rolagem de joia. Respawn por região em 30–90s (servidor gerencia densidade — sem "seca" nem farm infinito num nó).
- **10 camadas de profundidade** (tema/paleta por camada — barato de produzir): 1-Pedreira (cobre/quartzo) → 2-Grutas (ametista) → 3-Rio Subterrâneo (safira) → 4-Câmara de Magma (rubi) → 5-Jardim de Cristal (esmeralda) → 6-Abismo Gelado (topázio glacial) → 7-Fenda Ecoante (opala) → 8-Coração da Terra (diamante) → 9-Vazio (ônix estelar) → 10-Origem (prisma primordial). Camadas novas por temporada expandem verticalmente para sempre.
- **Acesso por tier de picareta** (12 tiers; compradas com dinheiro + minérios da camada anterior — sink duplo e progressão tátil). Ver outro jogador numa camada acima da sua = aspiração visível.
- **Perigos ambientais (sem HP/morte)**: gêiseres que arremessam, lava que faz derrubar parte do minério carregado, gelo escorregadio, zonas escuras que pedem lanterna (equipamento). Risco cômico, não punitivo.
- **Eventos de caverna (a cada 30–60 min, anunciados com sirene)**: *Veio Dourado* (nós dourados de alto rendimento spawnam por 5 min), *Chuva de Meteoros* (meteoros com minério raro caem na área da entrada — todos correm juntos), *Eclipse* (10 min; única janela da mutação Corrompido), *Terremoto* (abre fendas temporárias que dão acesso de 3 min à camada seguinte — "gostinho" do futuro que vende progressão como nenhum tutorial).
- **Trade-off central**: minerar = enriquecer, mas sua galeria fica sem o dono por perto. O jogo inteiro respira essa escolha.

### 3.6 A base-galeria e a renda

- **Pedestais**: começam 4, expansíveis até 24+ (upgrades + gamepass). Cada joia exposta rende `renda/s = base(raridade) × qualidade(★) × (1 + soma de mutações) × bônus de coleção × buffs`. **Bônus de coleção**: expor 3+ joias da mesma espécie ou um "conjunto" (ex.: rubi+safira+esmeralda) dá multiplicador — incentiva curadoria da galeria, não só empilhar o mais caro.
- **Plaquinha de coleta**: piso luminoso na entrada; pisar coleta tudo com feedback audiovisual generoso. **Renda acumula offline até um teto** (base: 2h de produção; upgrades de "Cofre" expandem até 8h; VIP +50%) → gancho de retorno múltiplo diário sem quebrar a economia.
- **Armazém**: capacidade limitada (upgradável) de joias guardadas em segurança — rende zero. A decisão "expor ou guardar" é individual por joia e reversível a qualquer momento (na base).
- **Upgrades de base**: pedestais, cofre (teto offline), armazém, slots de armadilha, decoração com micro-buffs (tapetes, lustres, vitrines — primitivas + neon; galeria bonita = status = alvo = clipe).

### 3.7 Roubo e defesa (o coração social)

**O roubo (pegar-e-correr):**
1. Qualquer jogador entra em qualquer base pela porta (sem barreira quando sem escudo).
2. Interagir com um pedestal por **2,5s de canalização** (barra visível; o ladrão fica vulnerável e iluminado) arranca a joia.
3. Carregando a joia: **-20% velocidade**, um **feixe de luz vertical** marca o ladrão no mapa (todos veem), e ele não pode usar o portal da caverna.
4. Chegou na **própria plaquinha** → a joia é dele (transferência real de propriedade). Foi **empurrado** no caminho → derruba a joia, que fica 10s no chão (qualquer um pega, inclusive a vítima) e depois **volta sozinha ao pedestal de origem**.
5. **Cooldown de roubo** (60s entre tentativas por jogador) e **limite de 1 joia carregada** por vez.

**A defesa:**
- **Empurrão** (ferramenta padrão de todos, cooldown 3s): derruba ladrões — cômico, sem dano.
- **Armadilhas** (slots na base, compradas com dinheiro do jogo): *Jaula* (prende 3s), *Laser* (arremessa para fora), *Piso de Cola* (lentidão), *Ventilador* (empurra). Posicionamento livre = expressão estratégica.
- **Perks compráveis** (dinheiro do jogo; premium só acelera, nunca exclusiva):
  - **Alarme** — notificação sonora/visual global para o dono quando alguém entra na base (inclusive com o dono na caverna: "SUA BASE ESTÁ SENDO INVADIDA") + destaque vermelho no invasor. Tiers: alcance/antecedência.
  - **Rastreador** — após ser roubado, marca o ladrão por 10 min para **vingança** (roubo contra ele sem cooldown e com canalização 50% mais rápida). Transforma frustração em gameplay.
  - **Seguro** — recupera 25% do valor de venda da joia roubada (em dinheiro, com cooldown; anti-abuso na seção 9).
  - **Câmeras** — ver a base à distância (UI picture-in-picture) enquanto minera.
- **Escudos**: bolha visível que bloqueia entrada de estranhos. **15 min grátis/dia** (resgatável na base), compráveis com dinheiro do jogo (30 min) e com Lumens (horas), VIP tem 2x o grátis diário. Escudo desativa a plaquinha de renda dobrada? Não — mas **joias sob escudo rendem -15%** (proteção total não pode ser a jogada dominante).
- **Proteções estruturais anti-frustração**:
  - **Novatos intocáveis**: até nível 8 (≈2h de jogo) a base tem escudo permanente automático.
  - **Servidores por faixa de patrimônio**: alocação aproximada por net worth (com prioridade para amigos/clã) — baleia não farma novato.
  - **Offline = menos exposto**: com o dono offline, apenas os **3 pedestais mais valiosos** ficam rouváveis (o resto fica cinza/trancado) e o Seguro cobre 50%. Perder tudo dormindo mata retenção; perder algo mantém a tensão.
  - **Anti-lavagem**: joia roubada fica marcada "quente" por 24h — não pode ser tradeada nem vendida a outro jogador nesse período (só exposta ou guardada). Fecha o ciclo de contas-laranja.

### 3.8 Joias: espécies, raridades e mutações (o coração da coleção)

- **Espécies** (40 no lançamento; +6–10 por temporada): quartzo, ametista, safira, rubi, esmeralda, topázio, opala, diamante, ônix… cada uma com forma/cor próprias (gerador procedural).
- **6 raridades**: Comum, Incomum, Rara, Épica, Lendária, Mítica — rolada na mineração, pesada pela camada e pela sorte (buffs/Espíritos/eventos).
- **Qualidade ★1–★5**: definida na **lapidação** (seção 3.9).
- **Mutações (até 3, roladas na mineração)**: *Luminoso* (glow), *Prismático* (arco-íris animado), *Gélido*, *Magmático*, *Estelar* (partículas), *Ecoante* (som ambiente), *Corrompido* (só durante Eclipse), *Bruto Perfeito* (garante ★5 na lapidação), **Puro (1/50.000)** — anunciado globalmente em TODOS os servidores com o nome do jogador.
- Tabela de chances **pública no índice** (transparência = confiança = menos churn por frustração).
- Combinatória: 40 espécies × 6 raridades × 5 qualidades × ~20 mutações = **dezenas de milhares de variantes colecionáveis a custo de produção ~zero**.

### 3.9 Crafting: Lapidação e Fusão

- **Lapidação** (bancada da base): transforma joia bruta em lapidada — define a qualidade ★ (RNG com pesos; leva tempo real curto, 1–15 min por tier — mais um timer de retorno). Joia lapidada rende ~2,5x mais que bruta. **Reroll de qualidade** com Poeira Estelar.
- **Fusão**: 3 joias lapidadas iguais → 1 da raridade acima (chance de herdar/ganhar mutação). Sink agressivo de excedente.
- **Reciclagem**: joias indesejadas → **Poeira Estelar** (moeda de crafting).
- **Receitas descobríveis** (combinações secretas de fusão → wiki/YouTube da comunidade — conteúdo gratuito de terceiros).
- **Forja de clã** (seção 3.17): fusões impossíveis solo.

### 3.10 Pets — "Espíritos" (sim, entram — com justificativa)

Pets são o segundo maior motor de retenção/monetização do gênero (colecionáveis + funcionais + tradeáveis). Aqui, **Espíritos** são orbes elementais flutuantes (esferas/poliedros + partículas — perfeitos para IA):

- **Função real** (não só cosmético), 3 equipados no máx.: velocidade de mineração, sorte de raridade/mutação, ímã de drops, capacidade de mochila, **Espírito-guardião** (fica na base e empurra ladrões 1x/30s — defesa enquanto você minera), desconto de lapidação.
- Obtidos em **geodos** (pedras misteriosas que caem minerando — o "unboxing" saudável: geodos são ganhos jogando; abrir na base é o segundo momento-dopamina), eventos, fusão de Espíritos e trade.
- Também têm raridades/mutações → segundo eixo de coleção.
- Inventário expansível (monetização de conveniência).

### 3.11 Progressão do jogador

- **Nível (1→∞)**: XP por minerar, lapidar, coletar renda, missões. Desbloqueia sistemas gradualmente (lapidação nv. 3, roubo nv. 5, trade nv. 10, clãs nv. 12) → FTUE limpo e anti-fraude de contas novas. **Roubo cedo (nv. 5)** — é a identidade do jogo; o jogador precisa provar a adrenalina na primeira sessão.
- **12 tiers de picareta** ↔ 10 camadas da caverna (+ novas por temporada).
- **Tier de base (1→10)**: pedestais, armazém, cofre, slots de armadilha.
- **Prestígio — "Ressonância" (infinito)**: reseta dinheiro/picaretas mantendo coleção do índice, Espíritos e cosméticos; concede **Fragmentos de Ressonância** → árvore de talentos permanente (+sorte, +renda, +velocidade). Progressão infinita e barata de manter.

### 3.12 Economia e moedas

| Moeda | Origem | Uso | Papel |
|---|---|---|---|
| **Cristalinas ($)** (soft) | Renda da galeria, venda de minério/joias, missões | Picaretas, mochilas, pedestais, armadilhas, perks, escudos básicos, lapidação | Motor do loop; inflação controlada por sinks fortes (picaretas caras, armadilhas consumíveis? não — permanentes; lapidação cobra taxa) |
| **Lumens** (hard/premium) | Robux, conquistas, eventos, passe | Geodos premium, escudos longos, poções de sorte, skips de lapidação, cosméticos | Moeda de conversão; **sempre ganhável grátis em pequena quantidade** (percepção de justiça) |
| **Poeira Estelar** (crafting) | Reciclar joias, subproduto de lapidação | Rerolls de qualidade/mutação, receitas de fusão | Sink de excedente → dá valor ao "lixo" e protege a economia |
| **Fragmentos de Ressonância** (prestígio) | Ressonância | Árvore de talentos permanente | Progressão infinita |

Sem sistema de energia: o ritmo já é limitado por mochila, respawn de nós e timers de lapidação — energia adicionaria fricção mobile e **derrubaria tempo de sessão** (que queremos alto para Premium Payouts).

**Princípios econômicos**: (1) toda moeda premium tem trilha gratuita; (2) sinks fortes em todos os horizontes (picareta → armadilha → lapidação → fusão → clã); (3) escassez transparente: contador global de existentes por variante no índice (mercado de trade saudável estilo Adopt Me).

### 3.13 Missões

- **Tutoriais encadeados** (FTUE): 15 missões que em ~20 min fazem o jogador minerar, lapidar, expor, coletar, ser apresentado ao roubo (rouba de uma "base fantasma" de treino — NPC estrutural, sem humanoide) e instalar a primeira armadilha.
- **Contratos do Golem** (NPC de pedra na praça): pedidos rotativos ("entregue 3 safiras ★3+ lapidadas") com recompensas escaladas — dá *propósito* à mineração além do lucro.
- **Arcos semanais** leves de história (o Golem conta a origem das camadas — lore barata que YouTubers adoram teorizar).

### 3.14 Sistema diário e semanal

**Diário:**
- Recompensa de login progressiva (dia 1→7; dia 7 = geodo raro).
- **Streak de mineração**: quebrar 1 veio/dia mantém streak → +2%/dia de sorte (cap +30%). **Proteção**: 1 falha perdoada a cada 7 dias.
- 3 missões diárias (5–10 min).
- **Modificador do dia** na caverna ("Dia do Rubi: +25% de chance de rubi") → razão temática de logar HOJE.
- Escudo grátis diário de 15 min (resgatar na base).

**Semanal:**
- **Contrato Semanal Grande** (3–4 sessões; recompensa: geodo Lendário).
- Meta de clã semanal (seção 3.17).
- **Loja do Viajante**: mercador com estoque semanal rotativo (Espíritos/decoração fora de temporada) — FOMO leve e recorrente.
- Torneio semanal de leaderboard (seção 3.18).

### 3.15 Eventos e temporadas

- **Eventos-surpresa de servidor**: os eventos de caverna (3.5) + **"Corrida do Ouro"** nas bases (por 10 min, renda 2x e roubos sem cooldown — caos deliberado e clipável, 1x/dia no horário de pico).
- **Eventos de calendário** (Halloween, Natal, verão…): espécie exclusiva + camada temática temporária + cosméticos limitados.
- **Temporadas (8 semanas)**: nova camada/bioma (paleta + materiais novos — barato), 6–10 espécies novas, passe free+premium (seção 4), leaderboard sazonal com troféus permanentes datados. **Espécies de temporadas passadas nunca mais são mineráveis** → valor de colecionador crescente e economia de trade viva (o motor do Adopt Me).

### 3.16 Recompensas, conquistas e índice

- **Conquistas (200+ no lançamento, geradas por template)**: marcos de mineração/lapidação/roubo/defesa/coleção/social; dão Lumens (trilha grátis da moeda premium) e **títulos sobre o avatar** ("Ladrão Lendário", "Barão do Diamante") — status social = desejo.
- **Índice de Joias ("Cristalopédia")**: registro permanente de cada variante já obtida, com % global de jogadores que a possuem → colecionismo infinito e comparável. Marcos de índice (10/50/100/500 variantes) → recompensas crescentes, incluindo Espíritos exclusivos intradeáveis (prova de dedicação).
- **Mural da Fama** na praça: os 3 roubos mais valiosos do servidor nas últimas 24h (nomes de ladrão e vítima) — drama social permanente.

### 3.17 Social, grupos e clãs

- **Visita livre** a qualquer base (é assim que o roubo existe) + botão de "estrelinha" em galerias → ranking de decoração.
- **Presentes diários** entre amigos (1 geodo comum/dia) → razão para adicionar amigos.
- **Clãs (20 membros)**: nome/bandeira/cor; **Galeria do Clã** na praça (vitrine coletiva que rende para o cofre do clã); **Forja do Clã** (fusões que exigem contribuição de vários membros); metas semanais coletivas; **aliança de defesa** (membros do clã recebem o alarme das bases uns dos outros e podem defender — brigada anti-roubo); guerra *econômica* de clãs (qual clã produz mais valor/semana — sem combate).
- **Grupo Roblox oficial**: +5% renda por entrar → base de notificação e marketing own-channel.
- **Trade seguro** (nv. 10+): UI dedicada, confirmação dupla, log server-side, cooling-off de 5s pós-alteração (anti-scam padrão-ouro).

### 3.18 Matchmaking e servidores

Sem matchmaking competitivo. Servidores de 10–12 jogadores com **alocação inteligente**: amigos > clã > idioma/região > **faixa de patrimônio** (net worth). A última regra é a espinha dorsal da justiça do roubo: você rouba e é roubado por gente do seu tamanho.

### 3.19 Ranking

- **Leaderboards globais e semanais**: valor de galeria, renda/h, índice completado, roubos bem-sucedidos, defesas (empurrões em ladrões), fusões.
- **Ranking sazonal** com troféus de base permanentes datados (status histórico).
- **Ranking de clãs** com destaque na praça.

### 3.20 PvP ou PvE? — **PvE econômico com PvP de roubo (justificado)**

Combate com dano/HP está descartado: balanceamento caro, toxicidade com público jovem, e animação de combate é ponto fraco de IA. O PvP é **assimétrico e econômico** — roubo pegar-e-correr com empurrão cômico (decisão do product owner, validada pelo recordista do gênero). A caverna é 100% PvE cooperativo-competitivo (disputa por nós raros, sem agressão direta). Quem quer paz joga com escudos/armazém e perde pouco; quem quer adrenalina vive na rua. O mapa único garante que os dois se encontrem — é aí que nascem as histórias.

### 3.21 Conteúdo de longo prazo

1. Temporadas de 8 semanas com **camadas novas para sempre** (a caverna é verticalmente infinita — motor principal, ~80% recombinação procedural).
2. Ressonância infinita + árvore de talentos profunda.
3. Índice praticamente incompletável (espécies novas a cada temporada + aposentadas valorizando).
4. Economia de trade com escassez real → metajogo de "investidor".
5. Sistemas novos por trimestre (roadmap, seção 8): guerra de clãs, museus públicos, modo heist cooperativo (assalto a "cofre do servidor" PvE em grupo — reaproveita 100% das mecânicas existentes).

---

## 4. ESTRATÉGIA DE MONETIZAÇÃO

> Filosofia: **"pay for convenience, never for power exclusivo"**. Tudo que um pagante consegue, um free player consegue com tempo (exceto cosméticos). Defesa NUNCA é exclusiva de pagante — um jogo de roubo onde só quem paga se protege é percebido como extorsão e morre. Jogos percebidos como justos monetizam MAIS no longo prazo.

### 4.1 Gamepasses (compra única — os "best value" percebidos)

| Gamepass | Preço (Robux) | Efeito | Racional |
|---|---|---|---|
| **VIP** | 399 | +10% renda, 2x escudo grátis diário, +50% teto offline, tag dourada | Âncora clássica; melhor custo-benefício percebido |
| **Mochila Grande** | 349 | 2x capacidade de mochila | A conveniência nº 1 do loop de mineração |
| **Auto-Coleta** | 299 | Coleta a renda da plaquinha automaticamente a cada 10 min | O gamepass nº 1 de renda passiva (com delay — não elimina o retorno à base) |
| **Pedestais de Elite** | 499 | +6 slots de pedestal | Mais renda E mais exposição — se auto-balanceia |
| **Lapidação Dupla** | 299 | 2 lapidações simultâneas | Conveniência de mid/late game |
| **Teleporte de Camada** | 249 | Teleporte direto a camadas já destravadas | Remove deslocamento repetido, não dá poder |

Regra pós-mai/2026: passes vendem apenas dentro do próprio jogo (venda cross-game foi desativada pela plataforma) → toda a vitrine é interna, acessível em 1 toque.

### 4.2 Developer Products (consumíveis — o motor de receita recorrente)

- **Pacotes de Lumens**: 99 / 449 / 799 / 1.699 Robux (curva com bônus crescente; o 2º pacote é o "sweet spot" destacado).
- **Geodos premium**: compráveis com Lumens — NUNCA diretamente com Robux (camada de abstração reduz percepção de gacha e risco de política; chances publicadas).
- **Escudos**: 1h / 8h / 24h.
- **Poções de sorte** (15–60 min; também ganháveis grátis em diárias/eventos).
- **Skip de lapidação** (proporcional ao tempo restante).
- **Reroll premium de qualidade/mutação**.
- **Ressonância instantânea** (para veteranos apressados).

### 4.3 Assinatura (ferramenta nova da plataforma — vantagem de pioneiro)

**"Pacto Lunar" — mensal (~R$ 9,90 equivalente em Robux):**
- 150 Lumens/mês + 1 geodo raro/semana + escudo diário automático de 1h + slot de lapidação exclusivo + aura cosmética de assinante.
- Vale ~2x o preço em itens → conversão alta; receita previsível; a plataforma promove ativamente jogos que adotam assinaturas.

### 4.4 Cosméticos

- **Skins de base/galeria** (temas completos: mármore, neon-cyberpunk, templo antigo — paleta/material, produção barata).
- **Skins de picareta** e efeitos de golpe (o item mais visto do jogo — está na mão do jogador o tempo todo).
- Auras/trilhas para avatar e Espíritos; efeitos de coleta na plaquinha (chuva de confete — clipável = marketing pago pelo jogador).
- Molduras de pedestal, pisos animados, estátuas.

### 4.5 Itens limitados

- **1 cosmético limitado por temporada** (contador global visível de unidades).
- Espécies sazonais aposentadas para sempre → valorização em trade (FOMO saudável: o item continua existindo no trade, só não é mais *minerável*).

### 4.6 Eventos pagos

Nunca conteúdo bloqueado por pagamento. Eventos são grátis; a monetização do evento é **aceleração e cosmético** (ex.: no Halloween, todos jogam; o pacote pago dá 2x tokens do evento + skin exclusiva).

### 4.7 Boosts e ofertas temporárias

- Boosts de 15 min–24h (sorte, renda, velocidade de mineração) — compráveis com Lumens E ganháveis grátis.
- **Boost de servidor**: um jogador compra, TODOS ganham +sorte 15 min (o comprador vira herói público → status como motor de compra).
- Ofertas relâmpago (4–24h) segmentadas por comportamento.

### 4.8 Bundles e ofertas segmentadas (funil de conversão)

| Segmento | Oferta | Objetivo |
|---|---|---|
| **Novo jogador (D0–D3)** | "Kit do Minerador": 100 Lumens + picareta tier 3 + escudo 24h por preço simbólico (~49 Robux) | **Primeira compra é o evento mais importante do funil** — quem compra 1x tem LTV ~10x maior; o kit é deliberadamente o melhor negócio do jogo |
| **Engajado free (D7+, nível 15+, 0 compras)** | Oferta única do Kit + trial de 3 dias de Pacto Lunar | Converter o "quase-pagante" |
| **Pagante recorrente** | Bundles de temporada, limitados, pacotes maiores com bônus | Elevar ARPPU sem tocar no free |
| **Baleia (top 1% gasto)** | Cosméticos de ultra-prestígio, limitados numerados, skin de galeria "cofre de banco suíço" | Teto de gasto alto via status, não poder |
| **Churn risk (7+ dias ausente)** | Notificação + "presente de retorno" grátis + escudo 24h automático ao logar + oferta de recuperação | Reativação sem medo ("minha base foi saqueada?" → não: proteção offline, seção 3.7) |

**Funil**: Free → primeira compra (Kit) → consumíveis ocasionais (Lumens) → assinatura (recorrente) → passe sazonal → colecionador de limitados. Cada degrau tem uma oferta desenhada para o próximo.

### 4.9 Premium Payouts e o boost 18+

- Tempo de sessão de assinantes Roblox Premium gera payout passivo → tudo que aumenta duração de sessão (mineração ativa, defesa da base, eventos de caverna) também aumenta essa receita. O loop ativo de mineração é estruturalmente superior ao plantio passivo nessa métrica.
- Jogo construído em **R15** e com estética heist não-infantilizada para capturar o **DevEx +42% de gasto 18+ verificado (EUA)** — decisão de arquitetura do dia 1, sem custo extra.

---

## 5. PLANO DE RETENÇÃO

### 5.1 Psicologia aplicada (mapa mecanismo → sistema)

| Princípio psicológico | Implementação no jogo |
|---|---|
| **Recompensa variável (Skinner)** | Toda quebra de nó rola joia/raridade/mutação; geodos; lapidação com ★ RNG. A "caixa de loot" central do jogo é GRÁTIS e infinita — a dopamina não está atrás de paywall |
| **Efeito Zeigarnik (tarefa incompleta)** | Renda acumulando até o teto; lapidações em andamento; contrato a 80%; camada seguinte a 2 upgrades de distância |
| **Aversão à perda (saudável)** | Joias expostas são roubáveis → "volto para vigiar/coletar" (mas proteção offline + seguro — a perda nunca é devastadora) |
| **Reciprocidade social** | Presentes diários; defender a base do amigo de clã via alarme compartilhado |
| **Compromisso e consistência** | Streaks com perdão; metas de clã (não quero decepcionar o grupo) |
| **Status e comparação** | Títulos, Mural da Fama, troféus sazonais datados, ranking de decoração, % global no índice |
| **Curiosidade** | Receitas de fusão secretas; camadas não visitadas; Terremoto mostra a camada seguinte por 3 min |
| **Narrativa pessoal** | Cada joia tem história ("essa eu minerei no Eclipse", "essa eu roubei do top 1") — apego = retenção |

### 5.2 Metas por horizonte

- **Curto (hoje)**: coletar renda antes do teto, diárias, streak, modificador do dia, escudo grátis.
- **Médio (semana)**: contrato semanal, meta de clã, torneio, Loja do Viajante, níveis do passe, próxima picareta/camada.
- **Longo (temporada/meses)**: completar índice da temporada, ranking sazonal, Ressonâncias, coleção de limitados, galeria dos sonhos, camada 10.

### 5.3 Mecânicas específicas de retorno

1. **Relatório de retorno**: ao logar — "Enquanto você esteve fora: sua galeria rendeu $12.400 (teto atingido há 3h — expanda o Cofre!), 2 tentativas de roubo bloqueadas pelo escudo, 1 lapidação pronta: Safira ★4!" — três ganchos em uma tela.
2. **Teto de renda offline** = retorno 2–4x/dia por design (e o upgrade do Cofre é comprado com renda — loop que se auto-alimenta).
3. **Timers de lapidação escalonados** (1 min a horas) → sempre algo pronto AGORA e algo pronto AMANHÃ.
4. **Eventos de caverna** em horários semi-aleatórios → checagens espontâneas ("será que tem meteoro agora?").
5. **Notificações Roblox** (opt-in, máx. 1/dia): lapidação Mítica pronta, escudo expirando, presente de amigo, Corrida do Ouro começando.
6. **FOMO saudável**: tudo que expira é cosmético/emissão (nunca poder); rotações voltam em ciclos anunciados; streak tem perdão. FOMO cruel gera burnout e churn em 60 dias — nosso alvo é D180.
7. **Progressão infinita** via camadas sazonais + Ressonância + índice + trade (não existe "zerei o jogo").

### 5.4 Alvos de métricas

| Métrica | Alvo | Benchmark de decisão |
|---|---|---|
| D1 | ≥ 35% | <25% no soft launch = reformular FTUE antes de escalar |
| D7 | ≥ 18% | Gênero premia 15%+ |
| D30 | ≥ 8% | Simuladores top mantêm D30 "anormalmente flat" — nosso design copia essa estrutura |
| Sessão média | ≥ 25 min | Mineração ativa + defesa + eventos puxam isso acima do gênero "grow" |
| Sessões/dia | ≥ 2,5 | Teto offline + lapidação + escudo diário são os drivers |

---

## 6. PLANO DE CRESCIMENTO

### 6.1 Motor orgânico (algoritmo da home page)

O algoritmo do Roblox promove por: **D1/D7, tempo de sessão, taxa de conversão de impressão→play (ícone/título) e monetização por usuário**. Estratégia:

1. **Soft launch silencioso** (2–3 semanas): iterar FTUE até D1 ≥ 30% com tráfego pequeno. NÃO gastar tráfego/marketing com retenção ruim — é queimar a única primeira impressão do algoritmo.
2. **A/B contínuo de ícone e título** (ferramenta nativa do Roblox): joia gigante brilhante + mão roubando + rosto de reação. CTR do ícone é alavanca tão importante quanto o jogo.
3. **Updates semanais SEMPRE no mesmo dia** (ex.: sexta 17h): ritual comunitário; o algoritmo premia o pico recorrente.
4. **Compatibilidade total mobile + performance em celular fraco** (geometria primitiva ajuda!): a maioria dos jogadores está em telefones medianos.

### 6.2 Convites e viralidade embutida

- **Sistema de indicação**: convidado e convidante ganham (geodo Épico para ambos quando o convidado atinge nível 10 — meta de nível evita fraude).
- **Presentes diários entre amigos** → razão mecânica para importar a lista de amigos.
- **Clãs recrutam sozinhos**: metas coletivas + brigada de defesa fazem membros chamarem amigos de fora ("preciso de gente para vigiar a galeria").
- **Boost de servidor público**: comprador vira herói → screenshot → share.

### 6.3 Máquina de conteúdo para criadores (TikTok/YouTube)

Momentos clipáveis **por design**:
1. **O roubo perfeito e a perseguição** (feixe de luz no ladrão = a câmera do espectador já sabe onde olhar) — narrativa pronta de 60 segundos.
2. Drop de mutação **Pura** (efeito explosivo + anúncio global com nome do jogador — o jogador filma a si mesmo ficando famoso).
3. **Corrida do Ouro** e eventos de caverna (caos coletivo).
4. Trade de espécie aposentada valiosa ("paguei X pela safira da Temporada 1").
5. Tours de galeria decorada (conteúdo calmo/ASMR para outra audiência).
6. **Vingança com Rastreador** (setup → payoff perfeito para vídeo).

Suporte ativo:
- **Programa de creator codes**: criador tem código; quem usa dá % de Lumens ao criador → exército de vendedores comissionados.
- **Kit de mídia** público + Discord com canal de criadores e acesso antecipado a updates.
- **Modo cinematográfico in-game** (esconder UI, câmera livre) — custo trivial, adorado por YouTubers.
- Semear 10–20 micro-influencers de Roblox (10k–100k inscritos) no lançamento em vez de 1 grande — mais horas totais de vídeo por custo.

### 6.4 Canais próprios

- Grupo Roblox (bônus por entrar) → anúncios de update para todos os membros.
- Discord da comunidade (eventos, sneak peeks, votações de espécies novas — cocriação gera lealdade).
- TikTok oficial com os melhores roubos e drops "Puros" da semana (conteúdo dos próprios jogadores, re-postado).

---

## 7. ANÁLISE DE CONCORRÊNCIA

| Concorrente | Pontos fortes | Pontos fracos | Oportunidade que deixa aberta | Como superamos |
|---|---|---|---|---|
| **Steal a Brainrot** (25,8M CCU recorde) — **concorrente direto de mecânica** | Tensão social geradora de clipes; fórmula "Steal a" com CTR máximo; simplicidade brutal | Itens vêm de compra passiva (esteira RNG) — zero apego/mérito; frustração de perder sem proteções; IP de memes de terceiros (risco legal + meia-vida de trend); economia rasa (sem trade profundo, crafting, clãs) | Roubo *justo* sobre itens *conquistados*, com metajogo de verdade | Loop ativo de mineração (mérito + apego), lapidação/fusão, trade com escassez, clãs com defesa cooperativa, IP próprio atemporal (joias/heist) |
| **Grow a Garden** (21M CCU pico) | Loop offline perfeito; mobile; simplicidade | Zero tensão social; profundidade rasa; dependente de novidade | Jogador que ama progresso passivo mas quer *emoção* | Nosso teto de renda offline dá o gancho passivo; o roubo dá a emoção que lá não existe |
| **Grow Crystals!** (dez/2024, 50M+ visitas) — **concorrente de tema** | Ocupou primeiro o nicho "cristais"; SEO de códigos estabelecido | Clone raso de Grow a Garden: sem roubo, sem trade, sem fusão, sem clãs, sem temporadas; porte médio | Todo o metajogo social e de economia está vago no nicho | Não competimos pelo nome ("Steal a", não "Grow a"); ele valida a demanda pelo tema e nos cede o jogador que quer mais que plantar-e-colher |
| **Pet Simulator 99 / BIG Games** | Execução impecável; economia de trade madura; máquina de updates | Complexidade acumulada intimida novatos; percepção de gacha pesado; exige equipe gigante | Entrada simples com teto profundo | FTUE de 60 segundos; gacha só periférico (geodos ganháveis); cadência procedural barateia nossos updates |
| **Adopt Me** | Economia de trade lendária; escassez que valoriza | Envelhecido; loop principal fraco (o trade É o jogo) | Trade forte APOIADO num loop forte | Trade + escassez sazonal sobre um loop de mineração/roubo vivo |
| **Blox Fruits** | Profundidade de meses; sessões longas; base fiel 13–17 | Exige combate/animação complexos (impossível para IA); onboarding hostil | — (arquétipo diferente) | Capturamos o mesmo 13–17 com sessões longas via economia e adrenalina social, não combate |

**Síntese**: nenhum líder combina (a) loop ativo de aquisição com mérito, (b) renda passiva com teto offline, (c) roubo justo, (d) coleção/crafting profundos, (e) trade com escassez e (f) clãs cooperativos. O recordista do gênero (Steal a Brainrot) é vulnerável exatamente onde somos fortes: apego ao item, justiça percebida e profundidade de economia — com custo de produção estruturalmente menor (procedural + IA).

---

## 8. ROADMAP

### MVP (semanas 1–6) — "a tensão minerar-vs-vigiar tem que funcionar sozinha"
- Mapa: distrito com 10–12 bases + praça + caverna com **3 camadas**; teleporte por toque na entrada.
- Mineração: nós com HP, 3 tiers de picareta, mochila, 15 espécies × 4 raridades × 6 mutações.
- Base: 4–8 pedestais, renda/s, plaquinha de coleta, armazém, **teto offline (2h)**.
- **Roubo pegar-e-correr completo** (canalização, feixe, empurrão, cooldowns) + escudo grátis diário + proteção de novato + proteção offline.
- FTUE (15 missões); diárias + streak; modificador do dia.
- DataStore robusto (sessão-lock, backup versionado — perda de save mata jogos deste gênero).
- UI mobile-first completa. **Sem trade/clãs/lapidação ainda.**
- *Meta interna: D1 ≥ 25% e "primeiro roubo sofrido → jogador continua jogando" ≥ 70% (métrica custom de frustração).*

### Alpha (semanas 7–10) — profundidade e defesa
- Lapidação + Poeira Estelar + fusão; geodos + Espíritos (8 tipos, incl. guardião); Cristalopédia; conquistas v1.
- Camadas 4–6; armadilhas (4 tipos) + perks (Alarme, Rastreador, Seguro, Câmeras).
- Eventos de caverna (Veio Dourado, Meteoros, Terremoto); Lumens + primeiras ofertas (Kit do Minerador, 3 gamepasses core).
- *Soft launch silencioso, 1–2k jogadores; iterar FTUE até D1 ≥ 30%; calibrar todos os diais do roubo via config remota.*

### Beta (semanas 11–16) — social e economia
- **Trade seguro** (confirmação dupla, log, regra "quente" anti-lavagem); presentes entre amigos; sistema de indicação.
- Clãs v1 (galeria coletiva, meta semanal, alarme compartilhado/brigada); leaderboards + Mural da Fama; Ressonância v1.
- Servidores por faixa de patrimônio; assinatura Pacto Lunar; infra de passe de temporada.
- Camadas 7–8; Eclipse + Corrompido; Corrida do Ouro.
- *Meta: D7 ≥ 15%, sessão ≥ 20 min, primeiras compras validando funil.*

### Lançamento (semanas 17–18)
- Temporada 1 completa (camada 9 temática + passe + limitado + espécies sazonais).
- Campanha: 10–20 micro-influencers + creator codes + Discord aberto + A/B de ícone rodando.
- Updates semanais travados no calendário a partir daqui. **Sempre.**

### Meses 1–3 pós-lançamento
- Temporada 2 (camada 10); guerra econômica de clãs; ranking de decoração; torneios semanais.
- Loja do Viajante; ofertas segmentadas por comportamento (funil completo da seção 4.8).
- Balanceamento econômico guiado por dados (sinks/sources); ferramentas anti-exploit/anti-dupe (crítico para trade).
- Localização: PT-BR, ES, ID, TH, FIL (mercados mobile gigantes; tradução é tarefa perfeita para IA).

### Meses 4–6
- **Modo Heist cooperativo** (assalto PvE em grupo ao "Cofre do Golem" — reusa 100% das mecânicas); árvore de talentos plena; forja de clã.
- Evento de plataforma (participar de eventos oficiais Roblox — tráfego grátis).
- Programa formal de creators; histórico de preços no trade (transparência = confiança).
- *Meta: estabilizar 15–30k CCU médio.*

### Ano 1
- 4–5 temporadas concluídas (caverna na camada ~14); espécie nº 100+; museus públicos de coleção.
- Guerra de clãs v2 com territórios na caverna (zonas de bônus disputadas por produção, não combate).
- Explorar Transfers API para economia inter-jogadores dentro das regras da plataforma.
- Avaliar spin-off da marca SOMENTE se CCU estável > 50k — antes disso, todo recurso no jogo principal.

---

## 9. AVALIAÇÃO HONESTA (0–10)

| Critério | Nota | Justificativa fria |
|---|---|---|
| **Potencial de lucro** | 8,5 | Gênero comprovadamente nº 1 em receita; funil completo (passes+consumíveis+assinatura+temporadas); teto real depende da execução da economia de trade |
| **Potencial de viralização** | 8 | A fórmula "Steal a" é a mais clipável da história da plataforma, e nossa versão adiciona mérito/apego (histórias melhores). Viral nunca é garantido — o plano NÃO depende dele |
| **Facilidade de desenvolvimento** | 8 | Desenhado para IA (primitivas + código), mas o pegar-e-correr no dia 1 antecipa trabalho de rede/anti-cheat (validação server-side de posse, velocidade, teleporte) que no design anterior ficava para depois |
| **Escalabilidade** | 9 | Conteúdo procedural (espécies/mutações/camadas = recombinação); caverna verticalmente infinita; custo marginal de update baixíssimo |
| **Retenção** | 9 | Loop ativo (sessão longa) + teto offline (retorno múltiplo diário) + roubo (emoção) + coleção/trade (meses) — cobre todos os horizontes |
| **Monetização** | 8,5 | "Pay for convenience" com funil segmentado + assinatura pioneira; perde 1,5 por recusar deliberadamente gacha hard — troca consciente de teto por longevidade |
| **Longevidade** | 8 | Temporadas + escassez + trade + prestígio + camadas infinitas; risco: fadiga da meta "Steal a X" (mitigada por profundidade que os clones não têm) |

**Riscos honestos que podem matar o projeto** (e mitigação):
1. **FTUE ruim** → soft launch obrigatório com gate de D1 ≥ 30% antes de qualquer marketing.
2. **Roubo frustrar novatos além do tolerável** → métrica custom no MVP ("continua jogando após 1º roubo sofrido" ≥ 70%); todos os diais (canalização, cooldown, seguro, proteção offline) em config remota para ajuste sem deploy.
3. **Exploits no roubo/trade** (dupe, lavagem por contas-laranja, auto-roubo para farmar Seguro) → toda posse validada server-side; regra "quente" 24h; Seguro paga em Cristalinas com cooldown e só para roubos de jogadores fora do próprio clã/amigos; logs completos.
4. **Perda de saves** → sessão-lock + backups versionados antes do soft launch (inegociável).
5. **Baleia farmando novato** → servidores por faixa de patrimônio + proteção de novato + proteção offline.
6. **Saturação da meta "Steal a X"** → nossa vantagem não é a ideia, é o custo estrutural: updates semanais procedurais que clones manuais não sustentam + profundidade (lapidação/fusão/trade/clãs) que nenhum clone tem.

---

## 10. RESUMO EXECUTIVO

Construir **"Steal a Crystal"**: mineração ativa numa caverna compartilhada de camadas infinitas, com joias RNG (espécie/raridade/mutação) expostas em galerias pessoais que geram renda coletada na plaquinha (com teto offline), sob a tensão permanente do roubo pegar-e-correr — defendido por empurrões, armadilhas, alarmes e escudos, com proteções estruturais de justiça (novatos, offline, faixa de patrimônio). Lapidação, fusão, trade com escassez sazonal, clãs com defesa cooperativa e temporadas de 8 semanas completam o metajogo. Mobile-first, R15, estética heist/neon feita de primitivas + materiais + partículas (100% construível por IA), monetizado por conveniência (gamepasses + Lumens + assinatura Pacto Lunar + passes sazonais) com funil segmentado. A tese: **pegar a fórmula social do maior recorde de CCU da história, corrigir sua fraqueza central (itens sem mérito, roubo sem justiça) com um loop de aquisição ativo e uma economia profunda, a um custo de produção que só produção procedural via IA permite.**

---

## Registro de revisões

- **v1 (jul/2026)**: conceito original "Grow a Crystal" — cultivo de sementes de cristal com crescimento offline.
- **v2 (jul/2026)**: pivô por direção do product owner — núcleo passa a ser mineração ativa (caverna compartilhada em camadas) + galeria de pedestais com renda por segundo e plaquinha de coleta + roubo pegar-e-correr; título de trabalho **"Steal a Crystal"**. Decisões travadas: roubo direto estilo Steal a Brainrot, caverna compartilhada com camadas, renda offline com teto, defesa por empurrão/armadilhas/perks (alarme, rastreador, seguro, câmeras).
