<h1>Filtrando e exibindo colunas de uma planilha utilizando a biblioteca pandas.</h1>

```python

import pandas as pd

#Configurar para exibir todas as linhas e colunas
pd.set_option('display.max_rows', None)
pd.set_option('display.max_columns', None)

#carregando a planilha
planilha = ('historicotaxajurosdiario_TodosCampos.csv')
colunas = pd.read_csv(planilha, delimiter=';')

#Filtrando as colunas que vão aparecer
colunas_exibidas = colunas[['Posicao','InstituicaoFinanceira', 'TaxaJurosAoMes', 'TaxaJurosAoAno']]
print(colunas_exibidas)
