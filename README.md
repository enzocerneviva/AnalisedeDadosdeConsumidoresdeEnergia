# Checkpoint 01 - Análise de Dados de Consumidores de Energia  

### INSTRUÇÕES DA ENTREGA:  
- A atividade pode ser desenvolvida em grupo.
- Apenas um integrante submete o arquivo.
- Enviar apenas o link do repositório.

### Dataset de Consumo de Energia Elétrica Residencial

Este dataset contém **medições do consumo de energia elétrica em uma residência**, registradas a cada **um minuto**, durante quase **4 anos de monitoramento**. Além do consumo global, também estão disponíveis diversas grandezas elétricas e valores de submedição.

---

## 📊 Características do Conjunto de Dados

- **Tipo**: Multivariada, Séries Temporais  
- **Área de estudo**: Física e Química  
- **Tarefas associadas**: Regressão, Agrupamento  
- **Tipo de recurso**: Real  

---

## 📂 Estrutura

- **Número de instâncias (linhas)**: `2.075.259`  
- **Número de características (colunas)**: `9`  

---

## ℹ️ Informações do Conjunto de Dados

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

## ❓ Valores Faltantes

- **Sim**, aproximadamente **1,25%** das linhas possuem valores ausentes.  

---

## 📌 Uso Sugerido

Este dataset pode ser utilizado para:  
- Modelos de **previsão de consumo energético**.  
- **Análise de séries temporais**.  
- Detecção de anomalias em padrões de consumo.  
- Estudos de eficiência energética e submedições.  

---
