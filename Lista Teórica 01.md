# Lista Teórica 01 - Exercícios sobre Tópicos Introdutórios

---

## Exercício 1 — Especificações de Ambiente de Tarefa

### Ar-condicionado

| Campo | Descrição |
|------|----------|
| Agente | Sistema de controle do ar-condicionado |
| Medida de desempenho | Manter temperatura no valor desejado, eficiência energética |
| Ambiente | Ambiente interno (sala/escritório) |
| Atuadores | Compressor, ventilador, resistência, termostato |
| Sensores | Sensor de temperatura, sensor de umidade |

---

### Robô jogador de futebol

| Campo | Descrição |
|------|----------|
| Agente | Robô autônomo jogador |
| Medida de desempenho | Número de gols marcados, posse de bola, não levar gols |
| Ambiente | Campo de futebol, bola, outros robôs (adversários e aliados) |
| Atuadores | Motores de locomoção, mecanismo de chute/passe |
| Sensores | Câmera, sensor de distância (ultrassom/LIDAR), sensor de posição (GPS/odometria) |

---

### Casa automatizada

| Campo | Descrição |
|------|----------|
| Agente | Sistema de automação residencial |
| Medida de desempenho | Conforto dos moradores, segurança, eficiência energética |
| Ambiente | Cômodos da casa, presença de moradores, condições externas (clima, luminosidade) |
| Atuadores | Interruptores de luz, fechaduras, ar-condicionado, cortinas motorizadas, alarmes |
| Sensores | Sensor de presença, sensor de luminosidade, sensor de temperatura, câmeras, sensor de fumaça |

---

### Veículo autônomo

| Campo | Descrição |
|------|----------|
| Agente | Sistema de direção autônoma |
| Medida de desempenho | Viagem segura, rápida, dentro das leis de trânsito, confortável |
| Ambiente | Estradas, outros veículos, pedestres, sinalização, condições climáticas |
| Atuadores | Direção, acelerador, freio, sinaleiros, buzina |
| Sensores | Câmeras, LIDAR, radar, GPS, velocímetro, acelerômetro, sensores do motor |

---

### Semáforo inteligente

| Campo | Descrição |
|------|----------|
| Agente | Sistema de controle semafórico |
| Medida de desempenho | Minimizar tempo de espera, reduzir congestionamento, priorizar emergências |
| Ambiente | Cruzamento, vias, veículos, pedestres, veículos de emergência |
| Atuadores | Sinais luminosos (vermelho/amarelo/verde), painéis de mensagem |
| Sensores | Câmeras de tráfego, sensores de presença indutivos no asfalto, sensor de veículos de emergência |

---

## Exercício 2 — Tabela Comparativa de Propriedades de Ambientes

| Propriedade | Carro Autônomo | Classificação de Peças (Visão Comp.) | Agente Jogador de Xadrez | Sistema de Diagnóstico Médico |
|------------|---------------|--------------------------------------|---------------------------|-------------------------------|
| Observabilidade | Parcialmente observável | Completamente observável | Completamente observável | Parcialmente observável |
| Nº de agentes | Multiagente | Agente único | Multiagente (competitivo) | Agente único |
| Determinismo | Estocástico | Determinístico | Determinístico | Estocástico |
| Temporalidade | Sequencial | Episódico | Sequencial | Sequencial |
| Dinamismo | Dinâmico | Estático | Estático (semi-dinâmico¹) | Estático |
| Continuidade | Contínuo | Discreto | Discreto | Contínuo |
| Conhecimento | Parcialmente conhecido | Conhecido | Conhecido | Parcialmente conhecido |

---

## Exercício 3 — Artigo Científico com Aplicação de Agentes Inteligentes

### Referência

MNIH, V. *et al.* Human-level control through deep reinforcement learning. *Nature*, v. 518, n. 7540, p. 529–533, 2015.  
Disponível em: <https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf>  
Acesso em: 18 abr. 2026.

---

### Descrição das principais características

O artigo propõe o agente DQN (Deep Q-Network), que combina Aprendizado por Reforço com redes neurais profundas (Deep Learning) para aprender a jogar jogos do Atari 2600 diretamente a partir de pixels da tela, sem nenhum conhecimento prévio das regras. O agente superou o desempenho humano em diversas modalidades.

---

### Especificações do Ambiente de Tarefa

| Campo | Descrição |
|------|----------|
| Agente | DQN — agente de aprendizado por reforço profundo |
| Medida de desempenho | Pontuação acumulada no jogo (maximizar recompensa) |
| Ambiente | Tela do jogo Atari (pixels), regras internas do jogo |
| Atuadores | Ações do joystick (mover, atirar, pular etc.) |
| Sensores | Pixels da tela do jogo (imagem 84×84 em escala de cinza) |

---

### Propriedades do Ambiente de Tarefa

| Propriedade | Classificação | Justificativa |
|------------|--------------|--------------|
| Observabilidade | Parcialmente observável | O agente vê apenas o frame atual da tela, sem acesso ao estado interno do jogo |
| Nº de agentes | Agente único | Somente o DQN age no ambiente (inimigos são parte do ambiente) |
| Determinismo | Estocástico | Elementos aleatórios no comportamento dos inimigos e eventos do jogo |
| Temporalidade | Sequencial | Cada ação afeta o estado futuro do jogo |
| Dinamismo | Dinâmico | O ambiente muda continuamente, mesmo sem ação do agente |
| Continuidade | Discreto | Ações e frames são discretos |
| Conhecimento | Desconhecido (inicialmente) | O agente não conhece as regras; aprende explorando o ambiente |
