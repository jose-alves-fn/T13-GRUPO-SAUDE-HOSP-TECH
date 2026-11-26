# Segmentação de perfis de pacientes com diabetes — Diabetes 130-US Hospitals

## Introdução

A base Diabetes 130-US Hospitals for Years 1999–2008, disponibilizada pelo UCI Machine Learning Repository, reúne **101.766 registros de atendimentos hospitalares**, referentes a 71.518 pacientes, em 130 hospitais dos Estados Unidos, entre 1999 e 2008. Os registros apresentam informações demográficas, clínicas e administrativas, incluindo diagnósticos, procedimentos realizados, medicamentos prescritos, duração da internação e ocorrência de reinternação.

Apesar da diversidade de informações disponíveis, os registros não apresentam uma classificação prévia dos pacientes segundo seus perfis clínicos e assistenciais. Isso abre espaço para investigar se existem grupos com características semelhantes, identificáveis a partir dos padrões presentes nos dados.

O objetivo deste projeto é desenvolver uma estratégia de **segmentação de perfis utilizando técnicas de aprendizado não supervisionado**, buscando identificar agrupamentos que representem diferentes características e padrões de utilização dos serviços hospitalares por pessoas com diabetes. A questão central é: **quais perfis podem ser identificados a partir das características demográficas, clínicas e assistenciais dos registros, e o que distingue esses grupos?**

O trabalho envolverá etapas de compreensão e preparação dos dados, análise exploratória, aplicação e avaliação de algoritmos de agrupamento e interpretação dos segmentos encontrados. Como produto final, os resultados serão disponibilizados em uma aplicação desenvolvida com Streamlit, permitindo visualizar e explorar os grupos identificados e suas principais características.

## Dados do projeto

A base utilizada é a **Diabetes 130-US Hospitals for Years 1999–2008**, disponibilizada pelo **UCI Machine Learning Repository**. O conjunto reúne 101.766 registros de atendimentos hospitalares, correspondentes a 71.518 pacientes distintos, realizados em 130 hospitais dos Estados Unidos entre 1999 e 2008. São 50 variáveis que descrevem características demográficas, informações clínicas, diagnósticos, procedimentos, medicamentos e aspectos administrativos dos atendimentos.

A diversidade de atributos permite investigar diferentes dimensões do cuidado hospitalar relacionado ao diabetes, tornando a base adequada à aplicação de técnicas de **aprendizado não supervisionado**, com o propósito de identificar padrões e agrupar registros com características semelhantes.

!!! tip "Por que esta base, e não outra"
    A base foi originalmente utilizada em pesquisas sobre a qualidade do atendimento hospitalar a pacientes com diabetes e a ocorrência de reinternações. Este projeto propõe uma abordagem complementar: em vez de partir de uma variável-alvo para prever um resultado, busca identificar agrupamentos que emergem das características dos dados. Assim, o foco deixa de ser exclusivamente a previsão de reinternação e passa a ser a descoberta de perfis e padrões entre os pacientes atendidos.

<span style="color:red">**Há um detalhe importante na estrutura dessa base: temos 101.766 atendimentos, mas apenas 71.518 pacientes distintos.**

Isso significa que precisamos decidir qual será a unidade de segmentação:

- Segmentar atendimentos: cada linha representa uma internação. Um mesmo paciente pode aparecer em grupos diferentes.

- Segmentar pacientes: consolidamos os registros de cada pessoa para construir um perfil individual. Cada paciente aparece uma única vez.**</span>

### Levantamento inicial

!!! info "Tipo do projeto"
    - [ ] Análise exploratória
    - [ ] Modelo preditivo
    - [ ] Modelo de classificação
    - [x] Modelo de agrupamento
    - [ ] Detecção de anomalias

### Nível de acesso

!!! warning "Confidencialidade"
    - [x] Público
    - [ ] Interno (toda a organização)
    - [ ] Restrito (apenas a área requisitante)

### Objetivos de negócio

!!! quote ""
    <span style="color:red">**Necessário decidir qual a abordagem, se por atendimento ou se por paciente**</span>

## Sobre o projeto

### Histórico do documento

| Data       | Versão | Descrição                   | Autor         |
| :--------- | :----- | :-------------------------- | :------------ |
| 26/11/2026 | 1.0    | Versão inicial do documento | José Alves |

### Dados do solicitante

``` mermaid
flowchart TD
    id1[Área de negócio] --o id2[Setor requisitante]
```

| Nome                      | Cargo / Função | E-mail            |
| :------------------------ | :------------- | :---------------- |
| Especialista de negócio 1 | Função 1       | email@exemplo.com |
| Especialista de negócio 2 | Função 2       | email@exemplo.com |

### Dados da equipe técnica

| Nome               | Cargo / Função        | E-mail            |
| :----------------- | :-------------------- | :---------------- |
| José Alves Fereira Neto (2650748) | Analista de Negócios  | josealvesfn@gmail.com |
| Membro da equipe 2 | Engenheiro de Dados   | email@exemplo.com |
| Membro da equipe 3 | Cientista de Dados    | email@exemplo.com |
