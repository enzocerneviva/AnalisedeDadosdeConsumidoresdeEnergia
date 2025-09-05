# Checkpoint 01 - Análise de Dados de Consumidores de Energia

### ***Responsável pelo Projeto***
- Enzo Cerneviva | Rm: 563480
---

### INSTRUÇÕES DA ENTREGA:  
- A atividade pode ser desenvolvida em grupo.
- Apenas um integrante submete a atividade.
- Enviar apenas o link do repositório.

---

## Dataset de Consumo de Energia Elétrica Residencial

Este dataset contém **medições do consumo de energia elétrica em uma residência**, registradas a cada **um minuto**, durante quase **4 anos de monitoramento**. Além do consumo global, também estão disponíveis diversas grandezas elétricas e valores de submedição.
  
  

### 📊 Características do Conjunto de Dados

- **Tipo**: Multivariada, Séries Temporais  
- **Área de estudo**: Física e Química  
- **Tarefas associadas**: Regressão, Agrupamento  
- **Tipo de recurso**: Real  

---

### 📂 Estrutura

- **Número de instâncias (linhas)**: `2.075.259`  
- **Número de características (colunas)**: `9`  

---

### ℹ️ Informações do Conjunto de Dados

As medições foram coletadas em uma residência localizada em **Sceaux (7 km de Paris, França)**, entre **dezembro de 2006 e novembro de 2010 (47 meses)**.

### Observações Importantes:
1. `(global_active_power*1000/60 - sub_metering_1 - sub_metering_2 - sub_metering_3)`  
   representa a **energia ativa consumida a cada minuto (Wh)** por equipamentos não medidos nas submedições 1, 2 e 3.  

2. O dataset contém **valores ausentes (~1,25%)**.  
   - Todos os registros de data/hora estão presentes.  
   - Para alguns instantes, os valores de medição estão vazios.  
   - Valores ausentes são representados por **dois separadores consecutivos (`;`)**.  
   - Exemplo: registros do dia **28/04/2007** apresentam dados faltantes.  

---

### ❓ Valores Faltantes

- **Sim**, aproximadamente **1,25%** das linhas possuem valores ausentes.  

---

## Dataset Appliances Energy Prediction (Parte 3)

Este dataset contém **medições do consumo de energia elétrica em uma residência**, registradas a cada **10 minutos**, durante cerca de **4,5 meses**. Além do consumo total de eletrodomésticos, foram coletadas **variáveis ambientais internas e externas** (temperatura e umidade) e variáveis aleatórias para teste de modelos.

### 📊 Características do Conjunto de Dados
- **Tipo**: Multivariada, Séries Temporais  
- **Área de estudo**: Física, Engenharia Elétrica, Ciência de Dados  
- **Tarefas associadas**: Regressão, Classificação, Agrupamento, PCA  
- **Tipo de recurso**: Real  

### 📂 Estrutura
- **Número de instâncias (linhas)**: `5.921`  
- **Número de características (colunas)**: `29`  

### ℹ️ Informações do Conjunto de Dados
As medições foram coletadas em uma residência na **Bélgica**, utilizando uma **rede de sensores sem fio ZigBee** para monitorar temperatura e umidade em diferentes cômodos da casa. O clima externo foi obtido da **estação meteorológica do Aeroporto de Chievres**, Bélgica.

#### Variáveis do dataset:
| Variável | Descrição |
|----------|-----------|
| `date` | Data e hora do registro (YYYY-MM-DD HH:MM:SS) |
| `Appliances` | Consumo de energia de eletrodomésticos (Wh) |
| `lights` | Consumo de energia das lâmpadas (Wh) |
| `T1`–`T9` | Temperatura em diferentes cômodos internos (°C) |
| `RH_1`–`RH_9` | Umidade relativa em diferentes cômodos internos (%) |
| `T_out` | Temperatura externa (°C) |
| `RH_out` | Umidade externa (%) |
| `Press_mm_hg` | Pressão externa (mm Hg) |
| `Windspeed` | Velocidade do vento (m/s) |
| `Visibility` | Visibilidade (km) |
| `Tdewpoint` | Temperatura do ponto de orvalho (°C) |
| `rv1`, `rv2` | Variáveis aleatórias, para teste de modelos |

### Observações Importantes:
1. Os dados internos foram calculados a partir de registros de 3,3 minutos, agregados para intervalos de 10 minutos.
2. O consumo de eletrodomésticos (`Appliances`) reflete o total de energia utilizada em Wh.
3. O dataset contém **valores contínuos**, sem dados ausentes significativos.

### ❓ Valores Faltantes
- **Não**, todos os registros possuem dados completos após agregação e limpeza.

---

### Tarefas Desenvolvidas com os Datasets

- **Pre-Processamento de Dados**: Limpeza, transformação de datas e agregação.
- **Distribuição do consumo**: Análise de consumo baixo, médio e alto (minuto a minuto e média diária).
- **Correlação**: Verificação da relação entre consumo e variáveis ambientais.
- **Normalização**: Aplicação de Min-Max Scaling.
- **PCA**: Redução para 2 componentes principais e análise de agrupamentos naturais.
- **Regressão Linear Múltipla**: Modelagem do consumo com variáveis ambientais.
- **Random Forest Regressor**: Comparação com regressão linear e avaliação do RMSE.
- **K-Means Clustering**: Identificação de perfis de consumo em intervalos de 1 minuto e 10 minutos.
- **Classificação Binária**: Separação de alto vs baixo consumo usando mediana.
- **Avaliação de Classificação**: Matrizes de confusão e métricas de desempenho (accuracy, precision, recall, F1-score).
