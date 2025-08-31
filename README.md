# 3D Print Roughness Analysis

## Descrição
Este projeto explora a predição da rugosidade de peças impressas em 3D como um problema de regressão. Foram realizados dois experimentos:

1. **Modelo com features selecionadas**: Inclui apenas parâmetros chave como `layer_height`, `material` e `nozzle_temperature`.
2. **Modelo com todas as features**: Inclui todos os parâmetros de impressão, exceto as variáveis de saída.

O pipeline utilizado inclui **padronização**, **regressão linear** e avaliação do modelo utilizando métricas como **MSE** e **R²**. Além disso, foi feita análise dos resíduos e interpretação do impacto de cada feature na rugosidade final.

## Objetivo
- Avaliar como diferentes parâmetros de impressão 3D afetam a rugosidade das peças.
- Comparar o desempenho de modelos de regressão linear com diferentes conjuntos de features.
- Fornecer insights para otimização do processo de impressão.

## Estrutura do Notebook
1. **Introdução**
2. **Ferramentas e versões**
3. **Análise de dados**
    - Exploração dos dados
    - Limpeza e preparação
4. **Modelagem**
    - Seleção de features
    - Padronização
    - Treinamento e teste dos modelos
5. **Avaliação**
    - Métricas de desempenho
    - Análise de resíduos
6. **Insights e conclusões**

## Tecnologias Utilizadas
- Python 3
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn

## Dataset
O dataset utilizado contém informações sobre impressões 3D, incluindo:
- `layer_height`
- `wall_thickness`
- `infill_density` e `infill_pattern`
- `nozzle_temperature`, `bed_temperature`, `print_speed`
- `material`, `fan_speed`
- Medidas de saída: `roughness`, `tension_strenght`, `elongation`

## Resultados
- O modelo com todas as features apresentou melhor desempenho em termos de R².
- Features como `nozzle_temperature` e `layer_height` mostraram forte influência na rugosidade final.
- Ambos os modelos apresentaram algum grau de **overfitting**, indicando que há espaço para otimização e utilização de modelos mais robustos.

## Como Executar
1. Clone este repositório:
git clone https://github.com/seu-usuario/3D_Print_Roughness_Analysis.git

2. Abra o notebook no Jupyter:
jupyter notebook

3. Execute as células sequencialmente para reproduzir os resultados.
