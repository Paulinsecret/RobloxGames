# 🎮 Game Design Document (GDD) & Especificação Técnica

> **Instruções de Preenchimento:**  
> Este documento é o mapa do nosso jogo. Preencha as seções abaixo (com o seu parceiro) com o máximo de detalhes possível.  
> Você pode marcar as caixas `[x]`, preencher os campos `[Insira aqui...]` e colar links ou imagens de referência.  
> A IA (Antigravity) utilizará estas respostas para construir a arquitetura de código, scripts do servidor, scripts do cliente e sistemas no Rojo.

---

## 1. Identidade & Visão Geral do Jogo

* **Nome Provisório / Oficial do Jogo:** `[Insira o nome aqui]`
* **Slogan / Descrição em 1 Frase:** `[Ex: Um RPG de sobrevivência medieval onde cada erro custa caro]`
* **Público-Alvo Principal:**
  - [ ] Crianças / Família (Casual, estilo Pet Simulator / Brookhaven)
  - [ ] Jovens / Hardcore (Competitivo, estilo Deepwoken / Bedwars)
  - [ ] Misto / Amplo (Acessível mas com profundidade)
* **Plataformas de Foco:**
  - [ ] PC (Teclado + Mouse)
  - [ ] Mobile (Touchscreen / Celular e Tablet)
  - [ ] Console (Controle / Xbox / PlayStation)
* **Tipo de Câmera:**
  - [ ] 3ª Pessoa Livre (Padrão Roblox)
  - [ ] 3ª Pessoa Travada / Shift Lock (Estilo Action RPG / Soulslike)
  - [ ] 1ª Pessoa Imersiva (Estilo Horror / FPS)
  - [ ] Câmera Customizada / Top-Down (Vista isométrica de cima)
* **Formato do Avatar:**
  - [ ] R15 (Mais flexível para animações detalhadas)
  - [ ] R6 (Clássico, hitboxes mais previsíveis, combate retrô)
  - [ ] Rthro / Customizado

---

## 2. Referências, Inspirações & Imagens

* **Jogos de Referência no Roblox (Cite 1 a 3 e o que copiar/melhorar de cada um):**
  1. *Jogo 1:* `[Nome do Jogo]` &rarr; *O que aproveitar dele:* `[Ex: A física de movimentação e fluidez]`
  2. *Jogo 2:* `[Nome do Jogo]` &rarr; *O que aproveitar dele:* `[Ex: O sistema de interface e inventário]`
  3. *Jogo 3:* `[Nome do Jogo]` &rarr; *O que aproveitar dele:* `[Ex: A progressão de quests e mapa]`
* **Jogos de Referência Fora do Roblox (Steam/Consoles):**
  * `[Ex: Dark Souls, Terraria, Minecraft, Dead by Daylight, etc.]`
* **Links de Vídeos / Inspiração (YouTube / TikTok):**
  * `[Cole links de referências aqui]`
* **Imagens & Concept Arts:**
  > Coloque as imagens na pasta `assets/references/` do repositório ou cole URLs aqui:
  * `[Ex: assets/references/mapa_layout.png]`
  * `[Ex: assets/references/estilo_combate.gif]`

---

## 3. Loop Central de Gameplay (Core Game Loop)

Descreva em etapas sequenciais o que o jogador faz durante o jogo:
```
[Passo 1: Spawn/Entrada] -> [Passo 2: Exploração/Ação] -> [Passo 3: Desafio/Combate/Coleta] -> [Passo 4: Recompensa/Upgrade] -> [Loop Reinicia com nível/recursos maiores]
```

* **No Primeiro Minuto (Primeira Impressão):**  
  `[O que acontece assim que o jogador entra no servidor? Tutorial? Spawn direto? Cutscene?]`
* **Após 10 Minutos de Jogo:**  
  `[Qual é a meta imediata? Conseguir a primeira arma? Subir o primeiro nível? Passar a primeira sala?]`
* **Após 10 Horas de Jogo (Endgame):**  
  `[O que mantém o jogador jogando a longo prazo? Bosses difíceis? Conquistas raras? Colecionáveis? PvP?]`

---

## 4. Mapa, Ambientação & Estilo Artístico (3D)

* **Estilo Artístico dos Modelos:**
  - [ ] Low-Poly / Cartunesco vibrante (Estilos Flat Shading, cores vivas)
  - [ ] Stylized Medieval / Fantasia
  - [ ] Sci-Fi / Futurista / Cyberpunk
  - [ ] Sombrio / Realista / Horror
  - [ ] Misto / Outro: `[Descreva]`
* **Estrutura do Mapa:**
  - [ ] Mundo Aberto Contínuo (Ilhas, continentes sem telas de carregamento)
  - [ ] Salas / Fases Instanciadas (Estilo portas, masmorras com teleporte)
  - [ ] Arena Fechada (Mapa único focado em combate rápido)
  - [ ] Mapa Gerado Proceduralmente (Salas que surgem aleatoriamente)
* **Clima e Iluminação:**
  - [ ] Ciclo de Dia e Noite Dinâmico (Relógio com influência no gameplay)
  - [ ] Iluminação Fixa Atmosférica (Ex: Noite perpétua com neblina densa)
  - [ ] Efeitos Climáticos (Chuva, tempestade, tempestade de areia, neve)
* **Zonas e Áreas Principais (POIs):**
  1. *Área 1:* `[Nome da Área]` &rarr; *Propósito:* `[Ex: Spawn Seguro, NPCs de compra e banco]`
  2. *Área 2:* `[Nome da Área]` &rarr; *Propósito:* `[Ex: Floresta de monstros iniciais]`
  3. *Área 3:* `[Nome da Área]` &rarr; *Propósito:* `[Ex: Masmorra do Boss final]`

---

## 5. Mecânicas do Jogador (Player Controller & Movimentação)

Quais habilidades de movimentação o jogador terá?
* [ ] **Sprint / Corrida:**
  - Possui barra de Stamina / Energia? `[Sim / Não]`
  - Velocidade normal: `[Ex: 16]` / Velocidade no Sprint: `[Ex: 26]`
* [ ] **Dash / Esquiva:**
  - Tem tempo de recarga (Cooldown)? `[Ex: 1.5s]`
  - Dá invulnerabilidade temporária (I-Frames)? `[Sim / Não]`
* [ ] **Pulo Duplo (Double Jump):**
  - Habilidade nativa ou desbloqueável? `[Descreva]`
* [ ] **Escalada / Mantle (Subir em bordas):**
  - O jogador escala paredes ou se apoia em quinas altas? `[Descreva]`
* [ ] **Slide / Agachamento:**
  - Deslizar ladeira abaixo ou agachar para furtividade? `[Descreva]`
* [ ] **Natação / Voo / Outra física customizada:**
  - `[Descreva se houver]`

---

## 6. Combate, Armas & Interações

* **O jogo possui combate?** `[Sim / Não]`
* **Estilo de Combate:**
  - [ ] Corpo a Corpo (Melee / Espadas, socos, combos M1/M2)
  - [ ] À Distância (Ranged / Arcos, magias, armas de fogo com raycast)
  - [ ] Habilidades com Teclas (Q, E, R, F para magias e skills especiais)
  - [ ] Focado em Quebra-cabeças / Interação com Objetos (Sem combate físico)
* **Mecânicas de Defesa:**
  - [ ] Bloqueio com Escudo / Arma (Redução de dano percentual)
  - [ ] Sistema de Parry (Bloqueio perfeito no frame certo que atordoa o inimigo)
  - [ ] Barra de Postura / Estabilidade
* **Efeitos de Status:**
  - [ ] Atordoamento (Stun)
  - [ ] Queimadura / Sangramento / Veneno (Dano contínuo - DoT)
  - [ ] Lentidão (Slow)
  - [ ] Repulsão (Knockback físico)
* **Interações com o Cenário (ProximityPrompt):**
  - `[Ex: Abrir portas trancadas com chave, coletar ervas/minérios, falar com NPCs]`

---

## 7. Economia, Progressão & Banco de Dados (DataStore)

* **Moedas do Jogo:**
  1. *Moeda 1 (Principal):* `[Ex: Moedas de Ouro - obtidas jogando]`
  2. *Moeda 2 (Secundária/Premium):* `[Ex: Gemas / Diamantes - raras ou compradas]`
* **Progressão do Personagem:**
  - [ ] Níveis & Pontos de Atributo (Ex: Pontos em Vida, Dano, Velocidade, Defesa)
  - [ ] Árvore de Habilidades (Skill Tree com desbloqueio progressivo)
  - [ ] Títulos / Ranks / Conquistas
* **Dados que precisam ser Salvos (DataStore Server-Side):**
  - [x] Moedas / Economia
  - [x] Inventário e Itens equipados
  - [ ] Nível e XP
  - [ ] Checkpoints / Localização no mapa
  - [ ] Estatísticas (Eliminações, Mortes, Vitórias, Tempo jogado)
  - [ ] Configurações do jogador (Volume, sombras, controles)
* **Leaderstats (Tabela TAB visível no jogo):**
  - Quais valores devem aparecer ao lado do nome do jogador? `[Ex: Moedas, Nível, Vitórias]`

---

## 8. Inventário & Sistema de Itens

* **Formato do Inventário:**
  - [ ] Hotbar Padrão do Roblox (Teclas 1 a 9 no topo/rodapé)
  - [ ] Mochila Customizada com Grid (Slots limitados, estilo RPG)
  - [ ] Limite por Peso ou Quantidade máxima
* **Raridade dos Itens:**
  - [ ] Comum (Cinza/Branco)
  - [ ] Incomum (Verde)
  - [ ] Raro (Azul)
  - [ ] Épico (Roxo)
  - [ ] Lendário (Dourado/Laranja)
  - [ ] Mítico / Exclusivo (Vermelho/Arco-íris)
* **Tipos de Itens:**
  - `[Ex: Armas, Armaduras/Capacetes, Poções/Consumíveis, Chaves, Acessórios]`

---

## 9. Interface do Usuário (UI / HUD) & UX

* **Elementos Fixos na Tela (HUD em Jogo):**
  - [ ] Barra de Vida (Health Bar)
  - [ ] Barra de Stamina / Energia / Mana
  - [ ] Contador de Moedas / Recursos no topo
  - [ ] Bússola ou Mini-mapa
  - [ ] Indicador de Habilidades & Cooldowns (Ícones com tempo)
* **Menus e Telas Secundárias:**
  - [ ] Menu de Inventário / Equipamento
  - [ ] Loja de Itens / NPCs
  - [ ] Menu de Configurações
  - [ ] Tela de Morte / Respawn customizada
  - [ ] Janela de Diálogo com NPCs (Estilo caixa de texto RPG)
* **Paleta de Cores e Estilo Visual da UI:**
  - `[Ex: Interface escura moderna com bordas douradas e cantos arredondados]`

---

## 10. Multiplayer & Servidores

* **Jogadores por Servidor:** `[Ex: 1 jogador solo, 4 jogadores co-op, 20 jogadores MMO, 50 jogadores]`
* **Modo de Jogo:**
  - [ ] Cooperativo (PvE / Jogadores contra Monstros/Ambiente)
  - [ ] Competitivo (PvP livre ou por Equipes)
  - [ ] Misto (Zonas Seguras + Zonas de PvP livre)
* **Sistema de Grupos / Parties:**
  - Jogadores podem formar equipe para dividir XP/recompensas? `[Sim / Não]`

---

## 11. Monetização (Gamepasses & Produtos)

* **Gamepasses Planejados:**
  1. `[Ex: VIP - Tag no chat + 1.5x moedas]`
  2. `[Ex: Inventário Extra - +20 slots]`
  3. `[Ex: Rádio / Música / Efeitos cosméticos]`
* **Developer Products (Compras repetíveis com Robux):**
  1. `[Ex: Pacote de 500 Moedas]`
  2. `[Ex: Reviver Instantâneo]`

---

## 12. Escopo do MVP (Versão Mínima Jogável - Fase 1)

> **Regra de Ouro:** O que precisamos ter funcionando **hoje e nos próximos commits** para o jogo já ser divertido e testável no Roblox Studio?

* [ ] **Sistema 1:** `[Ex: Movimentação avançada com Stamina e Dash]`
* [ ] **Sistema 2:** `[Ex: Coleta de moedas pelo mapa com salvamento no DataStore]`
* [ ] **Sistema 3:** `[Ex: Sistema de combate básico Melee contra dummies/bonecos de teste]`
* [ ] **Sistema 4:** `[Ex: HUD com barra de vida e contador de moedas]`

---

## 13. Notas Adicionais & Decisões da Equipe

`[Escreva livremente aqui qualquer detalhe técnico, ideias loucas ou regras específicas que você e seu parceiro conversaram]`
