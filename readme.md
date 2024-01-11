# Series temporais - Prophet
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