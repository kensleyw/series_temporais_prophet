# Previsão de Valor com Componentes Sazonais

Este é um script Python para prever valores utilizando a biblioteca Prophet do Facebook, considerando componentes sazonais, como estações do ano.

## Series temporais - Prophet
```Prophet``` segue o modelo da API ```sklearn```. Foi criado uma instância da classe Prophet e então é chamado seus métodos ```fit``` e ```predict```.

A entrada para o Prophet é sempre um dataframe com duas colunas: **ds** e **y**. A coluna "ds" (datetime) deve ter o formato esperado pelo Pandas, idealmente **AAAA-MM-DD** para uma data ou **AAAA-MM-DD HH:MM:SS** para data/hora. A coluna "y" deve ser **numérica** e representa a medida que desejamos prever.

**Exemplo:**
```
+------------+---------+
|     ds     |    y    |
+------------+---------+
| 2024-01-05 | 9500.00 |
| 2024-01-06 | 5489.13 |
| 2024-01-07 | 9627.32 |
| 2024-01-08 | 7631.20 |
| 2024-01-09 | 6891.00 |
| 2024-01-10 | 8312.00 |
+------------+---------+
```
Para saber mais acesse o link https://facebook.github.io/prophet/docs/quick_start.html



## Instalação

Certifique-se de ter as bibliotecas necessárias instaladas antes de executar o script. Você pode instalar as dependências usando o seguinte comando:

```bash
pip install pandas prophet matplotlib plotly
```

## Como Usar
1. Clone este repositório:

```bash
git clone https://github.com/seu_usuario/seu_repositorio.git
```

2. Execute o script Python:
```bash
jupyter notebook analise.ipynb
```

## Conteúdo do Notebook
O notebook realiza as seguintes etapas:

1. Carrega um conjunto de dados de exemplo contendo registros de valores ao longo do tempo.
2. Adiciona uma nova feature ao conjunto de dados representando as estações do ano.
3. Cria um modelo Prophet e adiciona a nova feature como um regressor.
4. Treina o modelo com o conjunto de dados.
5. Gera previsões futuras para 12 meses.
6. Plota o gráfico de previsão, incluindo a tendência prevista, valores reais e componentes sazonais.

## Observação
Este notebook utiliza a biblioteca Prophet, que é sensível à sazonalidade e pode produzir melhores resultados em conjuntos de dados com padrões temporais distintos.