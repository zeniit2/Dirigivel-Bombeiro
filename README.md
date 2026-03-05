# 🚒 Dirigível Bombeiro

Projeto desenvolvido como parte de uma **Iniciação Científica**, cujo objetivo é construir um **dirigível experimental controlado remotamente** capaz de identificar e apagar focos de incêndio simulados em uma maquete.

O sistema utiliza um **dirigível preenchido com hélio**, equipado com **câmera embarcada (ESP32-CAM)** e propulsão elétrica. O dirigível sobrevoará uma maquete que simula uma área com incêndios, representados por **LEDs vermelhos**.

Quando o operador posiciona corretamente a câmera sobre um LED, o sistema registra o evento e **desliga o LED**, representando um **foco de incêndio apagado**.

Este projeto busca demonstrar conceitos de **engenharia aeronáutica básica, robótica aérea, sistemas embarcados e monitoramento remoto** aplicados a um contexto de combate a incêndios.

---

# 📌 Objetivo do Projeto

O objetivo do projeto é demonstrar, de forma prática e didática, como **veículos aéreos mais leves que o ar (LTA - *Lighter Than Air*)** podem ser utilizados em missões de **monitoramento e apoio ao combate de incêndios**, principalmente em regiões de difícil acesso.

A proposta é criar um sistema que permita:

- Sobrevoar uma área simulada
- Identificar focos de incêndio
- Interagir com o ambiente simulando o combate ao fogo
- Registrar eventos de incêndios apagados

A simulação será realizada utilizando uma **maquete com LEDs representando focos de incêndio**, permitindo criar um ambiente controlado para testes e demonstrações.

---

# 🎈 Estrutura do Dirigível

O dirigível será construído no formato clássico de **zepelim**, com um balão preenchido com **hélio**, responsável por gerar a sustentação do sistema.

### Dimensões do Balão

- **Formato:** Elipse (formato típico de dirigíveis)
- **Comprimento:** 155 cm
- **Diâmetro:** 40 cm
- **Gás utilizado:** Hélio

O formato elíptico foi escolhido para proporcionar **maior estabilidade durante o voo e menor resistência aerodinâmica**, além de reproduzir o formato tradicional de dirigíveis utilizados em aplicações reais.

---

# ⚙️ Componentes do Sistema

O dirigível será composto por um conjunto de componentes eletrônicos responsáveis pela **propulsão, transmissão de vídeo e controle da câmera**.

### Componentes principais

**ESP32-CAM**

Microcontrolador responsável por:

- Capturar vídeo em tempo real
- Transmitir a imagem para o operador
- Servir como sistema embarcado principal

**Motores Coreless (2 unidades)**

Motores responsáveis pela **propulsão do dirigível**, permitindo deslocamento e controle de direção.

**Servos motores**

Utilizados para controlar o movimento da câmera da ESP32-CAM, permitindo que o operador ajuste o **ângulo de visão** durante o voo.

**Bateria LiPo**

Fonte de alimentação para todo o sistema embarcado.

A bateria será responsável por alimentar:

- ESP32-CAM
- Servos
- Motores

---

# 🎮 Controle do Dirigível

O dirigível será operado remotamente por um usuário que visualizará **em tempo real a imagem transmitida pela ESP32-CAM**.

O operador será responsável por:

- Controlar a direção do dirigível
- Ajustar o posicionamento da câmera
- Identificar focos de incêndio na maquete
- Mirar a câmera sobre o LED correspondente

Essa interação cria uma experiência semelhante a um **sistema de monitoramento aéreo remoto**.

---

# 🔥 Sistema de Simulação de Incêndio

No solo será construída uma **maquete que representa uma área afetada por incêndios**.

Nessa maquete serão instalados **LEDs vermelhos**, que representarão **focos de incêndio ativos**.

### Funcionamento da simulação

1. Os LEDs vermelhos acendem representando incêndios ativos.
2. O dirigível sobrevoa a área.
3. O operador utiliza a câmera para localizar o foco.
4. Ao mirar corretamente o LED com a câmera:
   
   - O sistema identifica o foco
   - O LED é desligado
   - O evento é registrado como **incêndio apagado**

Esse processo permite simular de forma interativa um **cenário de combate a incêndios**.

---

# 🧭 Funcionamento Geral do Sistema

Fluxo simplificado do funcionamento do projeto:
Maquete com LEDs (incêndios)
↓
Dirigível sobrevoa a área
↓
ESP32-CAM transmite vídeo
↓
Operador identifica o foco
↓
Câmera mira no LED
↓
Sistema registra o evento
↓
LED é desligado (incêndio apagado)

---

# 📡 Arquitetura do Sistema

O projeto integra três partes principais:

1. Plataforma aérea (dirigível)
2. Sistema de visão embarcado
3. Sistema de simulação de incêndio
         Dirigível
    ┌─────────────────┐
    │    ESP32-CAM    │
    │                 │
    │  Servo Pan/Tilt │
    │                 │
    │ Motores Coreless│
    └─────────┬───────┘
              │
              │ Vídeo
              │
         Operador
              │
              │ Interação
              ↓
      Maquete com LEDs
     (focos de incêndio)
     
---

# 🧪 Aplicações Educacionais

Este projeto permite explorar diversos conceitos importantes de engenharia e tecnologia, como:

- Aerodinâmica básica
- Sustentação por gás leve
- Robótica aérea
- Sistemas embarcados
- Controle remoto
- Sensoriamento visual
- Simulações de combate a incêndios

Além disso, serve como **plataforma educacional para ensino de robótica e engenharia**, demonstrando na prática a integração entre diferentes áreas tecnológicas.

---

# 📁 Estrutura do Repositório
dirigivel-bombeiro/

firmware/
esp32_cam/
controle_motores/

eletronica/
esquematicos/
pcb/

mecanica/
estrutura/
suporte_motores/

simulacao_incendio/
controle_leds/


---

# 🚀 Possíveis Evoluções do Projeto

O projeto pode evoluir futuramente para incorporar novas tecnologias, como:

- Detecção automática de incêndios usando visão computacional
- Sistema de estabilização automática
- Controle semi-autônomo
- Reconhecimento de focos de calor
- Navegação assistida

Essas melhorias aproximariam o sistema de aplicações reais utilizadas em **monitoramento ambiental e combate a incêndios florestais**.

---

# 👨‍🔬 Projeto de Iniciação Científica

Este projeto está sendo desenvolvido como parte de uma **Iniciação Científica**, com o objetivo de aplicar conceitos de engenharia e tecnologia em um sistema experimental funcional.

O desenvolvimento envolve áreas como:

- Engenharia
- Sistemas embarcados
- Robótica
- Aerodinâmica
- Simulação de cenários de emergência

---

# 📜 Licença

Projeto desenvolvido para **fins educacionais e acadêmicos**.
