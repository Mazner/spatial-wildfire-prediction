# Predição de Incêndios Florestais no Centro-Oeste do Brasil utilizando Aprendizado de Máquina

Este repositório contém o código, experimentos e documentação utilizados no Trabalho de Conclusão de Curso da Universidade Tecnológica Federal do Paraná (UTFPR), cujo objetivo é desenvolver um modelo de previsão de incêndios florestais a partir da integração de dados climáticos, socioeconômicos e geoespaciais.

O projeto é motivado pelo aumento recorrente das queimadas na região Centro-Oeste do Brasil, que apresenta forte dependência agropecuária, condições sazonais críticas e histórico significativo de focos.

---

## Objetivos do Projeto

- Analisar correlações entre variáveis climáticas, socioambientais e ocorrência de incêndios.
- Integrar diferentes bases de dados espaciais e temporais.
- Enriquecer o dataset principal com estatísticas trimestrais provenientes de estações meteorológicas.
- Tratar ausência de municípios no dataset Firewatch de forma estatística.
- Filtrar municípios dentro de um recorte geográfico específico definido por polígono.
- Treinar modelos clássicos de classificação supervisionada para prever a ocorrência de incêndios.
- Comparar métricas de desempenho entre diferentes algoritmos.

---

## Conjuntos de Dados Utilizados

### Firewatch
- Registros históricos de focos de calor.
- Coordenadas geográficas.
- Data e hora da ocorrência.
- Indicadores de risco e Fire Radiative Power (FRP).

### Dados Climáticos
Obtidos por subestações meteorológicas:
- Precipitação média.
- Temperatura.
- Umidade relativa.
- Número de dias consecutivos sem chuva.

### Dados Municipais
- Informações geográficas.
- População.
- PIB agropecuário.

---

## Processamentos Realizados

- Seleção de subestações contidas dentro de polígono geoespacial.
- Interpolação de dados climáticos faltantes.
- Cálculo de médias trimestrais associadas a cada município.
- Enriquecimento da base Firewatch com atributos climáticos agregados.
- Seleção de registros por época crítica do ano.
- Identificação de municípios negativos (sem focos).
- Expansão amostral quando a quantidade de negativos era insuficiente.
- Normalização e padronização.
- Limpeza e padronização de variáveis geográficas.

---

## Engenharia de Atributos

As principais variáveis produzidas incluem:
- Precipitação média trimestral.
- Acúmulo de dias secos.
- Umidade média do período.
- Densidade histórica de ocorrências.
- Indicadores sazonais.
- Dados socioeconômicos agregados.

---

## Análise Exploratória

A análise exploratória avaliou:
- Distribuição temporal dos incêndios.
- Sazonalidade trimestral.
- Correlação entre precipitação e focos.
- Concentração geoespacial da ocorrência.
- Impacto da estiagem prolongada.

Visualizações incluíram mapas, séries temporais, histogramas e matrizes de correlação.

---

## Modelos Treinados

Foram treinados e comparados:

- Support Vector Machine (SVM)
- k-Nearest Neighbors (k-NN)
- Decision Tree Classifier
- Multi-Layer Perceptron (MLP)
A acurácia obtida no conjunto de teste foi aproximadamente 0.83.

---

## Métricas Avaliadas

- Acurácia
- Precisão
- Recall
- F1-score
- Matriz de confusão
- Área sob a curva ROC (ROC-AUC)

---

## Recorte Geográfico

O estudo foi concentrado na região Centro-Oeste do Brasil devido a:
- elevada incidência anual de incêndios florestais,
- importância econômica na produção agropecuária,
- condições climáticas sazonais intensas.

A seleção dos municípios foi feita através de interseção geoespacial com polígono definido.

---

## Estudo sobre Extração de Dados Tabulares de PDF

Foi conduzida uma avaliação com as seguintes ferramentas:
- Camelot (stream, lattice, hybrid, network)
- Tabula-py
- Docling
- Tesseract OCR
- EasyOCR
- pdfminer

Foram analisados diferentes formatos, ruídos visuais e variações de layout.

---

## Arquivos Gerados

- `substations_attributes.csv`
- Dados interpolados e agregados por trimestre
- Relatórios comparativos de desempenho
- Recortes geoespaciais de municípios

---

## Possíveis Trabalhos Futuros

- Uso de imagens multi-espectrais (Sentinel, Landsat).
- Aplicação de redes neurais convolucionais (CNN).
- Modelagem temporal com LSTM ou Transformers.
- Ampliação da cobertura geográfica.
- Inclusão de dados de vegetação (NDVI) e seca (SPI).

---

## Conclusão

Os resultados demonstraram que características climáticas e sazonais são variáveis relevantes para predição de incêndios. Modelos clássicos de classificação alcançam desempenho satisfatório quando combinados com enriquecimento geoespacial e agregação temporal. A região Centro-Oeste apresenta padrões previsíveis em relação à estiagem e intensidade de focos.

---

## Autor

**Marcos Rampaso Bezner**  
Bacharelado em Ciência da Computação — UTFPR  
Foco em Ciência de Dados e Aprendizado de Máquina
