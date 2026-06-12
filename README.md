<p align="center">
  <img src="https://vectorseek.com/wp-content/uploads/2023/08/WorldSkills-Logo-Vector.svg-.png" alt="WorldSkills Logo" width="250"/>
</p>

<h1 align="center"> WorldsSkills - #23 Robótica Móvel </h1>

<p align="center">
  Repositório dedicado a atualizações diárias sobre o robô com o kit Studica para a WorldSkills.
</p>

# 🤖 Projeto de Robótica: Montagem, Estruturação e Integração Eletrônica (Kit Studica Lion)

Este repositório documenta o cronograma de desenvolvimento, montagem mecânica, elétrica, programação e integração de hardware do robô construído a partir do ecossistema da **Studica Robotics**. O projeto utiliza uma configuração de chassi triangular de alta mobilidade com foco em robustez estrutural e organização interna de componentes.

---

## 🛠️ Histórico de Desenvolvimento e Diário de Bordo

### 📅 Segunda-Feira: Ambientação Mecânica e Alinhamento Base
O foco inicial foi a estruturação do núcleo de movimentação e a montagem da base física do robô.
* **Montagem Estrutural:** Alinhamento e fixação das vigas de alumínio para a composição do chassi triangular, aplicando aperto cruzado nos parafusos para garantir a rigidez necessária e evitar torções.
* **Sistema de Tração:** Instalação e acoplamento mecânico dos 3 motores DC aos suportes do chassi, com verificação manual do torque de rotação dos eixos para evitar perdas por atrito.

### 📅 Terça-Feira: Infraestrutura Elétrica e Organização Base
Com a base validada, o trabalho concentrou-se no planejamento interno do chassi e na distribuição primária de energia.
* **Mapeamento Elétrico:** Passagem dos cabos de alimentação de alta corrente fornecidos pelo Kit Lion, roteando-os de forma centralizada para protegê-los de arestas metálicas cortantes.
* **Layout Interno:** Ensaios de posição dos componentes na placa superior para otimizar o espaço e preparar o encaixe dos controladores lógicos.

### 📅 Quarta-Feira: Fixação da Eletrônica e Fechamento Estrutural
Consolidação da arquitetura lógica de controle e finalização da blindagem de proteção do robô.
* **Fixação de Controladores:** Posicionamento estratégico e fixação mecânica rígida da unidade de gerenciamento auxiliar (**VXM**) e do controlador de motores (**Titan Quad**) na placa superior, utilizando espaçadores para atenuação de vibrações.
* **Instalação das Chapas de Acrílico:** Dimensionamento, furação e fixação de painéis de acrílico personalizados nas laterais e topo do chassi, atuando como blindagem física contra poeira e detritos externos.

### 📅 Quinta-Feira: Otimização Elétrica e Retenção de Potência
Refinamento do cabeamento interno e segurança do sistema de alimentação móvel.
* **Cable Management:** Organização, alinhamento e agrupamento de toda a fiação elétrica dos motores e placas de controle, eliminando fios soltos e prevenindo acidentes com partes móveis.
* **Fixação da Bateria:** Ajuste no encaixe do suporte da bateria e aplicação de abraçadeiras plásticas de alta resistência para travamento mecânico da célula de energia, impedindo qualquer deslocamento interno.

### 📅 Sexta-Feira: Resolução de Falhas, Inicialização e Teste Dinâmico (O Robô Andou!)
Fase de *troubleshooting* de barramento concluída com sucesso e validação de pista.
* **Correção de Erro de Conexão:** Após análise rigorosa, o erro intermitente de comunicação foi resolvido através do ajuste e sincronização do *Baud Rate* (taxa de transmissão) e mapeamento das portas seriais de comunicação entre o VXM e o Titan Quad.
* **Validação das Soldas:** Testes com multímetro confirmaram a integridade elétrica total do painel de controle recém-soldado.
* **Teste Dinâmico de Tração:** O firmware foi carregado com sucesso, o sistema de controle respondeu perfeitamente e **o robô realizou a sua primeira movimentação prática em pista de testes**, validando a cinemática de 3 motores no chassi triangular.

---

## 📐 Especificações Técnicas do Hardware Utilizado

| Componente / Subsistema | Modelo / Tipo | Função e Descrição Técnica | Status Atual |
| :--- | :--- | :--- | :--- |
| **Kit de Desenvolvimento** | Studica Lion | Ecossistema de peças estruturais, mecânicas e conexões. | **Operacional** |
| **Chassi** | Triangular | Geometria otimizada para manobrabilidade em 3 eixos de tração. | **Operacional** |
| **Atuadores** | 3 Motores DC | Responsáveis pela propulsão e deslocamento dinâmico. | **Operacional** |
| **Controlador Principal** | Titan Quad | Controladora de motores de alta performance e leitura de encoders. | **Operacional** |
| **Co-processador / Interface**| VXM | Módulo auxiliar na placa superior para expansão de portas e sensores. | **Operacional** |
| **Blindagem Externa** | Chapas de Acrílico | Painéis para fechamento, isolamento elétrico e proteção. | **Operacional** |
| **Interface Humana** | Painel de Controle | Módulo de acionamento manual soldado e integrado. | **Operacional** |

---

## 🔌 Layout Final da Placa Superior (Sistemas Ativos)

A organização dos componentes foi estabilizada e todas as comunicações de dados estão ativas:
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
---

## 🚀 Próximas Fases do Projeto
- [ ] Realizar testes de estresse em pista para avaliar a autonomia real da bateria.
- [ ] Desenvolver as primeiras rotinas de movimentação autônoma baseadas em sensores de distância.
- [ ] Implementar curvas PID para suavização de aceleração e frenagem dos motores.
