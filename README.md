<p align="center">
  <img src="https://vectorseek.com/wp-content/uploads/2023/08/WorldSkills-Logo-Vector.svg-.png" alt="WorldSkills Logo" width="250"/>
</p>

<h1 align="center"> WorldsSkills - #23 Robótica Móvel </h1>

<p align="center">
  Repositório dedicado a atualizações diárias sobre o robô com o kit Studica para a WorldSkills.
</p>

---

# 🤖 Projeto de Robótica: Montagem, Estruturação e Integração Eletrônica (Kit Studica Lion)

Este repositório documenta o cronograma de desenvolvimento, montagem mecânica e integração de hardware do robô construído a partir do ecossistema da **Studica Robotics**. O projeto utiliza uma configuração de chassi triangular de alta mobilidade com foco em robustez estrutural e organização interna de componentes.

---

## 🛠️ Histórico de Desenvolvimento e Diário de Bordo

### 📅 Etapa 1: Ambientação Mecânica e Elétrica Base
O foco inicial foi a estruturação do núcleo de movimentação e a distribuição primária de energia pelo chassi.
* **Montagem Estrutural:** Alinhamento e fixação das vigas para a composição do chassi triangular, garantindo a rigidez necessária para suportar impactos.
* **Sistema de Tração:** Instalação e acoplamento dos 3 motores aos eixos. Foi realizada a verificação do torque manual e do alinhamento geométrico para evitar perdas por atrito.
* **Infraestrutura Elétrica:** Mapeamento inicial do barramento de energia e passagem dos cabos de alimentação principais do Kit Lion.

### 📅 Etapa 2: Fixação da Eletrônica e Fechamento Estrutural
Com a base mecânica consolidada, o trabalho concentrou-se na eletrônica de controle e na segurança dos componentes.
* **Fixação dos Controladores:** Posicionamento estratégico e fixação mecânica rígida do **VXM** e do **Titan Quad** na placa superior do robô, minimizando vibrações que poderiam comprometer as conexões.
* **Instalação das Chapas de Acrílico:** Dimensionamento, furação e instalação das placas de acrílico personalizadas. As chapas atuam tanto como fechamento estético quanto como barreira de proteção física para os componentes internos e fiação contra detritos externos.

---

## 📐 Especificações Técnicas do Hardware Utilizado

| Componente / Subsistema | Modelo / Tipo | Função e Descrição Técnica |
| :--- | :--- | :--- |
| **Kit de Desenvolvimento** | Studica Lion | Ecossistema padronizado de peças estruturais, mecânicas e conexões elétricas. |
| **Chassi** | Triangular | Geometria otimizada para distribuição de peso e manobrabilidade em 3 eixos de tração. |
| **Atuadores** | 3 Motores DC | Responsáveis pela propulsão e deslocamento dinâmico do robô. |
| **Controlador Principal** | Titan Quad | Controladora de motores de alta performance, responsável pela modulação de potência e leitura de encoders. |
| **Co-processador / Interface**| VXM | Unidade de gerenciamento auxiliar instalada na placa superior para expansão de portas e lógica de sensores. |
| **Blindagem Externa** | Chapas de Acrílico | Painéis de policarbonato/acrílico para fechamento lateral, isolamento elétrico e proteção contra impactos. |

---

## 🔌 Status do Mapeamento de Componentes (Placa Superior)

A organização da placa superior foi projetada para otimizar o *Cable Management* (gerenciamento de cabos), deixando as portas de dados e alimentação logicamente acessíveis:

```
+---------------------------------------------------+
|               [ CHASSI TRIANGULAR ]               |
|                                                   |
|      +-------------------------------------+      |
|      |          PLACA SUPERIOR             |      |
|      |                                     |      |
|      |    +--------------+                 |      |
|      |    |  TITAN QUAD  |   [Acrílico]    |      |
|      |    +--------------+                 |      |
|      |                                     |      |
|      |    +--------------+                 |      |
|      |    |     VXM      |   [Acrílico]    |      |
|      |    +--------------+                 |      |
|      |                                     |      |
|      +-------------------------------------+      |
|                                                   |
+---------------------------------------------------+
```

---

## 🚀 Próximas Fases do Projeto
- [ ] Conectar os componentes elétricos dos 3 motores diretamente ao Titan Quad.
- [ ] Prender a bateria ao robô
- [ ] Realizar a crimpagem e organização final dos cabos de sinal e sensores utilizando malhas náuticas e organizadores.
- [ ] Configurar o ambiente de software para comunicação entre o VXM e o Titan Quad.
- [ ] Executar os primeiros testes de bancada para calibração dos motores e validação do sentido de rotação
