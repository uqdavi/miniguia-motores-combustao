# 🔧 Miniguia de Estudos — Motores a Combustão Automotivos

> **Projeto desenvolvido como parte do Desafio de Projeto da DIO**  
> Ferramenta utilizada: [NotebookLM](https://notebooklm.google.com/) (Google)  
> Autor: [Davi Silva]

---

## 📌 Contexto e Objetivos

### Contexto

Este caderno temático foi criado com o auxílio do **NotebookLM** como ferramenta de aprendizagem sobre motores de combustão interna utilizados em veículos automotivos.

O tema envolve engenharia mecânica, termodinâmica aplicada e sistemas automotivos.

### Objetivos de Estudo

- Consolidar o conhecimento técnico sobre os **três principais ciclos de combustão interna**: Otto, Diesel e Wankel
- Revisar o funcionamento interno dos motores, desde os **componentes mecânicos** até os **processos termodinâmicos** dentro dos cilindros
- Criar um material de referência rápida para consulta futura
- Explorar o **NotebookLM** como ferramenta de síntese e geração de perguntas a partir de fontes técnicas

---

## 📚 Fontes

As fontes abaixo foram selecionadas por serem abertas, técnicas e confiáveis. Todas foram carregadas no NotebookLM para análise.

| # | Título | Tipo | Link |
|---|--------|------|------|
| 1 | *Internal Combustion Engine Fundamentals* — Heywood (capítulos abertos via MIT OpenCourseWare) | PDF/Web | [MIT OCW — IC Engines](https://ocw.mit.edu/courses/2-615j-advanced-thermodynamics-for-engineers-fall-2005/) |
| 2 | *How Car Engines Work* — HowStuffWorks | Web (texto) | [howstuffworks.com/engine.htm](https://auto.howstuffworks.com/engine.htm) |
| 3 | *The Wankel Rotary Engine: A History* — SAE Technical Papers (aberto) | PDF | [sae.org — buscar "Wankel engine open access"](https://www.sae.org) |
| 4 | *Diesel Engine Technology* — Bosch Automotive Handbook (trechos abertos) | PDF | [bosch-mobility.com](https://www.bosch-mobility.com/en/solutions/publications/automotive-handbook/) |
| 5 | *Thermodynamic Cycles for IC Engines* — Engineering Toolbox | Web (texto) | [engineeringtoolbox.com](https://www.engineeringtoolbox.com/thermodynamic-cycle-d_403.html) |

> ⚠️ **Nota:** Alguns links levam a portais onde a busca pelo material específico é necessária. O NotebookLM aceita uploads diretos de PDF e URLs de páginas abertas.

---

## 🧪 Engenharia de Prompts e Cicatrizes

Esta seção documenta as perguntas estratégicas elaboradas no NotebookLM, variações testadas e as dificuldades encontradas (troubleshooting).

---

### 🔵 Bloco 1 — Motor Otto

**Prompt inicial:**
> "Explique o ciclo Otto de quatro tempos detalhando o que ocorre fisicamente e termodinamicamente em cada tempo."

**Resultado:** Resposta clara e bem referenciada. A IA citou corretamente as fontes carregadas.

**Variação testada:**
> "Qual é a diferença entre a eficiência teórica do ciclo Otto ideal e a eficiência real de um motor a gasolina? Quais são os principais fatores de perda?"

**Resultado:** Resposta mais rica, citou detonação (knocking), perdas por atrito e arrefecimento.

**⚡ Cicatriz (dificuldade):** Ao perguntar sobre "avanço de ignição", a IA misturou informações de fontes distintas sem deixar claro qual afirmava o quê. Solução: reformulei como *"Com base apenas na fonte X, explique o avanço de ignição"* — a resposta ficou mais precisa.

---

### 🟠 Bloco 2 — Motor Diesel

**Prompt inicial:**
> "Descreva o ciclo Diesel e compare-o com o ciclo Otto em termos de razão de compressão, ignição e eficiência térmica."

**Resultado:** Excelente comparação tabular gerada pela IA.

**Variação testada:**
> "Por que motores Diesel têm torque mais alto a baixas rotações em comparação a motores Otto de mesma cilindrada?"

**Resultado:** A IA relacionou corretamente a maior razão ar/combustível, injeção direta e taxa de compressão.

**⚡ Cicatriz:** A IA inicialmente confundiu *injeção direta* (common rail) com *injeção indireta* (pré-câmara). Foi necessário pedir que ela distinguisse as gerações de sistema de injeção Diesel explicitamente.

---

### 🔴 Bloco 3 — Motor Wankel (Rotativo)

**Prompt inicial:**
> "Como funciona o motor Wankel? Descreva o movimento do rotor triangular e as fases de admissão, compressão, expansão e escape."

**Resultado:** Boa explicação geométrica, porém sem diagramas (limitação do NotebookLM).

**Variação testada:**
> "Quais são as vantagens e desvantagens do motor Wankel em comparação com motores de pistão reciprocante, especialmente em termos de consumo e emissões?"

**Resultado:** Resposta equilibrada, destacou alta potência por peso, vibração reduzida, mas consumo elevado e vedação dos ápices como pontos críticos.

**⚡ Cicatriz:** O NotebookLM não encontrou referências suficientes sobre o Wankel nas fontes carregadas inicialmente (as fontes focavam em motores de pistão). Solução: adicionei a fonte 3 (SAE sobre Wankel) e refiz as perguntas — a qualidade das respostas melhorou consideravelmente. **Lição: a qualidade das respostas depende diretamente da qualidade e abrangência das fontes.**

---

### 🧩 Prompts Comparativos (multi-tema)

**Prompt:**
> "Crie uma tabela comparativa entre os motores Otto, Diesel e Wankel cobrindo: princípio de ignição, taxa de compressão típica, eficiência térmica, aplicações comuns e principais desvantagens."

**Resultado:** Tabela bem estruturada e corretamente referenciada. Uma das melhores respostas obtidas.

---

## 📖 Miniguia de Estudo — Entrega Final

---

### 1. Resumos Estruturados

#### ⚙️ Motor Otto (Ciclo a Gasolina/Etanol)

O **ciclo Otto** é um ciclo termodinâmico de quatro tempos baseado em ignição por centelha (vela de ignição). A mistura ar-combustível é comprimida e, no ponto de máxima compressão, a faísca provoca a combustão.

**Os quatro tempos:**
1. **Admissão** — o pistão desce com a válvula de admissão aberta, aspirando a mistura ar-combustível
2. **Compressão** — ambas as válvulas fechadas; o pistão sobe comprimindo a mistura (taxa de compressão: 8:1 a 12:1)
3. **Expansão (potência)** — a vela deflagra a mistura; a explosão empurra o pistão para baixo gerando trabalho útil
4. **Escape** — o pistão sobe novamente com a válvula de escape aberta, expelindo os gases queimados

**Eficiência térmica teórica (ciclo ideal):** η = 1 − (1/r^(γ−1)), onde *r* é a taxa de compressão e *γ* é o índice adiabático (~1,4 para ar). Eficiência prática: 25–35%.

---

#### ⚙️ Motor Diesel (Ciclo Diesel)

O **ciclo Diesel** opera por **ignição por compressão**: o ar é comprimido a uma taxa muito alta (14:1 a 25:1), elevando sua temperatura acima do ponto de ignição do combustível. O diesel é injetado diretamente no cilindro, onde se inflama espontaneamente.

**Diferenças-chave em relação ao Otto:**
- Sem vela de ignição; sem carburador/injeção de mistura prévia
- Maior taxa de compressão → maior eficiência térmica (35–45%)
- Combustão a pressão mais constante (ciclo misto na prática)
- Maior torque a baixas rotações por conta da maior expansão dos gases

**Sistemas de injeção modernos:** Common Rail (injeção direta de alta pressão), que permite múltiplas injeções por ciclo melhorando combustão e emissões.

---

#### ⚙️ Motor Wankel (Rotativo)

O **motor Wankel** substitui o mecanismo pistão-biela-virabrequim por um **rotor triangular excêntrico** que gira dentro de uma câmara epitrocóide. Cada face do rotor executa um ciclo completo de admissão → compressão → expansão → escape conforme gira.

**Vantagens:**
- Ausência de válvulas (portas nas paredes da câmara)
- Altíssima relação potência/peso e potência/volume
- Funcionamento extremamente suave (sem movimento alternado)
- Poucas peças móveis

**Desvantagens:**
- Vedação dos ápices do rotor (problema histórico de durabilidade)
- Consumo de combustível mais alto que motores de pistão equivalentes
- Emissões elevadas de HC (hidrocarbonetos não queimados)
- Uso limitado modernamente (Mazda RX-8 foi o último carro de produção em série, até 2012; Mazda retomou o Wankel como gerador no MX-30 em 2023)

---

### 2. Glossário de Conceitos-Chave

| Termo | Definição |
|-------|-----------|
| **PMI (Ponto Morto Inferior)** | Posição mais baixa do pistão no cilindro |
| **PMS (Ponto Morto Superior)** | Posição mais alta do pistão no cilindro |
| **Taxa de Compressão** | Relação entre volume total do cilindro e volume da câmara de combustão (ex: 10:1) |
| **Ciclo Termodinâmico** | Sequência de processos termodinâmicos que retornam o fluido de trabalho ao estado inicial |
| **Ignição por Centelha** | Ignição da mistura por faísca elétrica (motor Otto) |
| **Ignição por Compressão** | Ignição espontânea pelo calor gerado na compressão (motor Diesel) |
| **Torque** | Força rotacional gerada pelo motor (N·m); indica capacidade de tração |
| **Potência** | Taxa de trabalho realizado (kW ou cv); depende de torque × rotação |
| **Detonação (Knocking)** | Ignição espontânea não controlada da mistura no motor Otto, causando danos |
| **Common Rail** | Sistema de injeção Diesel de alta pressão com trilho comum a todos os injetores |
| **Câmara Epitrocóide** | Formato geométrico interno do motor Wankel que permite o movimento do rotor |
| **Rotor Wankel** | Peça triangular excêntrica que substitui o pistão no motor rotativo |
| **Ápices do Rotor** | Vértices do triângulo do rotor Wankel; críticos para vedação da câmara |
| **Eficiência Térmica** | Percentual da energia do combustível convertida em trabalho mecânico útil |
| **Ciclo de 4 Tempos** | Admissão, compressão, expansão e escape em dois giros do virabrequim |
| **Virabrequim** | Eixo que converte o movimento linear do pistão em movimento rotativo |
| **Biela** | Peça que conecta o pistão ao virabrequim |
| **Comando de Válvulas (CamShaft)** | Eixo com cames que controla a abertura/fechamento das válvulas |
| **Injeção Direta** | Injeção de combustível diretamente no cilindro (GDI em Otto; Common Rail em Diesel) |
| **Turbocompressor** | Dispositivo movido pelos gases de escape que comprime o ar admitido, aumentando a potência |

---

### 3. Prompts Reutilizáveis para Revisão Futura

Use estes prompts no NotebookLM (ou qualquer IA) para revisões futuras sobre o tema:

```
1. "Explique o [ciclo Otto / ciclo Diesel / motor Wankel] como se eu fosse um
   estudante de engenharia no segundo ano."

2. "Crie 10 perguntas de revisão de nível avançado sobre [tema] com gabarito."

3. "Quais são os principais problemas de engenharia no projeto de [componente]
   e como a engenharia moderna os resolve?"

4. "Compare os três ciclos de combustão interna (Otto, Diesel, Wankel) em uma
   tabela cobrindo: ignição, compressão, eficiência, torque e aplicações."

5. "Dado que a eficiência de Carnot é o limite teórico, por que motores reais
   ficam muito abaixo desse valor? Liste os fatores de perda por categoria."

6. "Trace a evolução histórica da tecnologia de injeção de combustível no
   motor Diesel, desde o sistema mecânico até o Common Rail eletrônico."

7. "Explique por que o motor Wankel foi abandonado pela maioria dos fabricantes
   e por que a Mazda o está reintroduzindo como range extender elétrico."

8. "Descreva o impacto da taxa de compressão na eficiência e nas emissões de
   motores Otto e Diesel."

9. "Quais modificações de engenharia permitem que um motor Otto funcione com
   etanol, gasolina ou flex (qualquer proporção)?"

10. "Resuma as principais normas de emissões (Euro 6, Proconve) e como elas
    influenciaram o design dos motores modernos a combustão."
```

---

## 🛠️ Ferramentas Utilizadas

- **[NotebookLM](https://notebooklm.google.com/)** — curadoria de fontes e geração de respostas fundamentadas
- **GitHub** — versionamento e portfólio
- **Markdown** — formatação do caderno

---

## 📎 Estrutura do Repositório

```
miniguia-motores-combustao/
│
├── README.md          ← Este arquivo (caderno temático completo)
└── fontes/            ← PDFs das fontes carregadas no NotebookLM
```

---

*Projeto desenvolvido para o Desafio de Projeto — DIO | Explorando o NotebookLM como Ferramenta de Aprendizagem Ativa*
