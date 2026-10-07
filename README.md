# Anime Fighters Simulator - Clone Otimizado para Baixo Consumo (Godot 4.x)

Projeto completo desenvolvido em **Godot Engine 4.x** (GDScript) com renderizador **Compatibility (OpenGL 3.3 / WebGL 2)**, focado em atingir **60 FPS estáveis** em computadores modestos, laptops antigos com gráficos integrados (Intel HD Graphics) e baixa memória RAM.

---

## 🎮 Controles do Jogo

| Ação | Tecla / Controle | Descrição |
|---|---|---|
| **Mover** | `W`, `A`, `S`, `D` ou Setas | Movimenta o jogador na direção da câmera |
| **Sprint / Correr** | `Shift` (Segurar) | Dobra a velocidade de movimento (12 -> 24) com partículas e FOV dinâmico |
| **Pular** | `Barra de Espaço` | Pulo simples com física cinemática |
| **Orbitar Câmera** | `Botão Direito do Mouse (Segurar e Arrastar)` | Rotação orbital suave (estilo Roblox / MMO) |
| **Zoom da Câmera** | `Roda do Mouse (Scroll Up / Down)` | Ajusta a distância da câmera do jogador |
| **Selecionar Alvo** | `Botão Esquerdo do Mouse (Clique no Inimigo/Chefe)` | Foca o alvo para os lutadores atacarem |
| **Desselecionar Alvo** | `ESC`, `Q` ou clicar no mesmo alvo | Libera o foco dos lutadores |
| **Interagir (Cápsulas / Máquinas / Portais)** | Tecla `E` | Abre a cápsula de gacha, máquina de passivas ou entra no portal |
| **Inventário de Lutadores** | Tecla `I` ou botão HUD | Abre e fecha o painel de inventário (Nível, XP, Passiva, DPS) |
| **Máquina de Passivas** | Tecla `P` ou botão HUD | Rola novas passivas para seus lutadores usando moedas da ilha |
| **Menu das 10 Ilhas** | Tecla `M` ou botão HUD | Visualiza e teleporta entre ilhas desbloqueadas |
| **Equipar Melhores** | Botão HUD / Inventário | Equipa automaticamente os 3 maiores DPS |
| **Salvar Jogo** | Botão HUD | Salva moedas, ilhas, passivas e pets em `user://savegame.json` |

### 📱 Controles Mobile / Touch (Smartphones & Tablets)

| Ação | Controle Touch | Descrição |
|---|---|---|
| **Mover Jogador** | Joystick Virtual Dinâmico | Toque e arraste no quadrante inferior esquerdo (centraliza sob o polegar) |
| **Girar Câmera** | Arrastar na Tela | Arraste o polegar direito na tela (funciona simultaneamente enquanto anda) |
| **Zoom da Câmera** | Pinça (Pinch to Zoom) | Gesto de pinça com 2 dedos para aproximar ou afastar a visão |
| **Centralizar Câmera** | Botão `[🔄 Câmera]` | Recentraliza a visão orbital imediatamente atrás do personagem com 1 toque |
| **Auto-Farm / Auto-Alvo** | Botão `[⚔️ Auto]` | Mira e caça inimigos automaticamente em sequência ao derrotar o anterior |
| **Selecionar Alvo** | Toque no Mob / Botão `[🎯 Alvo]` | Toque na tela (com tolerância de toque ampliada) ou foque o mais próximo |
| **Interagir** | Botão `[💬 Ação]` ou Prompt | Abre cápsula de gacha, máquina de passivas ou entra no portal |
| **Correr / Sprint** | Botão `[⚡ Sprint]` | Alterna corrida rápida (2x velocidade) com indicador visual verde neon |
| **Pular** | Botão `[🦘 Pular]` | Pulo com física e feedback tátil/sonoro |
| **Menu Rápido Superior** | Ícones no Cabeçalho | Acesso instantâneo a Inventário (🎒), Ilhas (🗺️), Passivas (⚙️), Melhores (⭐), Salvar (💾) e Tela Cheia (⛶) |

---

## 🗺️ Tabela de Balanceamento das 10 Ilhas de Anime

> **Atualização de Economia:**
> - Inimigos comuns agora concedem o **dobro** de moedas.
> - Chefes centrais concedem **5x mais moedas** que antes (equivalente ao custo integral de uma cápsula).

| # | Ilha / Tema Anime | Moeda Local | Mob HP | Mob Drop (2x) | Chefe Central | Chefe HP | Chefe Drop (5x) | Custo Cápsula | Custo Reroll |
|---|---|---|---|---|---|---|---|---|---|
| **1** | **Vila da Folha (Naruto)** | Ienes Ninja | 100 | **20** | Chefe Madara Uchiha | 1.000 | **100** | 100 | 50 |
| **2** | **Reino de Liones (Nanatsu no Taizai)** | Moedas de Liones | 500 | **120** | Chefe Rei Demônio | 5.000 | **600** | 600 | 300 |
| **3** | **Região Pokémon (Pokémon)** | Pokédólares | 2.500 | **700** | Chefe Mewtwo Armadurado | 25.000 | **3.500** | 3.500 | 1.750 |
| **4** | **Grande Rota (One Piece)** | Berries | 12.000 | **4.000** | Chefe Kaido Rei das Feras | 120.000 | **20.000** | 20.000 | 10.000 |
| **5** | **Academia U.A. (Boku no Hero)** | Créditos Heroicos | 60.000 | **24.000** | Chefe All For One | 600.000 | **120.000** | 120.000 | 60.000 |
| **6** | **Estádio Egoísta (Blue Lock)** | Pontos Ego | 300.000 | **140.000** | Chefe Noel Noa | 3.000.000 | **700.000** | 700.000 | 350.000 |
| **7** | **Ringue Kamogawa (Hajime no Ippo)** | Luvas de Ouro | 1.500.000 | **800.000** | Chefe Ricardo Martinez | 15.000.000 | **4.000.000** | 4.000.000 | 2.000.000 |
| **8** | **Planeta Namekusei (Dragon Ball Z)** | Esferas de Namek | 8.000.000 | **5.000.000** | Chefe Freeza 100% | 80.000.000 | **25.000.000** | 25.000.000 | 12.500.000 |
| **9** | **Mundo dos Stands (JoJo's)** | Flechas de Stand | 45.000.000 | **30.000.000** | Chefe DIO Over Heaven | 450.000.000 | **150.000.000** | 150.000.000 | 75.000.000 |
| **10** | **Torneio do Poder (DB Super)** | Energia dos Deuses | 300.000.000 | **200.000.000** | Chefe Jiren Supremo | 3.000.000.000 | **1.000.000.000** | 1.000.000.000 | 500.000.000 |

---

## 🌟 Sistema de Passivas e Reroll

- ⚪ **Comum (50%):** *Ataque I* (+10% Dano), *Agilidade I* (+10% Vel. Ataque)
- 🔵 **Raro (30%):** *Ataque II* (+25% Dano), *Magnata I* (+35% Moedas)
- 🟣 **Épico (13%):** *Guerreiro Feroz* (+60% Dano), *Estudioso* (+75% XP)
- 🟡 **Lendário (6%):** *Destruidor* (+130% Dano)
- 🔴 **Mítico (1%):** *Divindade Celestial* (+300% Dano, +40% Vel. Ataque, +100% Moedas)

---

## 🆙 Sistema de Níveis e XP (Teto Nv. 250)

- **Fórmula de XP:** $\text{xp\_necessário}(N) = \lfloor 100 \times 1.035^{N - 1} + (N \times 50) \rfloor$
- **Bônus de Nível:** +1.4% de dano base por nível acima de 1.
- **Distribuição:** Inimigos e Chefes concedem XP compartilhado para todos os lutadores equipados.

---

## 📁 Estrutura de Arquivos

```
├── project.godot                     # Configuração do Godot 4 (GL Compatibility, Autoloads)
├── play_demo.html                    # Demo 3D jogável completa no navegador
├── scenes/
│   ├── main/
│   │   └── World.tscn                # Cena principal integrando as 10 ilhas, iluminação e jogador
│   ├── entities/
│   │   ├── Player.tscn               # Jogador CharacterBody3D com sprint e câmera orbital
│   │   ├── Fighter.tscn              # Pet/Lutador com lógica de ataque, nível e passivas
│   │   ├── Enemy.tscn                # Inimigo comum com barra de HP em SubViewport
│   │   └── BossEnemy.tscn            # Chefe central (1.9x escala, respawn 15s, 5x moedas)
│   ├── world/
│   │   ├── Spawner.tscn              # Spawner de mobs
│   │   ├── GachaCapsule.tscn         # Estação de sorteio interativa por ilha
│   │   ├── PassiveMachine.tscn       # Estação 3D da Máquina de Passivas
│   │   └── IslandPortal.tscn         # Portal de compra e teleporte entre ilhas
│   └── ui/
│       ├── HUD.tscn                  # Moedas, alvo atual, atalhos [I], [M], [P]
│       ├── InventoryUI.tscn          # Grid de lutadores (Nv. 250, barra de XP, passivas, DPS)
│       ├── PassiveUI.tscn            # Interface de rolagem de passivas
│       └── IslandMenuUI.tscn         # Menu de teleporte rápido entre ilhas
└── scripts/
    ├── autoloads/
    │   ├── IslandData.gd             # Tabela de balanceamento, 10 ilhas, passivas e fórmulas
    │   ├── SaveManager.gd            # Salvamento automático e persistência
    │   └── GameManager.gd            # Estado global, moedas, XP em equipe e rerolls
    ├── entities/
    │   ├── Player.gd
    │   ├── Fighter.gd
    │   ├── Enemy.gd
    │   └── BossEnemy.gd
    ├── world/
    │   ├── Spawner.gd
    │   ├── GachaCapsule.gd
    │   ├── PassiveMachine.gd
    │   ├── IslandPortal.gd
    │   └── World.gd
    └── ui/
        ├── HUD.gd
        ├── InventoryUI.gd
        ├── PassiveUI.gd
        └── IslandMenuUI.gd
```

---

## 🚀 Como Executar

1. **No Godot 4.x:** Abra a Godot Engine 4.2+ ou 4.3+, importe o projeto e inicie a cena `res://scenes/main/World.tscn`.
2. **No Navegador:** Dê um duplo clique em `play_demo.html` para jogar imediatamente com gráficos 3D low-poly a 60 FPS.
