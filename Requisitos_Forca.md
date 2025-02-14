# Requisitos do Jogo de Forca Online

## 1. Descrição do Projeto
O objetivo deste projeto é desenvolver um jogo de forca online. O cliente solicitou um jogo interativo, mas não especificou todos os detalhes. Portanto, a equipe de desenvolvimento é responsável por definir as funcionalidades e a forma como o jogo funcionará, garantindo uma experiência envolvente e intuitiva para os usuários.

---

## 2. Requisitos Funcionais
Os requisitos funcionais especificam **o que o sistema deve fazer**, detalhando as funcionalidades e comportamentos esperados.

### RF 
- O sistema deve apresentar uma tela inicial com as seguintes opções:
  - Iniciar Jogo
  - Instruções
  - Sair do jogo

### RF 
- O sistema deve permitir o modo de jogo **Multiplayer:** Partidas entre dois jogadores.

### RF
- O sistema deve iniciar uma nova partida ao selecionar a opção "Iniciar Jogo" na tela inicial.

### RF
- O sistema deve permitir que o jogador escolha se quer hospedar uma partida ou jogar em uma partida existente.

### RF 
- O sistema deve exibir se o usuário é o jogador 1, o que hospedou a partida, ou o jogador 2, o que vai jogar a partida.

### RF
- No modo multiplayer, um jogador deve poder inserir a palavra secreta enquanto o outro tenta adivinhar.

### RF
- O sistema deve permitir que o jogador 1 dono da sala dê dicas para o outro jogador.
- O sistema deve permitir que o jogador 2 visualize as dicas do jogador 1.

### RF 
- O sistema deve permitir que o jogador insira letras para tentar adivinhar a palavra.
- O sistema deve validar a entrada para aceitar apenas letras do alfabeto.

### RF 
- O sistema deve exibir as letras corretas na posição correta na palavra secreta.
- O sistema deve listar as letras erradas tentadas pelo jogador.

### RF
- O sistema deve exibir uma mensagem de vitória caso o jogador adivinhe a palavra antes de esgotar as tentativas.
- O sistema deve exibir uma mensagem de derrota caso o jogador esgote todas as tentativas.
- O sistema deve oferecer a opção de reiniciar o jogo ou retornar à tela inicial.

### RF 
- O sistema deve permitir partidas multiplayer em tempo real.
- O sistema deve gerenciar a vez de cada jogador e garantir que apenas um jogue por vez.
- O sistema deve permitir chat entre os jogadores durante a partida.

---

## 3. Requisitos Não Funcionais
Os requisitos não funcionais definem **como o sistema deve se comportar**, especificando restrições e qualidades do sistema, de acordo com a [ISO25010](https://blog.onedaytesting.com.br/iso-iec-25010/).

### RNF01 - Desempenho
- O sistema deve carregar a tela inicial em menos de **2 segundos**.
- O sistema deve iniciar a partida em no máximo **1 segundo**.

### RNF02 - Usabilidade
- O sistema deve ter uma interface intuitiva e fácil de usar, com botões visíveis e bem descritos.
- O sistema deve fornecer feedback claro ao usuário em cada ação (como letras corretas e erradas).

### RNF03 - Confiabilidade
- O sistema deve manter o estado da partida mesmo em caso de falha de conexão para o modo multiplayer.
- O sistema deve garantir a integridade dos dados das partidas em andamento.

### RNF04 - Segurança
- No modo multiplayer, as comunicações devem ser criptografadas para proteger a privacidade dos jogadores.

### RNF05 - Compatibilidade
- O sistema deve ser compatível com os navegadores mais utilizados: Google Chrome, Mozilla Firefox, Safari e Microsoft Edge.
- O sistema deve ser responsivo e funcionar em dispositivos móveis, tablets e desktops.

### RNF06 - Escalabilidade
- O sistema deve suportar até 2 jogadores simultâneos na mesma partida e 50 espectadores no modo multiplayer.


---

