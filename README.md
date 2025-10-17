<!-- antes de enviar a versão final, solicitamos que todos os comentários, colocados para orientação ao aluno, sejam removidos do arquivo -->
# Previsão de casos de Depressão e pensamentos suicidas no meio acadêmico.

#### Aluno: [Eduardo Mattos Barboza](https://github.com/EduMBR)
#### Orientadora: [Manoela Koher](https://github.com/link_do_github).

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

<!-- para os links a seguir, caso os arquivos estejam no mesmo repositório que este README, não há necessidade de incluir o link completo: basta incluir o nome do arquivo, com extensão, que o GitHub completa o link corretamente -->
- [Link para o código](https://github.com/EduMBR/Monografia-Bi-Master-2023.2/blob/main/Depressao_estudantil.ipynb). <!-- caso não aplicável, remover esta linha -->

- [Link para a monografia](https://github.com/EduMBR/Monografia-Bi-Master-2023.2/main/README.md). <!-- caso não aplicável, remover esta linha -->

---

### Resumo

<!-- trocar o texto abaixo pelo resumo do trabalho, em português -->

O objetivo deste trabalho é prever casos de depressão e pensamentos suicidas no meio acadêmico. Os dados utilizados são provenientes do dataset do Kaggle: student-depression-dataset e que foram coletados através de pesquisas respondidas por estudantes na Índia. O conjunto de dados inclui detalhes demográficos, pressões acadêmicas e relacionadas ao trabalho, hábitos de estilo de vida e indicadores específicos de saúde mental. Com isso, foram realizadas análises, correções de dados, desenvolvimento de modelos de classificação, a fim de conseguir prever a ocorrência de depressão e pensamentos suicidas no meio acadêmico. 

### 1. Introdução

Segundo o ministério da saúde, a depressão é uma doença mental de elevada prevalência e é a mais associada ao suicídio, tende a ser crônica e recorrente, principalmente quando não é tratada. Além disso, segundo a Organização mundial da Saúde, na América Latina o Brasil é o país com maior prevalência de casos de depressão. Dessa forma, o presente trabalho visa fornecer uma forma de auxiliar na detecção de sintomas de depressão, tendência a pensamentos suicidas, fatores que contribuem para esse quadro e incentivar as pessoas afetadas a buscar tratamento.

Acerca do conjunto de dados, eles foram originalmente coletados por meio de pesquisas anônimas e autorrelatadas, distribuídas em várias instituições de ensino. Os participantes forneceram informações sobre dados demográficos, desempenho acadêmico, hábitos de estilo de vida e indicadores de saúde mental, utilizando instrumentos padronizados e escalas de depressão. Os dados estão anônimos, possuem 27901 regstros, com atributos sobre demografia, indicadores acadêmicos, estilo de vida, bem estar e saúde.

### 2. Modelagem

Inicialamente foi realizada a análise dos dados, com o intuito de compreender suas colunas e verificar possíveis inconsistências. Foram feitas análises visuais de diversas colunas e foi constatado que as variáveis relacionadas a emprego possuem 99% dos valores uniformes ou zerados. Alguns exemplos foram as colunas: "Profession", "Work Pressure" e "Job Satisfaction",as quais respectivamente possuem 99% dos valores preenchidos como: "Student" e zeros. Além disso, a coluna "Finantial Stress" deveria ser numérica, no entanto estava como categórica, porque 3 registros continham a string "?". Dessa forma, a substituição dessa string pelo valor 0 foi realizada, para uniformizar a coluna. 

No que tange outros tratamentos de dados, foi utilizado o LabelEncoder para codificar as colunas categóricas, facilitando a utilização dos modelos. Para normalizar os dados, o StandarScaler foi o escolhido. Não foram encontrados valores nulos e a base está balanceada com relação a casos de depressão e pensamentos suicidas. 

No quesito de modelos, foram utilzados os de classificação a fim de identificar as pessoas com pensamentos suicidas e as com depressão. Os modelos escolhidos foram: SVM, Random Forest, KNN e Decision Tree Classifier. 


### 3. Resultados

As correlações mais fortes para os casos de depressão foram as respectivas variáveis: 
Pensamentos suicidas, Pressão acadêmica, estresse financeiro. Já as variáveis com maior correlação na identificação de pensamentos suicidas foram: 
Depressão, estresse financeiro e pressão acadêmica.

<img width="700" height="600" alt="image" src="https://github.com/user-attachments/assets/7cec07c5-776c-464f-ad77-6cfe049d0127" />                

Correlação entre as variáveis

#### Identificação de Depressão

Os modelos que melhor performaram foram o Random Forest Classifier, junto do SVM com os seguintes resultados:    

**Resultados de Treino**   
<img width="235" height="84" alt="image" src="https://github.com/user-attachments/assets/92aff8b8-569e-4413-a678-a03bddbf49b9" />

**Resultados de Teste**    
<img width="235" height="84" alt="image" src="https://github.com/user-attachments/assets/193d3ebe-736d-4cb5-81f1-47ba7c5b8bfa" />


#### Identificação de Pensamentos suicidas    

Os modelos que melhor performaram, também foram o Random Forest Classifier, junto do SVM com os seguintes resultados:
   
**Resultados de Treino**          
<img width="240" height="84" alt="image" src="https://github.com/user-attachments/assets/ebf01b16-29a9-42c7-b8de-a6a8a1898608" />

**Resultados de Teste**        
<img width="240" height="84" alt="image" src="https://github.com/user-attachments/assets/0e0c939b-d72e-440c-8387-1774603c2fd1" />

### 4. Conclusões

Para uma melhor qualidade de vida e prevenção de casos de suicídio, faz se necessário investigar possíveis fatores que contribuem para esses quadros. Dessa forma, o presente trabalho buscou identificar esses fatores e utilizá-los, a fim de identificar pessoas que estão ou possam vir a apresentar esses quadros. Dentre os modelos desenvolvidos, os que apresentaram melhores resultados de teste foram os que utilizaram Random Forest Classifier e SVM.

---

Matrícula: 231101066

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
