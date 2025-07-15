![Requerimentos para aquisição de arma de fogo de 2019 e 2025](https://github.com/Antonino-Marques-Jares/aquisicao_armas_de_fogo_deferidas/blob/main/placa_pare.jpg?raw=true)

# Requesições para aquisições de armas de fogo deferidas no Brasil
O gráfico visa entendermos a variação de autorizações (deferimentos) para aquisições de armas de fogo pelo SINARM.
Buscamos criar um histórico que permita observar o total mensal por Estado.

# Visualize o gráfico em:
[Gráficoi](https://www.areadetrampo.com.br/mapa-de-pescadores-no-brasil/)

### Fonte das informações sobre requerimentos para aquisição de armas de fogo no Brasil
[![Gov Br](govbr.webp)](https://dados.gov.br/dados/conjuntos-dados/sinarm)

# O código:

- Passo 1 - Baixar os arquivos REQUERIMENTOS_com_categoria_<ano>.csv (2019 a 2025)
- Passo 2 - Os arquivos csv de 2024 e 2025 precisaram passar por ajustes para extrair as informações.
       + no Nodepad++
       + subistituir  '( {2,};)' por ';'
       + subistituir  ';' por '","'
       + subistituir  '^([0-9]|[A-Z])' por '"$1'
       + subistituir  '([0-9]|[A-Z])\r' por '$1"\r'
- Passo 3 - Soma agrupanda por 'MES','ANO','UF', 'MUNICIPIO', 'DECISAO'
- Passo 4 - Selecionando apenas as decisões deferidas
- Passo 5 - Soma agrupanda por 'MES_ANO','UF' e 'MUNICIPIO'
- Passo 6 - Temos o data frame df_grafico com os seguintes campos MES_ANO,	UF,	QTD
- Passo 7 - criando Json do nosso df_grafico
- Passo 8 - crianso HTML com JSON incorporado
  
# Autor:
**Antonino Marques Jares**

# Atualizado em:
**15/07/2025**

