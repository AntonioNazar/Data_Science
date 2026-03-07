### Instale as dependências com: pip install -r requirements.txt

# Relatório final das análise de churn

## 1. Introdução

Este relatório apresenta os resultados da análise de evasão de clientes (churn) utilizando diferentes modelos de aprendizado de máquina. O objetivo foi identificar os fatores mais relevantes que influenciam a saída de clientes e, a partir desses resultados, propor estratégias de retenção baseadas nos padrões encontrados nos dados.

Foram utilizados diferentes modelos para análise e comparação de desempenho, incluindo regressão logística, KNN, árvore de decisão e floresta aleatória. A interpretação dos resultados foi feita com base na importância das variáveis e nos coeficientes obtidos durante o treinamento.

---

## 2. Principais Fatores que Influenciam a Evasão

Como resultados finais, observamos que os **coeficientes (features) mais importantes dentro do treinamento foram**:

- **Tenure (tempo de permanência do cliente)**  
- **Uso de internet por fibra óptica**

Esses resultados eram esperados, pois análises exploratórias anteriores já indicavam que clientes com **baixo tempo de permanência** apresentam maior probabilidade de evasão. Isso sugere que o período inicial da relação entre cliente e empresa é crítico para a retenção.

Além disso, o **uso de fibra óptica** também apareceu como uma variável importante, indicando que a qualidade ou a percepção do serviço de internet pode influenciar diretamente na decisão do cliente de permanecer ou cancelar o serviço.

---

## 3. Comparação Entre os Modelos

Durante o processo de modelagem, foram avaliados diferentes algoritmos para compreender melhor o comportamento das variáveis.

Os modelos baseados em árvore, como **árvore de decisão** e **floresta aleatória**, indicaram que a variável:

- **Tipo de contrato mensal (Month-to-month)**

possui grande relevância para prever churn.

Entretanto, um resultado curioso foi observado no modelo de **regressão logística**. Apesar da relevância do contrato mensal nos modelos de árvore, essa variável se mostrou **estatisticamente irrelevante na regressão logística**, apresentando:
### P>|z| > 0.8

Esse valor indica uma **probabilidade extremamente alta de que o coeficiente seja estatisticamente insignificante**, o que sugere que essa variável não contribui para explicar o churn dentro desse modelo específico.

---

## 4. Interpretação dos Resultados

Com base nos resultados obtidos, alguns padrões importantes podem ser destacados:

- Clientes com **menor tempo de permanência (tenure baixo)** apresentam maior probabilidade de evasão.
- O **serviço de fibra óptica** tem forte relação com churn, possivelmente refletindo problemas de qualidade, preço ou expectativas do cliente.
- O **tipo de contrato mensal** parece estar associado ao churn em modelos baseados em árvore, sugerindo que clientes sem compromisso de longo prazo têm maior tendência a cancelar o serviço.

Esses fatores indicam que tanto **a experiência inicial do cliente quanto o tipo de contrato** desempenham papéis importantes na retenção.

---

## 5. Estratégias de Retenção de Clientes

Com base nos fatores identificados, algumas estratégias podem ser propostas para reduzir a evasão de clientes.

### 5.1 Benefícios para Clientes nos Primeiros Meses

Como clientes com baixo tenure apresentam maior risco de churn, uma estratégia importante seria oferecer **benefícios nos primeiros meses de serviço**, como:

- descontos iniciais
- bônus de serviços
- suporte prioritário

Isso pode aumentar o engajamento e melhorar a experiência inicial do cliente.

---

### 5.2 Incentivo a Contratos de Longo Prazo

Outra estratégia seria incentivar contratos mais longos, oferecendo:

- **pacotes anuais com preços mais baixos**
- vantagens adicionais para contratos de maior duração

Isso pode reduzir a rotatividade de clientes e aumentar a previsibilidade da receita.

---

### 5.3 Melhoria do Serviço de Fibra Óptica

Como o uso de fibra óptica aparece como um fator relevante para churn, é importante avaliar:

- qualidade do serviço
- estabilidade da conexão
- atendimento técnico

Investimentos na **melhoria da experiência com fibra óptica** podem aumentar a satisfação dos clientes que utilizam esse serviço.

---

## 6. Conclusão

A análise realizada permitiu identificar fatores importantes associados à evasão de clientes. Entre os principais fatores destacam-se o **tempo de permanência do cliente (tenure)** e o **uso de fibra óptica**, ambos com forte impacto nos modelos analisados.

Além disso, foi observado que diferentes modelos podem interpretar as variáveis de maneira distinta, como no caso do **contrato mensal**, que foi relevante para modelos baseados em árvore, mas estatisticamente insignificante na regressão logística.

Com base nesses resultados, estratégias focadas em **retenção nos primeiros meses, incentivo a contratos mais longos e melhoria na qualidade do serviço de fibra óptica** podem contribuir significativamente para reduzir a evasão de clientes.

Essas ações podem melhorar a satisfação do cliente, fortalecer o relacionamento com a empresa e aumentar a retenção a longo prazo.