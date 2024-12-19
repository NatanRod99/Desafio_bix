# Previsão de Falhas em Sistemas de Ar de Caminhões

## Descrição

Este projeto tem como objetivo prever falhas em sistemas de ar de caminhões utilizando técnicas de Machine Learning. O modelo prevê se um caminhão terá uma falha no sistema de ar (classe "pos") ou não (classe "neg") com base em dados históricos de sensores e outros atributos.

## Dados

Os dados utilizados neste projeto são provenientes de dois arquivos CSV:

- `air_system_previous_years.csv`: Dados históricos de anos anteriores.
- `air_system_present_year.csv`: Dados do ano atual.

Os dados contêm informações sobre diversos atributos dos caminhões, incluindo leituras de sensores e informações de manutenção. A coluna `class` representa a variável alvo, indicando se houve falha no sistema de ar ou não.

## Metodologia

1. **Preparação dos dados:** Os dados são carregados, combinados, tratados para valores ausentes e escalados.
2. **Treinamento e avaliação dos modelos:** Diversos modelos de Machine Learning são treinados e avaliados, incluindo Árvore de Decisão, Regressão Logística, Random Forest, Gradient Boosting e LightGBM. A métrica principal para avaliação é o ROC AUC.
3. **Seleção do melhor modelo:** O modelo com o melhor desempenho (maior ROC AUC) é selecionado para uso em produção.
4. **Otimização de hiperparâmetros:** Otimização de hiperparâmetros pode ser realizada para melhorar ainda mais o desempenho do modelo selecionado.
5. **Balanceamento de classes:** Se os dados estiverem desbalanceados, técnicas como SMOTE podem ser aplicadas para melhorar o desempenho do modelo.
6. **Colocar o modelo em produção:** O modelo treinado é salvo utilizando a biblioteca `joblib` para ser utilizado em um ambiente de produção.

## Resultados

Os resultados da avaliação dos modelos são apresentados em termos de acurácia, ROC AUC e validação cruzada. O melhor modelo e seus hiperparâmetros (se otimizados) são indicados.

## Próximos Passos

- Explorar outros modelos de Machine Learning.
- Realizar otimização de hiperparâmetros mais extensiva.
- Implementar técnicas de balanceamento de classes se necessário.
- Integrar o modelo em um sistema de monitoramento em tempo real.
