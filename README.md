# Exercícios e nálises de Área Queimada com Sensoriamento Remoto

Projeto com exercícios práticos para **mapeamento e análise de cicatrizes de queimadas** utilizando imagens de satélite, índices espectrais e técnicas de **Machine Learning**.

---

# 🧪 POC 1 — Mapeamento inicial de área queimada

Etapas do processamento:

1. Definição da **Área de Interesse (AOI)**
2. Busca de imagens via **STAC**
3. Leitura de imagens do satélite **Sentinel-2**
4. Composição RGB utilizando bandas:
   - B12
   - B09
   - B04
5. Plot das imagens geradas
6. Aplicação de **índices espectrais**
   - NDVI
   - NBR
   - NBRSWIR
7. Cálculo da diferença dos índices
7. Mapeamento da **área queimada**
8. Conversão da área queimada para:
   - máscara raster
   - vetor
9. Comparação com dados de focos do **BDQueimadas**

---

# 🚀 Desafio 02 — Generalização da metodologia

Objetivo: tornar o código mais reutilizável e expandir os produtos gerados.

### Tarefas

- Criar **funções reutilizáveis**
- Replicar a lógica da POC para gerar **novos produtos de cicatriz de queimadas**
- Utilizar **outros índices espectrais**
- Aplicar **limiares específicos para cada índice**

---

# 📊 Análise Exploratória dos Dados

Exploração estatística dos índices espectrais.

### Atividades

- Analisar diferenças registradas em cada **índice espectral**
- Extrair estatísticas relevantes:
  - Mediana
  - Desvio padrão
  - Primeiro quartil
- Visualização com:
  - **Boxplots**
  - **Histogramas**
- Definir **limiar de classificação de queimadas** baseado nos dados analisados

---

# 🗺️ Aprendizado 01 — Extração de dados no QGIS

Uso do QGIS para geração de amostras.

### Passos

- Criar **pontos e polígonos**
- Utilizar essas geometrias para **extrair valores de imagens `.tif`**
- Gerar um **DataFrame com os dados extraídos**

---

# 🤖 Machine Learning

## 🔹 Aprendizado supervisionado

1. Criar base de dados de treinamento (`train_data`)
2. Treinar modelo **Random Forest**
3. Definir hiperparâmetros ideais usando **Grid Search**
4. Avaliar modelo com dados de teste (`test_data`)
5. Executar modelo em dois cenários:
   - Todos os índices confirmam queimadas
   - Pelo menos **2 de 3 índices** confirmam
6. Extrair estatísticas da previsão

---

## 🔹 Aprendizado não supervisionado

Utilização de **K-Means** para agrupamento.

### Etapas

- Importação do modelo
- Agrupamento em **2 clusters** usando `test_data` para comparativo com o modelo supervisionado
- Combinação dos índices em uma única imagem:
  - cada índice em uma banda
- Clusterização dos **pixels da imagem** em vários clusters
  - identificação de diferentes intensidades dentro da área queimada

---

# 📚 Tecnologias Utilizadas

- Python
- Jupyter Notebook
- Sentinel-2
- STAC
- QGIS
- Machine Learning (Random Forest, K-Means)

---