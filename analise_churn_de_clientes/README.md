# Análise de Churn de Clientes

Este projeto apresenta uma análise completa de **evasão de clientes (churn)**. O objetivo foi identificar **fatores que influenciam o cancelamento de serviços** e propor **estratégias de retenção baseadas em dados**.

O projeto foi estruturado em duas etapas principais:

1. **Análise exploratória de dados (EDA)** para identificar padrões de churn.
2. **Modelagem preditiva com Machine Learning** para avaliar a importância das variáveis.

---

# 1. Introdução

A evasão de clientes representa um dos principais desafios estratégicos para empresas de telecomunicações. A perda de clientes impacta diretamente:

- receita recorrente
- previsibilidade financeira
- custo de aquisição de novos clientes

Como **reter clientes costuma ser mais barato do que adquirir novos**, compreender os fatores associados ao churn é essencial para decisões estratégicas.

Este projeto utiliza **análise estatística e modelos de aprendizado de máquina** para identificar padrões de evasão e gerar insights acionáveis.

---

# 2. Limpeza e Tratamento de Dados

Antes da análise, os dados passaram por um processo de **pré-processamento** para garantir consistência e confiabilidade.

As principais etapas incluíram:

- verificação de **valores ausentes**
- remoção de **inconsistências**
- conversão de **variáveis categóricas**
- correção de **tipos de dados**
- padronização de **nomes de colunas**

Algumas variáveis numéricas que estavam armazenadas como texto foram convertidas para tipos adequados, garantindo maior qualidade nas análises posteriores.

---

# 3. Análise Exploratória de Dados (EDA)

A análise exploratória foi realizada utilizando **visualizações estatísticas**, como:

- histogramas
- boxplots
- comparações entre grupos

Essa etapa permitiu identificar padrões importantes associados ao churn.

---

# 4. Principais Variáveis Analisadas

## 4.1 Variáveis Demográficas

### Gênero
Não foram observadas diferenças relevantes entre homens e mulheres em relação à evasão.

### Clientes idosos
Clientes com mais de 65 anos apresentaram uma **tendência ligeiramente maior de churn**, porém o número reduzido de observações limita conclusões mais robustas.

### Presença de parceiro(a)
Clientes **sem parceiro(a)** apresentam aproximadamente **o dobro de churn** em comparação com clientes que possuem parceiro.

### Dependentes
Clientes **sem dependentes** apresentaram um churn aproximadamente **cinco vezes maior**, indicando um padrão significativo.

---

## 4.2 Serviços Contratados

### Serviço telefônico
Não foram observadas diferenças relevantes.

### Serviço de internet
Clientes que utilizam **fibra óptica** apresentaram **taxa significativamente maior de churn**.

Isso pode indicar:

- problemas de qualidade
- custo elevado
- expectativas não atendidas

### Segurança online, backup e proteção de dispositivos

Clientes que **não possuem esses serviços adicionais** apresentaram maior evasão.

Esses serviços podem aumentar o **valor percebido** pelo cliente.

### Assistência técnica

A ausência de suporte técnico também mostrou associação com maior churn.

### Streaming (TV e filmes)

Foi observada uma **leve tendência de maior churn** entre clientes que não possuem esses serviços.

---

## 4.3 Contratos e Pagamentos

### Tipo de contrato

Clientes com **contrato mensal (Month-to-month)** apresentaram a **maior taxa de churn**.

Isso sugere que a ausência de compromisso de longo prazo facilita o cancelamento.

### Faturamento online

Clientes que utilizam faturamento eletrônico apresentaram uma taxa maior de churn.

### Cheque eletrônico

O método de pagamento **electronic check** mostrou forte associação com evasão.

Esse foi um dos fatores mais críticos observados.

---

## 4.4 Variáveis Numéricas

### Tempo de permanência (Tenure)

Clientes com **menor tempo de permanência** apresentam maior probabilidade de churn.

Esse padrão é comum em serviços baseados em assinatura.

### Gasto mensal

Clientes que cancelaram tendem a apresentar **gastos mensais mais altos**.

### Gasto total

Clientes que evadiram possuem **menor gasto total**, consequência direta do menor tempo de permanência.

---

# 5. Modelagem de Machine Learning

Após a análise exploratória, foram utilizados diferentes algoritmos para modelar o churn:

- Regressão Logística
- K-Nearest Neighbors (KNN)
- Árvore de Decisão
- Floresta Aleatória

O objetivo foi comparar os modelos e identificar **quais variáveis possuem maior poder preditivo**.

---

# 6. Principais Fatores Identificados pelos Modelos

Os fatores mais relevantes encontrados durante o treinamento foram:

- **Tenure (tempo de permanência do cliente)**
- **Uso de internet por fibra óptica**

Esses resultados confirmam os padrões observados na análise exploratória.

Clientes que estão **nos primeiros meses de contrato apresentam maior risco de churn**.

---

# 7. Diferença Entre os Modelos

Durante a modelagem, foi observado um comportamento interessante.

Nos modelos baseados em árvore (**árvore de decisão e random forest**), a variável:

**Tipo de contrato mensal**

apareceu como altamente relevante para prever churn.

Entretanto, no modelo de **regressão logística**, essa variável apresentou:

### P>|Z| > 0.8


Esse valor indica que o coeficiente é **estatisticamente insignificante** dentro desse modelo.

Isso demonstra que **diferentes algoritmos podem interpretar as variáveis de maneiras distintas**, reforçando a importância de comparar múltiplos modelos.

---

# 8. Insights Principais

A análise revelou três fatores principais associados à evasão:

1. **Tempo de permanência baixo (tenure baixo)**
2. **Uso de internet por fibra óptica**
3. **Contratos mensais**

Outros fatores relevantes incluem:

- pagamento por cheque eletrônico
- ausência de serviços adicionais (backup, segurança, suporte)
- clientes sem dependentes

---

# 9. Estratégias de Retenção Baseadas nos Dados

Com base nos resultados obtidos, algumas estratégias podem ser implementadas.

## 9.1 Foco nos primeiros meses de contrato

Clientes novos apresentam maior risco de churn.

Possíveis ações:

- descontos iniciais
- bônus de serviços
- acompanhamento ativo do cliente
- suporte prioritário

---

## 9.2 Incentivo a contratos de longo prazo

Oferecer:

- planos anuais com desconto
- benefícios exclusivos
- pacotes premium

Isso aumenta a previsibilidade da receita e reduz churn.

---

## 9.3 Melhorias no serviço de fibra óptica

É importante investigar:

- estabilidade da conexão
- qualidade do serviço
- suporte técnico

Melhorias nessa área podem aumentar a satisfação dos clientes.

---

## 9.4 Pacotes de serviços combinados

Combinar serviços como:

- internet
- segurança online
- backup
- proteção de dispositivos

Isso aumenta o valor percebido pelo cliente e reduz cancelamentos.

---

# 10. Conclusão

A análise permitiu identificar fatores importantes associados à evasão de clientes em serviços de telecomunicações.

Os resultados indicam que:

- **clientes novos são mais propensos a cancelar**
- **a experiência com fibra óptica é um fator relevante**
- **contratos mensais apresentam maior rotatividade**

Além disso, o uso de diferentes modelos mostrou que **a interpretação das variáveis pode variar dependendo do algoritmo**, destacando a importância da comparação entre métodos.

Estratégias focadas em:

- retenção nos primeiros meses
- melhoria da experiência do cliente
- incentivo a contratos de longo prazo

podem reduzir significativamente a taxa de churn e aumentar o valor do cliente ao longo do tempo.

---

# Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# Instalação

Instale as dependências com:

```bash
pip install -r requirements.txt