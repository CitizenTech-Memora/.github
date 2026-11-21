<div align="center">

<img src="logo.svg" alt="Logo do Memora: duas mãos segurando as três doses do dia" width="110" />

# Memora

**Cuidar de quem cuida.**

Caixa de remédios conectada para idosos com Alzheimer e suas famílias.

[![Pitch no YouTube](https://img.shields.io/badge/YouTube-Assistir%20Pitch-red?style=for-the-badge&logo=youtube&logoColor=white)](https://youtu.be/DyYcnP_5acY)
[![Painel do Cuidador](https://img.shields.io/badge/Painel-Acessar-2f5d50?style=for-the-badge&logo=vercel&logoColor=white)](https://memora-painel.vercel.app)
[![Simulação no Wokwi](https://img.shields.io/badge/Wokwi-Ver%20a%20caixa-4a5e9a?style=for-the-badge&logo=arduino&logoColor=white)](https://wokwi.com/projects/480810351690378241)

![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-0F172A?style=flat-square&logo=tailwindcss&logoColor=38BDF8)

<sub>Global Solution 2026.2 · CitizenTech · FIAP · Engenharia de Software</sub>

</div>

---

## O problema

Para quem tem Alzheimer, o remédio traz duas dúvidas todos os dias: *"já está na hora?"* e *"será que eu já tomei?"*. Esquecer a dose atrapalha o tratamento, e tomar duas vezes pode ser perigoso. Enquanto isso, a família, muitas vezes longe, fica sem saber o que aconteceu.

## A solução

O **Memora** troca essa dúvida por informação. Na hora de cada dose, a caixa libera **só o compartimento certo** e toca um lembrete com a voz gravada da família. Um sensor percebe quando o remédio sai da caixa. Se ninguém retira a dose, ou se alguém tenta abrir outro compartimento fora de hora, o cuidador recebe um aviso. A caixa também vigia a temperatura onde os remédios ficam guardados e funciona mesmo sem internet.

O objetivo é simples: que a pessoa idosa tome o remédio certo, na hora certa, com mais autonomia, e que a família só precise agir quando algo realmente sair do lugar.

```mermaid
flowchart LR
    A["<b>Caixa</b><br/>lembra e protege<br/>na hora da dose"] --> B["<b>Registros</b><br/>retirada, atraso,<br/>fora de hora e calor"]
    B --> C["<b>Família</b><br/>acompanha pelo painel<br/>e recebe os avisos"]

    classDef caixa fill:#eaf2ef,stroke:#2f5d50,stroke-width:2px,color:#1e2a2b
    classDef registro fill:#fdf3dc,stroke:#e2b23f,stroke-width:2px,color:#1e2a2b
    classDef familia fill:#e8eff7,stroke:#4a5e9a,stroke-width:2px,color:#1e2a2b
    class A caixa
    class B registro
    class C familia
```

---

## As partes do projeto

| Repositório | O que é | Tecnologias | Disciplina |
|---|---|---|---|
| [**caixa**](https://github.com/CitizenTech-Memora/caixa) | A caixa de remédios inteligente, simulada no Wokwi: libera o compartimento certo, lembra, confirma a retirada e mede a temperatura | ESP32 · C++ · Wokwi | Edge Computing & Computer Systems |
| [**central-do-cuidador**](https://github.com/CitizenTech-Memora/central-do-cuidador) | Central em terminal para cadastrar remédios, registrar cada retirada e ver o resumo da semana | Python · JSON | Computational Thinking with Python |
| [**modelagem-matematica**](https://github.com/CitizenTech-Memora/modelagem-matematica) | Modelo que mostra como atrasar, esquecer ou dobrar uma dose muda a concentração do remédio no corpo | Python · NumPy · Matplotlib | Differentiated Problem Solving |
| [**painel-web**](https://github.com/CitizenTech-Memora/painel-web) | Painel do Cuidador: status das doses do dia, alertas, rede de cuidado, lembrete de voz e adesão semanal | React · Tailwind CSS · MockAPI | Web Development e Front-end Design |

### As regras que todas as partes seguem

| Regra | Valor |
|---|---|
| Compartimentos | 🟡 manhã · 🟠 tarde · 🔵 noite |
| Lembrete | 10 min depois do horário |
| Dose no horário | Retirada em até 20 min |
| Temperatura máxima | 30 °C (o valor certo depende da bula) |
| Indicador de impacto | **Taxa de adesão:** % de doses retiradas no horário, por semana |

---

## Objetivos de Desenvolvimento Sustentável

- **ODS 3 · Saúde e bem-estar** (principal): apoiar a adesão ao tratamento de pessoas idosas com Alzheimer.
- **ODS 10 · Redução das desigualdades** (secundário): mais autonomia para a pessoa idosa e menos sobrecarga para quem cuida.

> **Importante:** o Memora é um **apoio ao cuidado** e não substitui o cuidador, o médico ou o farmacêutico. O sistema registra a *retirada* do remédio, não confirma que ele foi ingerido. Pessoas, telefones, remédios e horários do projeto são **fictícios**.

---

## Equipe

| Nome | RM |
|------|----|
| Eric Kang | 572575 |
| Guilherme Tomé Nogueira | 570144 |
| Lucas de Andrade Astorini | 569119 |
| Sabrina Lopes da Silva | 571870 |
| Sofia Satomi Hagio | 569120 |
