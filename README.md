
# EMQA – Estação de Monitoramento da Qualidade Ambiental

Este repositório contém os materiais relacionados ao projeto **EMQA (Estação de Monitoramento da Qualidade Ambiental)**, desenvolvido como um sistema de **baixo custo** para monitoramento ambiental em tempo real em ambientes urbanos.

O projeto foi desenvolvido no contexto acadêmico e está documentado no artigo científico:

> **EMQA – Estação de Monitoramento da Qualidade Ambiental**  
> Felipe Sledz Ferreira, Gabriel Arriello Santana, Vinicius Romualdo Silva  
> Universidade Tecnológica Federal do Paraná (UTFPR)

---

## Objetivo do Projeto

O objetivo da EMQA é monitorar, em tempo real, indicadores ambientais relevantes para a saúde pública e para a qualidade de vida urbana, incluindo qualidade do ar, poluição sonora e radiação ultravioleta.

A estação foi projetada para ser:
- Financeiramente acessível  
- Modular e escalável  
- Reprodutível  
- Adequada para pesquisas acadêmicas e aplicações educacionais  

---

## Parâmetros Monitorados

A EMQA realiza medições dos seguintes parâmetros ambientais:

- Temperatura (°C)
- Umidade relativa do ar (%)
- Material particulado (PM2.5 e PM10)
- Monóxido de Carbono (CO)
- Dióxido de Carbono (CO₂)
- Dióxido de Nitrogênio (NO₂)
- Ozônio (O₃)
- Compostos Orgânicos Voláteis (VOCs)
- Nível de ruído sonoro (dB)
- Radiação ultravioleta (Índice UV)

Os dados são interpretados com base em índices e referências técnicas reconhecidas, como IQAr, Kaiterra e INPE.

---

## Arquitetura do Sistema

O sistema é composto por três camadas principais:

### Hardware
- Microcontrolador ESP32-S3
- Conjunto de sensores ambientais dedicados
- Sistema de ventilação ativa para circulação de ar
- Gabinete plástico com estrutura mecânica adaptada

### Firmware
- Desenvolvido em C++ utilizando a Arduino IDE
- Leitura periódica dos sensores
- Processamento e normalização dos dados
- Envio das medições via Wi-Fi

### Software
- Back-end desenvolvido em Flask (Python)
- Front-end desenvolvido em Vue.js com PrimeVue
- Visualização de dados em tempo real via navegador
- Armazenamento de histórico em arquivos JSON

---

## Sensores Utilizados

| Sensor | Parâmetro |
|------|----------|
| PMS5003 | PM2.5 e PM10 |
| MiCS-4514 | CO e NO₂ |
| MQ-131 | O₃ |
| SGP30 | CO₂ e VOCs |
| GUVA-S12SD | Radiação UV |
| DHT22 | Temperatura e Umidade |
| MAX9814 | Nível de Ruído |

---

## Validação Experimental

A EMQA foi testada em dois ambientes distintos na cidade de Curitiba (PR):

- Zona residencial (bairro Sítio Cercado)
- Avenida de tráfego intenso (Avenida Marechal Floriano Peixoto)

Os resultados demonstraram boa estabilidade temporal das medições, capacidade de distinguir diferentes cenários urbanos e coerência com dados de referência públicos para diversos parâmetros ambientais. As limitações observadas estão associadas principalmente à calibração de sensores de baixo custo.

---
