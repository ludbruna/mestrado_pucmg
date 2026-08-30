# Impacto da Codificação de Atributos no Desempenho e na Interpretabilidade de Modelos de Aprendizado de Máquina

Este repositório disponibiliza o **material suplementar** e os **códigos-fonte** utilizados no desenvolvimento da dissertação:

**Impacto da Codificação de Atributos no Desempenho e na Interpretabilidade de Modelos de Aprendizado de Máquina**

**Autora:** Ludmila Bruna Santos Nascimento  
**Programa de Pós-Graduação em Informática – PUC Minas**  
**Belo Horizonte, 2026**

---

## Conteúdo do repositório

O repositório contém os seguintes arquivos:

- `Apendice.pdf` — material suplementar da dissertação;
- `1pipelineInicial.py` — caracterização, análise e limpeza inicial das bases de dados;
- `2codBinOrd.py` — codificação dos atributos dicotômicos e ordinais;
- `3pipeline.py` — execução do pipeline experimental.

---

## Material suplementar

O arquivo `Apendice.pdf` reúne análises e visualizações complementares aos resultados apresentados na dissertação.

### Apêndice A — Métricas

- **A.1** Resultados de F1-score por estratégia de codificação e algoritmo nas bases de baixa cardinalidade;
- **A.2** Resultados de F1-score por estratégia de codificação e algoritmo nas bases de alta cardinalidade;
- **A.3** Resultados de Recall por estratégia de codificação e algoritmo nas bases de baixa cardinalidade;
- **A.4** Resultados de Recall por estratégia de codificação e algoritmo nas bases de alta cardinalidade;
- **A.5** Resultados de Precisão por estratégia de codificação e algoritmo nas bases de baixa cardinalidade;
- **A.6** Resultados de Precisão por estratégia de codificação e algoritmo nas bases de alta cardinalidade;
- **A.7** Médias de F1-score nas análises geral e por cardinalidade.

### Apêndice B — Dimensionalidade

- **B.1** Relação entre instâncias e dimensionalidade nas bases de alta cardinalidade;
- **B.2** Resultados da dimensionalidade por estratégia de codificação nas bases de baixa cardinalidade.

### Apêndice C — Custo computacional

- **C.1** Tempo médio de codificação e treinamento nas bases de baixa cardinalidade;
- **C.2** Tempo médio de codificação e treinamento nas bases de alta cardinalidade.

---

## Códigos-fonte

### `1pipelineInicial.py`

Código utilizado nas etapas iniciais de preparação das bases de dados, incluindo:

- caracterização dos atributos;
- identificação de valores ausentes;
- identificação de redundâncias e inconsistências;
- remoção de atributos e instâncias conforme os critérios definidos;
- imputação de valores ausentes;
- geração das bases de dados após a limpeza.

### `2codBinOrd.py`

Código utilizado para a transformação dos atributos dicotômicos e ordinais, conforme os mapeamentos definidos para cada atributo.

### `3pipeline.py`

Código responsável pela execução do pipeline experimental, incluindo:

- divisão estratificada dos dados em treino e teste;
- validação cruzada estratificada com 5 folds no conjunto de treino;
- aplicação das estratégias de codificação;
- treinamento dos modelos de classificação;
- cálculo das métricas de Precisão, Recall e F1-score;
- registro do tempo de codificação e treinamento;
- registro da dimensionalidade após a codificação;
- geração dos mapeamentos das representações;
- armazenamento dos resultados e dos modelos treinados.

O código também gera os valores por dobra utilizados posteriormente nas análises estatísticas.

---

## Estratégias de codificação

Foram consideradas as seguintes estratégias de codificação:

- One-Hot Encoding;
- Dummy Encoding;
- Count Encoding;
- Frequency Encoding;
- Ordinal Encoding;
- Hashing Encoding;
- Binary Encoding;
- Helmert Encoding;
- CatBoost Encoding;
- Leave-One-Out Encoding;
- Target Encoding.

Para o Hashing Encoding, foram avaliadas diferentes configurações de função hash, número de componentes e forma de representação.

---

## Algoritmos de classificação

Os experimentos consideram os seguintes algoritmos:

- Decision Tree;
- Random Forest;
- Multilayer Perceptron;
- Support Vector Machine;
- XGBoost.

---

## Execução

Antes da execução dos códigos, os caminhos de entrada e saída devem ser ajustados de acordo com o ambiente utilizado.

As principais bibliotecas utilizadas incluem:

```bash
pip install numpy pandas scikit-learn category_encoders xgboost joblib matplotlib
