# Mini Projeto - Análise Exploratória de Dados de Varejo

## Objetivo

Este projeto tem como objetivo realizar uma análise exploratória de uma base de dados de varejo utilizando Python e a biblioteca Pandas.
Durante a análise, foram realizadas etapas de inspeção, identificação e tratamento de problemas de qualidade dos dados, análise estatística e agrupamentos, buscando compreender melhor as características e os padrões presentes na base.

## Tecnologias utilizadas

- Python
- Pandas
- Google Colab
- Git e GitHub

## Base de dados

A base utilizada contém informações relacionadas a compras realizadas no varejo, incluindo dados dos clientes, produtos, categorias e identificadores das compras.
Cada registro representa um item associado a uma compra. Por esse motivo, o identificador `CO_ID` pode aparecer em mais de uma linha quando uma mesma compra possui diferentes produtos.

## Etapas do projeto

### 1. Importação e inspeção dos dados
A base de dados foi carregada utilizando a biblioteca Pandas. Inicialmente, foram verificadas a quantidade de registros e colunas, os nomes das variáveis e seus respectivos tipos de dados.

### 2. Verificação da qualidade dos dados
Foram analisados valores nulos, registros duplicados e inconsistências nas categorias dos produtos. Nessa etapa, foram identificadas colunas completamente vazias, registros duplicados e valores `#N/D` na coluna de categoria.

### 3. Limpeza e tratamento
As colunas vazias foram removidas, os registros completamente duplicados foram excluídos e os valores `#N/D` foram tratados como `Sem Categoria`. A coluna de data também foi convertida para o tipo `datetime`.

### 4. Estatística descritiva
Foram calculadas medidas estatísticas relacionadas ao número de filhos dos clientes, incluindo média, mediana, moda, desvio padrão, valores mínimo e máximo, contagem e quartis.

### 5. Validação das compras
Foi analisado o identificador `CO_ID`, verificando que sua repetição não representa necessariamente uma duplicidade, pois cada linha corresponde a um item e uma mesma compra pode possuir vários produtos.

### 6. Agrupamentos e análise
Foram realizados agrupamentos para analisar a quantidade de compras por gênero, a quantidade de itens por categoria e a relação entre o número de clientes e compras de cada gênero.

## Principais insights

## Qualidade dos dados e ETL

## ETL e qualidade dos dados

O processo realizado neste projeto pode ser relacionado às etapas de ETL (Extract, Transform e Load). A extração ocorreu com a importação da base CSV para o Pandas. A transformação envolveu a identificação e o tratamento de problemas como registros duplicados, colunas vazias, categorias inconsistentes e tipos de dados inadequados. Por fim, a base tratada foi exportada para um novo arquivo CSV, representando a etapa de carga dos dados transformados.
A qualidade dos dados é importante para garantir análises mais confiáveis. Problemas como duplicidades, valores ausentes ou categorias inconsistentes podem alterar os resultados e levar a interpretações incorretas. Por isso, a inspeção e o tratamento dos dados devem ocorrer antes das análises estatísticas e dos agrupamentos.

## Principais insights

- A categoria **ALIMENTOS** apresentou a maior quantidade de itens, com 384.197 registros.
- Foram identificadas **18.471 compras únicas** na base analisada.
- O gênero feminino apresentou maior quantidade total de compras, com 9.615, em comparação a 8.856 do gênero masculino.
- Apesar da diferença no total de compras, a média por cliente foi muito semelhante entre os gêneros: aproximadamente 18,53 para o feminino e 18,41 para o masculino.
- Em relação ao número de filhos, a média foi de aproximadamente 1,14 por cliente, enquanto a mediana e a moda foram iguais a 0.
- A análise de qualidade identificou registros duplicados, colunas vazias e categorias sem identificação, demonstrando a importância da etapa de limpeza antes da análise dos dados.

## Como executar o projeto

1. Faça o download ou clone este repositório.
2. Abra o notebook no Google Colab.
3. Adicione o arquivo `Base Varejo.csv` ao ambiente do Colab.
4. Execute as células do notebook em ordem.
5. Ao final da execução, será gerado o arquivo `df_limpo.csv` contendo a base tratada.

### Requisitos

- Python 3
- Pandas

## Autora

Bruna Hariadni

**Turma:** Análise de Dados T6
