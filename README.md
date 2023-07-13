# Diabetes prediction using Random Forest

Diabetes descreve um grupo de doenças metabólicas em que uma pessoa tem alto nível de açúcar no sangue devido à produção insuficiente de insulina, resposta inadequada das células à insulina ou uma combinação de ambos.

É importante **prevenir** e **diagnosticar** a diabetes em estágio inicial, pois pode ser a causa de muitas outras doenças, como as renais e cardíacas.

## Objetivo 🎯

Desenvolver um modelo preditivo para diabetes utilizando Machine Learning com o classificador Random Forest, indicando se um paciente tem ou não a doença.

## Descrição do Dataset 📝

O [Sylhet Diabetes Dataset](https://archive.ics.uci.edu/dataset/529/early+stage+diabetes+risk+prediction+dataset) contém 16 atributos preditores e um atributo alvo com 520 registros que foram coletados usando questionários diretos dos pacientes do Diabetes Hospital em Sylhet, Bangladesh e aprovado por médicos.

 - **Atributos:**
   
**1)** Age: idade  - 20-65  
**2)** Sex: sexo - Male/Female  
**3)** Polyuria: frequência urinária -  Yes/No  
**4)** Polydipsia: sede excessiva - Yes/No  
**5)** sudden weight loss: perda de peso não intencional - Yes/No  
**6)** weakness: fraqueza - Yes/No  
**7)** Polyphagia: excesso de fome - Yes/No  
**8)** Genital thrush: candidíase - Yes/No  
**9)** visual blurring: visão embaçada - Yes/No  
**10)** Itching: coceira -  Yes/No  
**11)** Irritability: irritabilidade - Yes/No  
**12)** delayed healing: cicatrização tardia - Yes/No  
**13)** partial paresis: paresia parcial - Yes/No  
**14)** muscle stiffness: rigidez muscular - Yes/No  
**15)** Alopecia: alopecia - Yes/No  
**16)** Obesity: obesidade - Yes/No  
**17)** Class: classe preditora para diabetes - Positive/Negative

 Na etapa de pré-processamento dos dados foi feita a verificação de atributos com valores faltantes, outliers e transformação de atributos não- numéricos em númericos.

## Modelo de aprendizado de máquina:     	Random Forest 🌳

- **Formalização Matemática :**

O algoritmo de treinamento para Random Forest aplica a técnica geral de bootstrap aggregating, ou bagging, a aprendizes de árvores. 

Dado um conjunto de treinamento X = $\ x_1$, ..., $\ x_n$  com respostas Y = $\ y_1$, ..., $\ y_n$, é selecionado  uma amostra aleatória com substituição do conjunto de treinamento e ajusta árvores a estas amostras:

For b = 1, ..., B:

 1.  Amostra, com substituição,  n  exemplos de treinamento de  X,  Y; chamados de $\ X_b$ e $\ Y_b$.
 2. Treinar uma árvore de classificação ou regressão de $\ f_b$ em $\ X_b$, $\ Y_b$.

Após o treinamento, as previsões para amostras não vistas x' podem ser feitas pela média das previsões de todas as árvores de regressão individuais em x':

ou pelo voto da maioria, nos casos das árvores de classificação.

Esse procedimento de bootstrapping leva a um melhor desempenho do modelo, pois diminui a variância do modelo, sem aumentar o viés. É uma forma de descorrelacionar as árvores, mostrando-lhes diferentes conjuntos de treinamento.

## Avaliação 🔎

Foram utilizados para os dados de treino: 70% e para os dados de teste: 30%.

Utilizado o classificador Random Forest, e para en contrar os recursos ideais a serem usados no treinamento, foi escolhida a técnica de **eliminação de recursos recursivos**, denominada **RFECV** (Recursive Feature Elimination with Cross-Validation).  

O desempenho do modelo foi medido através da Matriz de Confusão, Acurácia, Precision, Recall e F1-score.

## Conclusão 📈

Neste projeto, foi analisado a predição de diabetes para 520 pacientes. 

O modelo criado como resultado da utilização do Random Forest com o RFEC resultou em uma acurácia de 99,35%.
