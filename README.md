# Exercicios sobre area queimada

## POC 1
- Definição de uma área de interesse
- Busca das imagens utilizando o stac
- Leitura de imagem de satélite (sentinel-2)
- Composição das bandas rgb (b12/b09/b04)
- Plot das imagens geradas
- Aplicação de indices espectrais (NDVI,NBR e NBRSWIR)
- Calculo da área queimada
- Converter a área queimada em máscara e vetor
- Comparação do vetor de área queimada com os dados de focos do bdqueimadas


## Desafio 02
- Criar funções reutilizaveis para otimizar o código
- Replicar a lógica do primeiro exercício para gerar outros produtos de cicatriz de queimadas
- Utilizar os outros índices espectrais apresentados
- Aplicar limiares específicos para cada índice


## Análise Exploratória de dados
- Explorar os dados obtidos a partir da diferença registrada em cada índice espectral
- Extrair dados relevantes, como: Mediana, desvio padrão e primeiro quartil das amostras
- Representação dos resultados obtidos em Bloxplots e Histogramas
- Extrair um limiar para ser utilizado na classificação da queimada com base nos dados obtidos


## Aprendizado 01
- Aprender a utilizar as funções do Qgis para criar pontos e polígonos
- Utilizar estes pontos e polígonos para extrair dados da imagem .tif
- Produzir um dataframe com os dados obtidos da extração