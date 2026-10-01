# ML-Classificacao

Projeto simples de **Machine Learning** que tenta adivinhar qual é a **fonte de energia** de uma usina (solar, eólica, hidrelétrica etc.) usando só três informações: a **potência** (em kW), a **latitude** e a **longitude**.

Os dados vêm da ANEEL (agência de energia elétrica do Brasil).

## Como abrir

O código está no notebook [`classificacao_aneel.ipynb`](classificacao_aneel.ipynb). Dá para abrir direto no Google Colab: é só subir o arquivo em [colab.research.google.com](https://colab.research.google.com) (Arquivo → Fazer upload de notebook) e rodar as células em ordem. Os dados são baixados da internet automaticamente.

## O que foi feito

1. **Carreguei os dados** de um arquivo CSV e dei uma olhada neles: se faltava algum valor, que tipos de dado existem, quais são as fontes de energia e quantas usinas há de cada uma.
2. **Escolhi o que o modelo vai usar**: potência, latitude e longitude são as "pistas" (entrada) e a `fonte` é a "resposta" que queremos prever.
3. **Separei os dados em treino e teste**: 80% para o modelo aprender e 20% para testar se aprendeu de verdade. Usei `stratify` para que a proporção de cada fonte fique parecida nas duas partes.
4. **Treinei três modelos** diferentes:
   - Regressão Logística
   - K-Nearest Neighbors (KNN), que olha para os "vizinhos mais parecidos"
   - Random Forest, que junta várias árvores de decisão
5. **Comparei os resultados** com a acurácia (porcentagem de acertos), o relatório de classificação (precisão, recall e f1-score) e a **matriz de confusão**, que mostra onde cada modelo mais errou.
6. **Desenhei as matrizes de confusão** em gráficos lado a lado para ficar fácil de comparar.

## Bibliotecas usadas

`pandas`, `numpy`, `matplotlib`, `seaborn` e `scikit-learn`.


