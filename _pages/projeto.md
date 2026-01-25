---
layout: default
title: "Projeto"
permalink: /projeto/
heroImage: "/assets/img/Hardware_do_Rack_Inteligente.png"
heroAlt: "Diagrama de blocos do hardware"
---

## Resumo

 
 O **Rack Inteligente AIoT** integra sensores, atuadores e um microcontrolador para:
 
 - Monitorar **temperatura** e **umidade**.
 - Detectar **estado de porta** e eventos de segurança.
 - Publicar telemetria e receber comandos via **MQTT**.
 - Exibir dados e controles em um **dashboard**.
 - Apoiar decisões com **IA generativa** e **previsão** (séries temporais).


## Arquitetura (alto nível)

 
- **Firmware (C/C++ com FreeRTOS)**: leitura de sensores, controle de atuadores e comunicação.
- **Camada IoT (MQTT)**: tópicos para telemetria, comandos e ACK.
- **Dashboard (Python)**: monitoramento, histórico e comandos.
- **AIoT**: geração de análises e previsões a partir dos dados.


## Comunicação MQTT (visão geral)

 
 A comunicação utiliza tópicos hierárquicos por rack.
 
 - Base: `racks` (configurável)
 - Identificação: `<rack_id>`
