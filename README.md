
# Análise de Personalidade com Machine Learning

Este projeto visa analisar e prever tipos de personalidade usando técnicas de machine learning. O foco é em classificar perfis de personalidade com base em dados de entrada variados, utilizando algoritmos avançados e técnicas de balanceamento de classes.

## Objetivos do Projeto

- Classificar tipos de personalidade com base em características demográficas e pontuações de traços.
- Avaliar a eficácia de diferentes algoritmos de machine learning.
- Lidar com problemas de desequilíbrio de classes utilizando técnicas como Borderline-SMOTE.
- Fornecer insights acionáveis sobre a distribuição de tipos de personalidade.

## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- AutoViz

## 2. Entendimento dos Dados

O dataset utilizado contém informações que exploram a relação entre dimensões de personalidade e fatores como idade, gênero, educação e interesses. As variáveis principais são:

| Variável              | Descrição                                                |
|-----------------------|----------------------------------------------------------|
| Idade                 | Variável contínua que representa a idade do indivíduo.   |
| Gênero                | Variável categórica ('Masculino', 'Feminino').            |
| Educação              | Variável binária (1 = Pós-graduação ou superior, 0 = Graduação ou inferior). |
| Interesse             | Principal área de interesse do indivíduo (categórica).   |
| Pontuação de Introversão | Variável contínua (0 a 10) indicando introversão/extroversão. |
| Pontuação de Sensing   | Variável contínua (0 a 10) indicando sensoriamento/intuição. |
| Pontuação de Pensamento | Variável contínua (0 a 10) indicando pensar/sentir.      |
| Pontuação de Julgamento | Variável contínua (0 a 10) indicando julgar/perceber.    |
| Personalidade         | Tipo de personalidade MBTI (variável alvo).               |

Exemplo das primeiras linhas do dataset:

```python
import pandas as pd

df = pd.read_csv('data.csv')
display(df.head())
````

| Age | Gender | Education | Introversion Score | Sensing Score | Thinking Score | Judging Score | Interest   | Personality |
| --- | ------ | --------- | ------------------ | ------------- | -------------- | ------------- | ---------- | ----------- |
| 19  | Male   | 0         | 9.47               | 7.14          | 6.03           | 4.36          | Unknown    | ENFP        |
| 27  | Female | 0         | 5.85               | 6.16          | 0.80           | 4.22          | Sports     | ESFP        |
| 21  | Female | 0         | 7.08               | 3.38          | 2.66           | 5.12          | Unknown    | ENFP        |
| 28  | Male   | 0         | 2.01               | 4.82          | 7.30           | 5.98          | Others     | INTP        |
| 36  | Female | 1         | 9.91               | 4.75          | 5.31           | 4.67          | Technology | ENFP        |

---
## Resultados

- **Acurácia do modelo:** 90.68%
- **Relatório de Classificação:** O relatório inclui precisão, recall e f1-score para cada classe.
- **Matriz de Confusão:** Uma visualização da performance do modelo em cada classe.
  
## 3. Previsões

Abaixo estão exemplos das previsões feitas pelo modelo, associadas ao gênero dos indivíduos (1 = masculino, 0 = feminino):

| Índice | Previsões | Gênero |
| ------ | --------- | ------ |
| 33507  | INFP      | 1      |
| 16990  | ESFJ      | 0      |
| 91298  | INFP      | 0      |
| 66353  | INFP      | 1      |
| 2271   | ENFP      | 0      |
| ...    | ...       | ...    |

### Visualização dos resultados

<img width="1258" height="627" alt="Captura de tela 2025-07-20 111028" src="https://github.com/user-attachments/assets/dc8b04a2-28d8-47af-87f7-99ca0fe65234" />

---

## 4. Análise e Insights

### Distribuição dos tipos de personalidade previstos

| Tipo de Personalidade | Ocorrências |
| --------------------- | ----------- |
| INFP                  | 5           |
| ENFP                  | 3           |
| ENFJ                  | 3           |
| ESTJ                  | 3           |
| ESFJ                  | 2           |
| INTJ                  | 1           |
| ESTP                  | 1           |
| ESFP                  | 1           |

### Distribuição por Gênero

* **Homens (1):**

  * Tipos mais comuns: INFP (2), ENFJ (2), ENFP (2), ESTJ (2)
  * Outros: ESTP (1)

* **Mulheres (0):**

  * Tipos mais comuns: INFP (3), ESFJ (2)
  * Outros: ENFP (1), INTJ (1), ESFP (1), ESTJ (1)

### Insights importantes

* O tipo INFP é o mais frequente, predominando entre as mulheres, sugerindo maior presença de características introvertidas e idealistas.
* Homens apresentam maior incidência de personalidades extrovertidas e associadas à liderança, como ENFJ, ENFP e ESTJ.
* Mulheres apresentam maior diversidade, com tipos mais introvertidos e sensíveis, além de algumas personalidades extrovertidas e analíticas.
* Entre os homens, a extroversão e tomada de decisão lógica são mais marcantes, enquanto nas mulheres há maior presença de empatia e cooperação.

---

## 5. Conclusão Geral

O modelo demonstrou boa capacidade de previsão dos tipos de personalidade, com resultados que evidenciam tendências de personalidade relacionadas a gênero. Essas informações podem ser úteis para entender melhor padrões comportamentais em diferentes grupos.

---

## 6. Como contribuir

Se você quiser mais detalhes do projeto, acesse o dataset completo ou abra uma issue para sugerir melhorias, correções ou discussões.

