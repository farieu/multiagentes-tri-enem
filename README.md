# Multiagentes TRI-ENEM

Este repositório reúne os códigos, notebooks e artefatos desenvolvidos no contexto de um estudo sobre a simulação de respostas educacionais utilizando a Teoria de Resposta ao Item aliada a arquiteturas baseadas em agentes e Large Language Models.

O projeto tem como objetivo investigar a geração de padrões de resposta sintéticos e sua aderência a modelos psicométricos, com foco em avaliações de larga escala como o ENEM.

---

## Estrutura do Repositório

### 📁 data/

Contém os dados utilizados no projeto, organizados em duas etapas do pipeline:

#### raw/
Dados brutos, sem tratamento inicial:
- `ITENS_PROVA_2020.csv` a `ITENS_PROVA_2023.csv`: Microdados originais das provas do ENEM.
- `questoes_enem_2020_lc.json` a `questoes_enem_2023_lc.json`: Questões estruturadas por área (Linguagens e Códigos).

#### processed/
Dados tratados e prontos para uso nos experimentos:
- `batches_estudantes.json`: Perfis sintéticos de estudantes organizados em lotes.
- `enem2020_lc.json` a `enem2023_lc.json`: Questões processadas e estruturadas.
- `itens_enem_2020_azul.csv` a `itens_enem_2023_azul.csv`: Itens calibrados e filtrados por caderno.

---

### 📁 notebooks/

Contém os notebooks principais do pipeline experimental:

- `01 [PIBIC] Extração API + Caderno INEP.ipynb`  
  **Objetivo:** Realizar a coleta e estruturação inicial dos dados das provas do ENEM.

- `02 [PIBIC] Estatísticas 50x20.ipynb`  
  **Objetivo:** Gerar distribuições estatísticas de estudantes e parâmetros de simulação.

- `03 [PIBIC] Geração de Habilidades.ipynb`  
  **Objetivo:** Simular níveis de habilidade (θ) dos estudantes sintéticos.

- `04 [PIBIC] Plot 1000 estudantes.ipynb`  
  **Objetivo:** Visualizar distribuições e comportamento das habilidades simuladas.

- `05 [PIBIC] Saída do n8n.ipynb`  
  **Objetivo:** Processar e analisar as respostas geradas por agentes/LLMs no fluxo automatizado.

---

### 📁 outputs/

Armazena os resultados e artefatos gerados durante os experimentos:

#### results/

- `experimento 6.1/` e `experimento 6.2/`: Resultados de execuções experimentais específicas.
- `Curva Característica do Item.png`: Representação da curva logística da TRI.
- `Curva Características dos Itens no Modelo.png`: Comparação entre itens.
- `Habilidades 1000 (20x50).png`: Distribuição simulada de habilidades.
- `Habilidades 1000.png`: Visualização geral das habilidades.

---

## Pipeline Experimental

O fluxo do projeto segue as seguintes etapas:

1. **Coleta e processamento de dados**
   - Extração dos dados do ENEM
   - Estruturação e limpeza

2. **Modelagem estatística**
   - Definição de distribuições
   - Geração de perfis sintéticos de estudantes

3. **Simulação de habilidades**
   - Atribuição de níveis de proficiência (θ)

4. **Geração de respostas**
   - Execução de fluxos automatizados com agentes/LLMs

5. **Análise dos resultados**
   - Avaliação da aderência ao modelo TRI
   - Visualização das curvas características dos itens

---

## Observações

- Todos os notebooks foram desenvolvidos e executados no ambiente Visual Studio Code.
- O projeto está estruturado para permitir reprodutibilidade dos experimentos.
- Parte do fluxo de geração de respostas integra ferramentas de automação (como n8n) para orquestração de agentes.

---

## Contribuição

Este repositório faz parte de um projeto acadêmico no contexto de iniciação científica (PIBIC), com foco em aplicações de Inteligência Artificial e Arquiteturas Multiagentes.

---