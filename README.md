# 🛡️ HomeLabSOC

<p align="center">
  <strong>Laboratório de Cybersecurity focado em SOC, SIEM, XDR, EDR, IDS/IPS, Threat Intelligence, Threat Hunting e Resposta a Incidentes.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Foco-Cybersecurity-red?style=for-the-badge">
  <img src="https://img.shields.io/badge/SOC-Laboratório-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Wazuh-SIEM%20%7C%20XDR-purple?style=for-the-badge">
  <img src="https://img.shields.io/badge/Linux-Ambiente-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Windows-Endpoints-blue?style=for-the-badge">
</p>

---

## 📌 Sobre o Projeto

O **HomeLabSOC** é um laboratório pessoal de Cybersecurity desenvolvido para simular um ambiente de **Security Operations Center (SOC)**.

O principal objetivo é construir um ecossistema integrado de segurança onde diferentes tecnologias possam trabalhar em conjunto para:

* 🛡️ Monitoramento de segurança
* 📊 Coleta e análise de logs
* 🔎 Detecção de ameaças
* 🧠 Threat Hunting
* 🚨 Investigação de incidentes
* 🦠 Threat Intelligence
* 🛡️ Detecção e Resposta em Endpoints
* 🌐 Monitoramento e proteção de rede
* 🔄 Resposta a incidentes
* ⚙️ Automação de processos de segurança

O laboratório será desenvolvido de forma incremental, permitindo adicionar novas ferramentas, sistemas operacionais, integrações e cenários de segurança ao longo do projeto.

---

# 🎯 Objetivos

Os principais objetivos do HomeLabSOC são:

* 🛡️ Construir um ambiente de SOC funcional para estudos
* 📊 Centralizar e analisar logs de segurança
* 🔎 Desenvolver e testar regras de detecção
* 🚨 Simular e investigar incidentes de segurança
* 🧠 Praticar Threat Hunting
* 🌐 Monitorar tráfego de rede
* 🦠 Analisar malware e Indicadores de Comprometimento (IOCs)
* 🔗 Integrar diferentes plataformas de segurança
* 🔄 Automatizar processos de resposta a incidentes
* 🧪 Simular técnicas de ataque em ambiente controlado
* 📚 Desenvolver conhecimentos práticos em Cybersecurity
* 🗂️ Documentar investigações, detecções e respostas

---

# 🏗️ Arquitetura do Laboratório

O laboratório será construído de forma incremental, permitindo adicionar novas tecnologias de segurança conforme o projeto evoluir.

```text
                              ┌─────────────────────┐
                              │     INTERNET / WAN  │
                              └──────────┬──────────┘
                                         │
                                         ▼
                              ┌─────────────────────┐
                              │       FIREWALL      │
                              │       / GATEWAY     │
                              └──────────┬──────────┘
                                         │
                        ┌────────────────┴────────────────┐
                        │                                 │
                        ▼                                 ▼
                 ┌──────────────┐                 ┌──────────────┐
                 │   IDS / IPS  │                 │   MONITORA-  │
                 │              │                 │   MENTO DE   │
                 │  Suricata /  │                 │     REDE     │
                 │    Snort     │                 │              │
                 └──────┬───────┘                 └──────────────┘
                        │
                        ▼
              ┌─────────────────────────┐
              │          WAZUH          │
              │                         │
              │       SIEM / XDR        │
              │                         │
              │ Gerenciamento de Logs   │
              │ Detecção de Ameaças     │
              │ FIM                     │
              │ Vulnerabilidades        │
              └────────────┬────────────┘
                           │
             ┌─────────────┼──────────────┐
             │             │              │
             ▼             ▼              ▼
       ┌──────────┐   ┌──────────┐   ┌──────────┐
       │ Windows  │   │  Linux   │   │ Servidores│
       │ Endpoints│   │ Endpoints│   │ Serviços  │
       └──────────┘   └──────────┘   └──────────┘
             │             │
             └─────────────┼─────────────────┐
                           │                 │
                           ▼                 ▼
                    ┌──────────────┐  ┌──────────────┐
                    │     EDR      │  │    Threat    │
                    │              │  │ Intelligence │
                    │Elastic Defend│  │  VirusTotal  │
                    └──────┬───────┘  └──────┬───────┘
                           │                 │
                           └────────┬────────┘
                                    ▼
                           ┌─────────────────┐
                           │     THEHIVE     │
                           │                 │
                           │ Resposta a      │
                           │ Incidentes      │
                           │                 │
                           │ Gerenciamento   │
                           │ de Casos        │
                           └────────┬────────┘
                                    │
                                    ▼
                           ┌─────────────────┐
                           │  INVESTIGAÇÃO   │
                           │   E RESPOSTA    │
                           └─────────────────┘
```

---

# 🧰 Tecnologias do Laboratório

| Tecnologia             | Categoria             | Função                           | Status              |
| ---------------------- | --------------------- | -------------------------------- | ------------------- |
| 🛡️ **Wazuh**           | SIEM / XDR            | Monitoramento e Detecção         | 🟢 Em implementação |
| 🐝 **TheHive**         | Resposta a Incidentes | Gerenciamento de Casos           | 🟡 Planejado        |
| 🌐 **Suricata**        | IDS / IPS             | Detecção de Ameaças de Rede      | 🟡 Planejado        |
| 🌐 **Snort**           | IDS / IPS             | Detecção de Intrusões            | 🟡 Planejado        |
| 🪟 **Windows**         | Endpoint              | Telemetria de Endpoints          | 🟡 Planejado        |
| 🐧 **Linux**           | Endpoint / Servidor   | Telemetria de Sistemas           | 🟡 Planejado        |
| 🦠 **VirusTotal**      | Threat Intelligence   | Enriquecimento de IOCs           | 🟡 Planejado        |
| 🛡️ **Elastic Defend**  | EDR                   | Detecção e Resposta em Endpoints | 🟡 Planejado        |
| 🔥 **Firewall**        | Segurança de Rede     | Segmentação e Controle           | 🟡 Planejado        |
| 🧪 **Atomic Red Team** | Simulação de Ataques  | Testes de Detecção               | 🟡 Planejado        |
| 🎯 **MITRE Caldera**   | Simulação Adversária  | Emulação de Ataques              | 🟡 Planejado        |

### Legenda

```text
🟢 Implementado / Em desenvolvimento
🟡 Planejado
🔵 Em avaliação
🔴 Descontinuado
```

---

# 🛡️ Wazuh

O **Wazuh** será a principal plataforma de monitoramento de segurança do HomeLabSOC.

Ele será responsável pela coleta, análise e correlação de eventos provenientes dos endpoints Windows e Linux.

### Principais recursos explorados

* Gerenciamento de Logs
* Análise de Eventos de Segurança
* File Integrity Monitoring (FIM)
* Detecção de Vulnerabilidades
* Security Configuration Assessment (SCA)
* Detecção de Rootkits
* Detecção de Malware
* Monitoramento de Endpoints
* Detecção de Ameaças
* Active Response
* Monitoramento de conformidade

### Integrações planejadas

```text
Windows
   │
Linux
   │
Servidores
   │
   ▼
 WAZUH
   │
   ├──────────────► TheHive
   │
   ├──────────────► VirusTotal
   │
   ├──────────────► IDS / IPS
   │
   └──────────────► EDR
```

---

# 🐝 TheHive

O **TheHive** será utilizado como plataforma de **Resposta a Incidentes e Gerenciamento de Casos**.

O objetivo é transformar alertas de segurança em investigações estruturadas.

### Fluxo planejado

```text
Evento de Segurança
        │
        ▼
      Wazuh
        │
        ▼
 Detecção / Alerta
        │
        ▼
      TheHive
        │
        ├── Criação de Caso
        ├── Tarefas
        ├── Observáveis
        ├── Investigação
        ├── Evidências
        └── Resposta
```

### Processo de investigação

```text
Alerta
  │
  ▼
Triagem
  │
  ▼
Investigação
  │
  ▼
Threat Intelligence
  │
  ▼
Contenção
  │
  ▼
Erradicação
  │
  ▼
Recuperação
  │
  ▼
Lições Aprendidas
```

---

# 🌐 IDS / IPS

O laboratório contará com uma camada dedicada à **detecção e prevenção de intrusões na rede**.

As principais tecnologias avaliadas serão:

* **Suricata**
* **Snort**

### Objetivos

* Detecção de Intrusões
* Prevenção de Intrusões
* Análise de Pacotes
* Detecção baseada em assinaturas
* Detecção de ameaças de rede
* Identificação de tráfego suspeito
* Detecção de Command & Control
* Detecção de reconhecimento de rede

### Fluxo

```text
Tráfego de Rede
      │
      ▼
   IDS / IPS
      │
      ├── Tráfego Normal
      │
      └── Tráfego Suspeito
              │
              ▼
             Alerta
              │
              ▼
            Wazuh
              │
              ▼
           TheHive
```

---

# 🪟 Máquinas Windows

As máquinas Windows serão utilizadas para representar estações de trabalho e endpoints de um ambiente corporativo.

O objetivo será coletar telemetria dos endpoints e simular diferentes eventos de segurança.

### Telemetria

* Windows Event Logs
* Eventos de Segurança
* PowerShell
* Criação de Processos
* Eventos de Autenticação
* Alterações no Sistema de Arquivos
* Alterações no Registro
* Conexões de Rede
* Tarefas Agendadas
* Serviços
* Atividades de Usuários

### Cenários

```text
Brute Force
     │
     ▼
Acesso a Credenciais
     │
     ▼
Execução de PowerShell
     │
     ▼
Persistência
     │
     ▼
Command & Control
     │
     ▼
Detecção
     │
     ▼
Investigação
     │
     ▼
Resposta
```

---

# 🐧 Máquinas Linux

As máquinas Linux serão utilizadas principalmente para representar servidores e sistemas de infraestrutura.

### Telemetria

* Logs de autenticação
* SSH
* sudo
* Execução de processos
* Integridade de arquivos
* Logs do sistema
* Conexões de rede
* Atividades de usuários
* Indicadores de escalação de privilégios

### Cenários

* Brute Force via SSH
* Login suspeito
* Escalação de privilégios
* Persistência
* Processo malicioso
* Alteração não autorizada de arquivos
* Conexões de rede suspeitas

---

# 🦠 Threat Intelligence — VirusTotal

O **VirusTotal** será utilizado como fonte de Threat Intelligence para enriquecimento de indicadores.

### Indicadores analisados

* Hashes de arquivos
* Endereços IP
* Domínios
* URLs
* Amostras de Malware
* Indicadores de Comprometimento (IOCs)

### Fluxo de investigação

```text
Alerta de Segurança
        │
        ▼
    Indicador
        │
        ▼
    VirusTotal
        │
        ▼
Reputação / Inteligência
        │
        ▼
   Investigação
        │
        ▼
     TheHive
```

---

# 🛡️ Endpoint Detection & Response — EDR

O laboratório também contará com uma solução de **EDR**, inicialmente utilizando o **Elastic Defend**.

O objetivo será estudar como a telemetria de um EDR pode complementar as informações coletadas por um SIEM como o Wazuh.

### Recursos a serem explorados

* Telemetria de Endpoints
* Monitoramento de Processos
* Detecção de Malware
* Monitoramento de Arquivos
* Visibilidade de Rede
* Detecção de Ameaças
* Investigação de Endpoints
* Análise de Segurança

### SIEM + EDR

```text
                ┌──────────────┐
                │    Endpoint  │
                └──────┬───────┘
                       │
             ┌─────────┴─────────┐
             │                   │
             ▼                   ▼
         ┌────────┐        ┌──────────────┐
         │ Wazuh  │        │     EDR      │
         │  SIEM  │        │Elastic Defend│
         └────┬───┘        └──────┬───────┘
              │                   │
              └─────────┬─────────┘
                        ▼
                    Correlação
                        │
                        ▼
                     TheHive
                        │
                        ▼
                   Investigação
                        │
                        ▼
                      Resposta
```

---

# 🔗 Integrações

Uma das principais propostas do HomeLabSOC é estudar como diferentes soluções de segurança podem trabalhar em conjunto.

### Integração principal

```text
                   ┌──────────────┐
                   │   Windows    │
                   └──────┬───────┘
                          │
                   ┌──────▼───────┐
                   │    Linux     │
                   └──────┬───────┘
                          │
                          ▼
                   ┌──────────────┐
                   │    Wazuh     │
                   └──────┬───────┘
                          │
             ┌────────────┼────────────┐
             │            │            │
             ▼            ▼            ▼
        ┌────────┐   ┌──────────┐  ┌──────────┐
        │TheHive │   │VirusTotal│  │   EDR    │
        └────────┘   └──────────┘  └──────────┘
             │
             ▼
       Resposta a Incidentes
```

---

# 🔍 Casos de Uso de Segurança

O laboratório será utilizado para desenvolver e testar diferentes cenários de detecção.

## Detecção em Endpoints

* Brute Force
* PowerShell Suspeito
* Detecção de Malware
* Monitoramento de Integridade de Arquivos
* Escalação de Privilégios
* Persistência
* Execução de Processos Suspeitos
* Criação não autorizada de contas
* Tarefas Agendadas Suspeitas

## Detecção de Rede

* Varredura de Portas
* Reconhecimento de Rede
* Conexões Suspeitas
* Indicadores de Command & Control
* Anomalias de DNS
* Alertas do IDS/IPS
* Tráfego de Rede Suspeito

## Autenticação

* Múltiplas Tentativas de Login
* Login Bem-sucedido após várias falhas
* Autenticação Suspeita
* Brute Force via SSH
* Eventos de Autenticação do Windows
* Atividades de Contas Privilegiadas

## Threat Intelligence

* Reputação de Hash
* Reputação de IP
* Reputação de Domínio
* Reputação de URL
* Enriquecimento de IOCs

---

# 🧪 Simulação de Ataques

O laboratório utilizará simulações controladas de ataques para gerar telemetria e validar as capacidades de detecção.

Possíveis tecnologias:

* **MITRE ATT&CK**
* **Atomic Red Team**
* **MITRE Caldera**
* **Nmap**
* **Metasploit**

Essas ferramentas serão utilizadas para reproduzir comportamentos de adversários em ambiente controlado e avaliar se a infraestrutura consegue detectar, investigar e responder aos eventos.

---

# 🎯 MITRE ATT&CK

O **MITRE ATT&CK** será utilizado como referência para organizar os comportamentos dos adversários e os casos de uso de detecção.

Exemplo do ciclo de ataque:

```text
Reconhecimento
      │
      ▼
Acesso Inicial
      │
      ▼
Execução
      │
      ▼
Persistência
      │
      ▼
Escalação de Privilégios
      │
      ▼
Evasão de Defesas
      │
      ▼
Acesso a Credenciais
      │
      ▼
Descoberta
      │
      ▼
Movimentação Lateral
      │
      ▼
Command & Control
      │
      ▼
Exfiltração
      │
      ▼
Impacto
```

Sempre que possível, as regras de detecção e investigações serão associadas às respectivas técnicas e subtécnicas do MITRE ATT&CK.

---

# 🧠 Threat Hunting

O **Threat Hunting** será utilizado para procurar proativamente comportamentos suspeitos dentro do ambiente.

### Atividades

* Identificação de processos suspeitos
* Análise de conexões de rede incomuns
* Investigação de autenticações anormais
* Análise de atividades do PowerShell
* Identificação de mecanismos de persistência
* Investigação de escalação de privilégios
* Busca por indicadores de Command & Control
* Pesquisa por hashes maliciosos
* Análise de consultas DNS suspeitas
* Investigação de movimentação lateral

### Fluxo

```text
Hipótese
    │
    ▼
Coleta de Dados
    │
    ▼
Pesquisa / Consulta
    │
    ▼
Identificação de Anomalia
    │
    ▼
Investigação
    │
    ▼
Validação do IOC
    │
    ▼
Criação de Detecção
```

---

# 🚨 Resposta a Incidentes

O laboratório será utilizado para simular o ciclo completo de resposta a incidentes.

```text
Preparação
     │
     ▼
Identificação
     │
     ▼
Contenção
     │
     ▼
Erradicação
     │
     ▼
Recuperação
     │
     ▼
Lições Aprendidas
```

O **TheHive** será utilizado para organizar casos, tarefas, evidências, observáveis e etapas das investigações.

---

# 📊 Engenharia de Detecção

O HomeLabSOC também será utilizado para desenvolver, testar e aprimorar regras de detecção.

### Processo

```text
Ameaça / Técnica
        │
        ▼
Hipótese de Detecção
        │
        ▼
Fonte de Telemetria
        │
        ▼
Regra de Detecção
        │
        ▼
Simulação de Ataque
        │
        ▼
Alerta
        │
        ▼
Validação
        │
        ▼
Ajustes
        │
        ▼
Detecção Validada
```

---

# 📁 Estrutura do Projeto

```text
HomeLabSoc/
│
├── README.md
│
├── wazuh/
│   ├── config/
│   ├── docker/
│   └── README.md
│
├── thehive/
│   ├── config/
│   └── README.md
│
├── ids-ips/
│   ├── suricata/
│   ├── snort/
│   └── README.md
│
├── endpoints/
│   ├── windows/
│   └── linux/
│
├── edr/
│   └── elastic-defend/
│
├── threat-intelligence/
│   └── virustotal/
│
├── attack-simulation/
│   ├── atomic-red-team/
│   └── caldera/
│
├── detections/
│   ├── wazuh/
│   ├── sigma/
│   └── mitre-attack/
│
├── investigations/
│   ├── incidents/
│   └── cases/
│
├── playbooks/
│   ├── incident-response/
│   └── automation/
│
└── docs/
    ├── architecture/
    ├── installation/
    ├── configuration/
    ├── detections/
    ├── investigations/
    └── troubleshooting/
```

---

# 🗺️ Roadmap

## Infraestrutura

* [x] Criar laboratório inicial
* [x] Criar repositório no GitHub
* [ ] Definir arquitetura de rede
* [ ] Configurar Firewall
* [ ] Criar rede isolada para segurança

## SIEM / XDR

* [x] Implementar Wazuh
* [ ] Configurar Wazuh Manager
* [ ] Configurar Wazuh Dashboard
* [ ] Instalar agentes Windows
* [ ] Instalar agentes Linux
* [ ] Criar regras de detecção
* [ ] Configurar Active Response

## Segurança de Rede

* [ ] Implementar Suricata
* [ ] Avaliar Snort
* [ ] Integrar IDS/IPS com Wazuh
* [ ] Criar casos de uso de detecção de rede

## Resposta a Incidentes

* [ ] Implementar TheHive
* [ ] Integrar Wazuh com TheHive
* [ ] Criar fluxos de incidentes
* [ ] Criar modelos de investigação
* [ ] Criar playbooks de resposta

## Threat Intelligence

* [ ] Integrar VirusTotal
* [ ] Automatizar enriquecimento de IOCs
* [ ] Criar fluxo de investigação de IOCs

## EDR

* [ ] Implementar Elastic Defend
* [ ] Configurar telemetria de endpoints
* [ ] Comparar telemetria do EDR e Wazuh
* [ ] Criar casos de uso de detecção em endpoints

## Threat Hunting

* [ ] Criar hipóteses de investigação
* [ ] Desenvolver consultas de hunting
* [ ] Mapear detecções para MITRE ATT&CK
* [ ] Documentar investigações

## Simulação de Ataques

* [ ] Implementar Atomic Red Team
* [ ] Avaliar MITRE Caldera
* [ ] Criar cenários de ataque controlados
* [ ] Validar cobertura das detecções

## Automação

* [ ] Automatizar enriquecimento de alertas
* [ ] Automatizar consultas de IOCs
* [ ] Criar playbooks de resposta
* [ ] Automatizar tarefas repetitivas do SOC

---

# 📚 Documentação

Toda a documentação do laboratório será mantida dentro do diretório:

```text
/docs
```

Categorias previstas:

* Arquitetura
* Instalação
* Configuração
* Integrações
* Engenharia de Detecção
* Threat Hunting
* Resposta a Incidentes
* Investigações
* Playbooks
* Simulação de Ataques
* Troubleshooting

---

# 🔐 Segurança e Isolamento

O HomeLabSOC deve funcionar em um ambiente controlado e, preferencialmente, isolado da infraestrutura de produção.

### Boas práticas

* Utilizar redes virtuais dedicadas
* Restringir exposição desnecessária à Internet
* Criar snapshots antes de testes
* Nunca utilizar credenciais reais de produção
* Nunca armazenar senhas no repositório
* Nunca armazenar API Keys no código
* Utilizar `.gitignore` para arquivos sensíveis
* Manter sistemas vulneráveis isolados
* Realizar testes somente em sistemas autorizados

---

# ⚠️ Aviso Legal

Este projeto é destinado **exclusivamente para fins educacionais, pesquisa e testes de segurança autorizados**.

Todas as simulações de ataques, testes de segurança e experimentos realizados no laboratório devem ocorrer somente em sistemas próprios, ambientes controlados ou sistemas para os quais exista autorização explícita.

O autor não se responsabiliza pelo uso indevido das ferramentas, técnicas ou informações disponibilizadas neste projeto.

---

# 🚀 Possíveis Expansões

Conforme o laboratório evoluir, novas tecnologias poderão ser adicionadas:

* **MISP**
* **Cortex**
* **Shuffle**
* **Zeek**
* **Velociraptor**
* **Security Onion**
* **OpenCTI**
* **Grafana**
* **Prometheus**
* Outros EDRs
* Plataformas SOAR
* Ambiente de Malware Analysis
* Honeypots
* Scanners de Vulnerabilidade
* Active Directory
* Windows Domain Controller
* Cenários de Purple Team

---

# 🧩 Visão Geral das Tecnologias

```text
                         HOME LAB SOC
                              │
             ┌────────────────┼────────────────┐
             │                │                │
             ▼                ▼                ▼
            SIEM             EDR             IDS/IPS
           Wazuh       Elastic Defend     Suricata/Snort
             │                │                │
             └────────────────┼────────────────┘
                              │
                              ▼
                     THREAT INTELLIGENCE
                          VirusTotal
                              │
                              ▼
                     INCIDENT RESPONSE
                           TheHive
                              │
                              ▼
                       THREAT HUNTING
                              │
                              ▼
                       MITRE ATT&CK
                              │
                              ▼
                     ATTACK SIMULATION
                  Atomic Red Team / Caldera
```

---

# 👨‍💻 Áreas de Estudo

O HomeLabSOC será utilizado para estudos práticos nas seguintes áreas:

```text
SOC
SIEM
XDR
EDR
IDS / IPS
Threat Intelligence
Threat Hunting
Detection Engineering
Incident Response
Digital Forensics
Malware Analysis
Network Security
Endpoint Security
Security Monitoring
MITRE ATT&CK
Adversary Emulation
Security Automation
```

---

<p align="center">

### 🛡️ Aprender. Detectar. Investigar. Responder.

**HomeLabSOC — Laboratório de Cybersecurity**

</p>
