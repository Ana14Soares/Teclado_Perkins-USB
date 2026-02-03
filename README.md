# Teclado Perkins USB

O Teclado Perkins via USB é um periférico voltado para entrada de texto em Braille, baseado no layout de seis teclas do padrão Perkins. A comunicação ocorre via USB HID, permitindo reconhecimento nativo pelo sistema operacional sem a necessidade de drivers adicionais. O firmware interpreta combinações simultâneas das teclas (pontos 1 a 6), mapeando-as para seus respectivos caracteres, além de suportar funções complementares como espaço, backspace e enter. Essa solução garante precisão, responsividade e acessibilidade para usuários que dependem da leitura e escrita em Braille.

## Funcionalidades 

- `Conexão via USB`: Reconhecimento automático como teclado padrão, sem drivers.
- `Tecla de enter`: Realiza quebras de linha e confirma comandos.
- `Tecla de backspace`: Apaga caracteres digitados.
- `Tecla de prefixo maiúsculo`: Ativa letras maiúsculas e Caps Lock.
- `Tecla de shift`: Permite o uso de símbolos especiais.
- `Setas de orientação`: Setas direcionais integradas para controle do cursor no computador.
- `MP3 para feedback de áudio`: Feedback por voz para cada tecla e modo ativado.

## Tecnologias Utilizadas

**Hardware:**  
- **ESP32** – microcontrolador responsável pelo processamento e controle das entradas do teclado Perkins e reprodução de áudio via chip MP3.

**Software e Desenvolvimento:**  

- Arduino IDE – Ambiente principal utilizado para desenvolvimento, programação e upload de código para o ESP32, com suporte nativo às bibliotecas e placas da plataforma Arduino/ESP32.

- (Opcional) Visual Studio Code (VSCode) – Pode ser utilizado como editor alternativo para quem preferir, com extensões específicas para Arduino/ESP32.

**Simulação e Testes:**  
- **Wokwi** – plataforma de simulação online para testar circuitos e código do ESP32 antes da implementação física.


##  Pinagem

### Pontos Braille

| Ponto | Função  | GPIO |
|-------|---------|------|
| B1    | Ponto 1 | 18   |
| B2    | Ponto 2 | 7    |
| B3    | Ponto 3 | 6    |
| B4    | Ponto 4 | 17   |
| B5    | Ponto 5 | 8    |
| B6    | Ponto 6 | 9    |

### Botões de Função

| Função       | GPIO |
|--------------|------|
| Enter        | 5    |
| Espaço       | 15   |
| Backspace    | 37   |
| Modo Número  | 4    |
| Shift Sticky | 36   |

### Setas

| Direção | GPIO |
|---------|------|
| Cima    | 21   |
| Baixo   | 35   |
| Direita | 48   |
| Esquerda| 47   |

### DFPlayer

| Função | GPIO |
|--------|------|
| RX     | 40   |
| TX     | 39   |

## Forma de utilização dos modos

**Modo Maiúsculo (Caps Lock):**
- Ativado pela combinação Braille 000101 (Pontos 4 e 6). Um toque ativa o modo para a próxima letra; dois toques travam o Caps Lock. O botão Espaço desativa o trava-letras.

**Modo Numérico:**
- Ativado pelo botão físico no pino 4 ou pela combinação Braille 001111 (Pontos 3, 4, 5 e 6).

**Shift:**
- Permite que o próximo caractere digitado seja um símbolo especial (ex: ! ou @) sem ter que segurar o botão.

## Autoras
- [Ana Luiza](https://share.google/TvTGWeP9tyLsO0Y1l)
- [Ana Vírna](https://github.com/anavrna)
- [Maria Fernanda](https://github.com/mariafernandabq)
