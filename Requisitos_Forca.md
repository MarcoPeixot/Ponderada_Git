# Especificação de Requisitos do Jogo da Forca Online
=====================================================

## 1. Descrição do Projeto
O objetivo deste projeto é desenvolver um jogo de forca online. O cliente solicitou um jogo interativo, mas não especificou todos os detalhes. Portanto, a equipe de desenvolvimento é responsável por definir as funcionalidades e a forma como o jogo funcionará, garantindo uma experiência envolvente e intuitiva para os usuários.



## 2. Requisitos Funcionais
------------------------

### RF01 - Sistema de Autenticação
- O sistema deve permitir registro de novos usuários
- O sistema deve implementar login com senha segura
- O sistema deve suportar autenticação social (Google/Facebook)
- O sistema deve manter sessão ativa por 8 horas

### RF02 - Interface Principal
- O sistema deve apresentar uma tela inicial com as seguintes opções:
  * Iniciar Jogo
  * Ver Ranking Global
  * Minhas Estatísticas
  * Loja de Itens
  * Sair do jogo

### RF03 - Sistema de Partidas
- O sistema deve permitir criar salas privadas com senhas
- O sistema deve manter uma lista de partidas em andamento
- O sistema deve permitir espectadores assistirem às partidas
- O sistema deve suportar até 50 espectadores por partida

### RF04 - Modo Multiplayer
- O sistema deve permitir partidas entre dois jogadores
- O sistema deve iniciar uma nova partida ao selecionar "Iniciar Jogo"
- O sistema deve permitir que o jogador escolha entre:
  * Hospedar uma nova partida
  * Entrar em uma partida existente
- O sistema deve exibir claramente se é jogador 1 (anfitrião) ou jogador 2 (convidado)

### RF05 - Mecânica de Jogo
- No modo multiplayer, um jogador deve poder inserir a palavra secreta
- O outro jogador deve tentar adivinhar a palavra letra por letra
- O sistema deve validar entrada apenas para letras do alfabeto
- O sistema deve exibir:
  * Letras corretas na posição correta
  * Lista de letras erradas tentadas
  * Quantidade de tentativas restantes

### RF06 - Sistema de Chat
- O sistema deve permitir comunicação em tempo real entre jogadores
- O sistema deve suportar emojis e formatação básica de texto
- O sistema deve manter histórico de mensagens durante a partida
- O sistema deve permitir silenciar outros jogadores

### RF07 - Sistema de Recompensas
- O sistema deve oferecer recompensas diárias por login consecutivo
- O sistema deve conceder troféus por conquistas especiais
- O sistema deve permitir compra de itens cosméticos
- O sistema deve manter inventário de itens adquiridos

## 3. Requisitos Não Funcionais
---------------------------

### RNF01 - Desempenho
- O sistema deve carregar a tela inicial em menos de 2 segundos
- O sistema deve iniciar uma nova partida em até 1 segundo
- O sistema deve processar mensagens do chat em menos de 100ms
- O sistema deve manter latência inferior a 200ms nas partidas

### RNF02 - Usabilidade
- O sistema deve ter interface intuitiva e fácil de usar
- O sistema deve fornecer feedback claro para todas as ações
- O sistema deve suportar navegação por teclado
- O sistema deve oferecer tema claro e escuro

### RNF03 - Confiabilidade
- O sistema deve manter estado da partida mesmo com falhas de conexão
- O sistema deve garantir integridade dos dados das partidas
- O sistema deve implementar reconexão automática
- O sistema deve manter histórico de partidas por 30 dias

### RNF04 - Segurança
- Todas as comunicações devem ser criptografadas (HTTPS/TLS)
- Senhas devem ser armazenadas com hash seguro
- Sistema deve implementar rate limiting
- Sistema deve validar todos os inputs do usuário

### RNF05 - Compatibilidade
- Sistema deve ser compatível com navegadores Chrome, Firefox e Safari
- Sistema deve funcionar em dispositivos móveis, tablets e desktops
- Sistema deve se adaptar automaticamente ao tamanho da tela
- Sistema deve suportar resoluções mínimas de 320px

### RNF06 - Escalabilidade
- Sistema deve suportar até 2 jogadores simultâneos por partida
- Sistema deve permitir até 50 espectadores por partida
- Sistema deve suportar até 1000 usuários online simultaneamente
- Sistema deve manter performance com 90% de carga

## 4. Matriz de Correlação
---------------------------

| Requisito Funcional | Requisitos Não Funcionais Relacionados |
|--------------------|----------------------------------------|
| RF01               | RNF04 (Segurança)                      |
| RF02               | RNF02 (Usabilidade)                    |
| RF03               | RNF03 (Confiabilidade), RNF06 (Escalabilidade) |
| RF04               | RNF01 (Desempenho), RNF03 (Confiabilidade)    |
| RF05               | RNF01 (Desempenho), RNF02 (Usabilidade)      |
| RF06               | RNF01 (Desempenho), RNF02 (Usabilidade)      |
| RF07               | RNF03 (Confiabilidade), RNF04 (Segurança)     |

## 5. Casos de Uso
--------------

### UC01 - Criar Partida
1. Jogador seleciona opção "Hospedar Partida"
2. Sistema solicita palavra secreta
3. Jogador insere palavra válida
4. Sistema cria sala com código único
5. Sistema aguarda conexão do segundo jogador

### UC02 - Entrar em Partida
1. Jogador seleciona opção "Entrar em Partida Existente"
2. Sistema exibe lista de salas disponíveis
3. Jogador seleciona sala desejada
4. Sistema verifica se sala está disponível
5. Sistema conecta jogador à partida

### UC03 - Realizar Jogada
1. Jogador digita letra para tentativa
2. Sistema valida entrada
3. Sistema processa jogada
4. Sistema atualiza estado da partida
5. Sistema notifica resultado ao jogador


## 6. Diagrama
-------------

De acordo com os requisitos mencionados, foi gerado um diagrama do fluxo de negócios do jogo da forca na IA [Phind](https://www.phind.com/).

![alt text](<Untitled diagram-2025-02-14-153643.png>)

O diagrama acima representa o fluxo completo do jogo, onde:
- Os retângulos representam estados ou telas do sistema
- As setas indicam possíveis transições entre estados
- Os estados aninhados (como dentro de "IniciarJogo") mostram subprocessos específicos
- O asterisco ([*]) indica o ponto inicial de cada estado

## Histórico de Versões
- v1.0.0: Documentação inicial dos requisitos
