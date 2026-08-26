Trabalho 1 - Experimento Completo de Base
# Entrega de Trabalho: Implementação de Regressão Linear via Gradiente Descendente

## Descrição
O objetivo deste trabalho é implementar o algoritmo de regressão linear utilizando o método dos mínimos quadrados, programado em **Python**, **R** ou **Julia**.

Você deverá:
- Entregar um **arquivo PDF** gerado a partir de um **Jupyter Notebook**.
- O notebook deve conter a **implementação própria** do algoritmo (sem utilizar bibliotecas de machine learning para o ajuste do modelo).
- O relatório deve ser elaborado com o uso de **markdown** para descrever:
  - O funcionamento do algoritmo.
  - A análise crítica dos resultados obtidos.

## Especificações Técnicas

### Implementação
- Desenvolver uma classe chamada `RTrainer`, que deve possuir:
  - Um método `fit()` para realizar o treinamento.
  - Um método `predict()` para realizar previsões.
- O método `fit()` deve retornar:
  - Um vetor de parâmetros, ou
  - Um objeto `Model`, contendo ao menos uma propriedade que indique o **número de parâmetros** do modelo.
- A implementação deve ser generalizada para **qualquer quantidade de atributos**.

### Algoritmo de Treinamento
- O treinamento do modelo deve ser realizado utilizando o **Gradiente Descendente**.

---

## Sobre os Experimentos

### Testes
- **Testes Unitários**: validar individualmente métodos como `fit()`, `predict()`, funções de erro, entre outros.
- **Testes Funcionais**: validar o pipeline completo de treinamento e predição com conjuntos de dados simples.

### Datasets
- **Toy Dataset**:
  - Criar um pequeno conjunto de dados artificial com cerca de **4 exemplos** e **1 atributo**.
  - O objetivo é validar se o algoritmo encontra uma solução correta com erro na ordem de **10⁻³**.
  - Exemplo: y=2x.

- **Dataset Real**:
  - Utilizar um dataset público voltado para **regressão** disponível no **UCI Machine Learning Repository** ou no **Kaggle**.

### Procedimento Experimental
1. **Divisão dos Dados**:
   - Separar o dataset em três conjuntos: **treinamento**, **desenvolvimento** e **teste**.

2. **Calibração da Taxa de Aprendizado**:
   - Utilizar o conjunto de **desenvolvimento** para encontrar a melhor taxa de aprendizado (**learning rate**).
   - Após encontrar o melhor valor, **retreinar** o modelo utilizando o conjunto de **treinamento + desenvolvimento**, e avaliar no conjunto de **teste**.

3. **Análises Obrigatórias**:
   - **Curva de Treinamento**:
     - Gerar um gráfico que mostre a evolução da função de erro durante o treinamento.
     - Realizar uma análise textual sobre o comportamento da curva de erro.

   - **Análise dos Parâmetros**:
     - Criar um gráfico de barras exibindo os coeficientes encontrados.
     - Analisar em texto quais parâmetros são mais relevantes positiva e negativamente para a predição.

   - **Avaliação Quantitativa**:
     - Calcular e reportar as métricas:
       - **MAE** (Mean Absolute Error)
       - **MSE** (Mean Squared Error)
       - **MAPE** (Mean Absolute Percentage Error)
     - As métricas devem ser implementadas em **módulos** ou **classes próprias**.
     - Comparar os erros de **treinamento+desenvolvimento** e **teste**.
     - Analisar se há **overfitting** ou **underfitting**, justificando os resultados.

   - **Análise de Tempo de Treinamento**:
     - Medir o tempo total de treinamento.
     - Comentar sobre o desempenho temporal observado.

4. **Vídeo de Apresentação**:
   - Gravar um vídeo (pode ser privado no YouTube) explicando:
     - O notebook.
     - As decisões de implementação.
     - As análises realizadas.
   - Incluir o link para o vídeo no final do relatório.

---

## Resumo da Entrega
- PDF ou HTML gerado do notebook contendo:
  - Implementação.
  - Explicações em markdown.
  - Gráficos e análises.
- Código-fonte completo (Jupyter Notebook).
- Link para o vídeo de apresentação no YouTube.

---

# Avaliação do Trabalho

A nota final será composta a partir dos seguintes critérios:

## Critérios de Avaliação

### a) Qualidade de Escrita do Relatório
- Clareza e objetividade na descrição dos métodos e resultados.
- Uso correto da linguagem técnica e acadêmica.
- Organização lógica das seções e subseções no notebook.

### b) Estética do Notebook
- Apresentação visual agradável e organizada:
  - Uso adequado de markdown, títulos, subtítulos e formatação.
  - Inclusão e formatação adequada de gráficos e tabelas.
- Separação clara entre código, resultados e análises.

### c) Explicação no Vídeo
- Coerência e clareza na apresentação oral do trabalho.
- Explicação correta dos principais pontos:
  - Funcionamento do algoritmo.
  - Procedimentos experimentais.
  - Interpretação dos resultados.
- Qualidade mínima de áudio e vídeo (não será avaliada a edição, apenas a clareza da comunicação).

### d) Corretude Técnica
- Implementação correta dos métodos exigidos (`fit()`, `predict()`, métricas próprias).
- Respeito às restrições (não utilizar bibliotecas externas para ajuste do modelo e métricas).
- Algoritmo funcional para qualquer número de atributos.

### e) Qualidade das Análises
- Análises interpretativas bem fundamentadas:
  - Discussão crítica dos resultados obtidos.
  - Identificação correta de fenômenos como overfitting ou underfitting.
  - Justificativas técnicas para as observações feitas nos gráficos e métricas.

---

## Considerações Finais
Trabalhos que demonstrarem inovação na organização, aprofundamento nas análises ou experimentos adicionais relevantes poderão receber bonificação extra.
