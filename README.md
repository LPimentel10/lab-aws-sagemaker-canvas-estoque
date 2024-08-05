# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas. Neste Lab DIO, você aprenderá a usar o SageMaker Canvas para criar previsões de estoque baseadas em Machine Learning (ML). Siga os passos abaixo para completar o desafio!

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira nosso repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).


## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)

- Dê um fork neste projeto e reescreva este `README.md`. Sinta-se à vontade para detalhar todo o processo de criação do seu Modelo de ML para uma "Previsão de Estoque Inteligente".
- Para isso, siga o [passo a passo] descrito a seguir e evolua as suas habilidades em ML no-code com o Amazon SageMaker Canvas.
- Ao concluir, envie a URL do seu repositório com a solução na plataforma da DIO.


## 🚀 Passo a Passo

### 1. Selecionar Dataset

-   Navegue até a pasta `datasets` deste repositório. Esta pasta contém os datasets que você poderá escolher para treinar e testar seu modelo de ML. Sinta-se à vontade para gerar/enriquecer seus próprios datasets, quanto mais você se engajar, mais relevante esse projeto será em seu portfólio.
-   Escolha o dataset que você usará para treinar seu modelo de previsão de estoque.
-   Faça o upload do dataset no SageMaker Canvas.

### 2. Construir/Treinar

-   No SageMaker Canvas, importe o dataset que você selecionou.
-   Configure as variáveis de entrada e saída de acordo com os dados.
-   Inicie o treinamento do modelo. Isso pode levar algum tempo, dependendo do tamanho do dataset.

### 3. Analisar

-   Após o treinamento, examine as métricas de performance do modelo.
-   Verifique as principais características que influenciam as previsões.
-   Faça ajustes no modelo se necessário e re-treine até obter um desempenho satisfatório.

### 4. Prever

-   Use o modelo treinado para fazer previsões de estoque.
-   Exporte os resultados e analise as previsões geradas.
-   Documente suas conclusões e qualquer insight obtido a partir das previsões.

## 📋 Resultados

Dataset utilizado: dataset-1000-com-preco-promocional-e-renovacao-estoque.csv

Model type: Time series forecasting(O modelo irá prever QUANTIDADE_ESTOQUE usando valores de dados passados ​​para prever valores de dados futuros.)

-   Avg. wQL = 0.437 -> A perda quantílica ponderada média avalia a performance de previsões para diferentes quantis. A quantile loss é útil para prever intervalos de confiança, não apenas um valor central, permitindo entender a incerteza das previsões. Um valor de 0.437 indica a média da perda ponderada através de diferentes quantis. Quanto menor o valor, melhor a previsão do modelo em termos de quantis.
-   MAPE = 1.345 -> A MAPE mede a precisão da previsão como uma porcentagem. É calculada pela média dos erros absolutos divididos pelos valores reais. Com um valor de 1.345, isso significa que, em média, as previsões do modelo estão errando em 134.5%. MAPE é frequentemente criticado por amplificar erros em previsões de valores baixos.
-   WAPE = 0.754 -> Semelhante ao MAPE, mas ponderado pelos valores reais. Isso ajuda a evitar que grandes erros em valores baixos distorçam a métrica. Um valor de 0.754 indica que a média ponderada dos erros absolutos é de 75.4%. Oferece uma visão mais equilibrada do desempenho do modelo em relação ao MAPE.
-   RMSE = 30.926 -> A RMSE mede a média da magnitude dos erros de previsão ao elevar ao quadrado os erros, calcular a média desses valores e, em seguida, tirar a raiz quadrada. Um valor de 30.926 indica que o desvio padrão dos erros de previsão é de aproximadamente 30.926 unidades. Valores mais baixos indicam previsões mais precisas.
-   MASE = 0.880 -> A MASE compara a precisão do modelo com a de uma previsão simples baseada na média histórica, normalizando o erro absoluto médio pelo erro absoluto médio de um modelo de referência. Um valor de 0.880 indica que o modelo é, em média, 12% mais preciso do que o modelo de referência. Valores abaixo de 1 indicam que o modelo é melhor que o de referência.

Resumo:
- Avg. wQL (0.437): Indica uma boa performance em prever intervalos de confiança.
- MAPE (1.345): Mostra que as previsões têm um erro percentual alto, o que pode ser um sinal de que o modelo precisa ser ajustado.
- WAPE (0.754): Oferece uma visão mais realista do erro percentual, mostrando um desempenho razoável.
- RMSE (30.926): O desvio padrão dos erros é alto, sugerindo que os erros são substanciais.
- MASE (0.880): Indica que o modelo é melhor que um modelo de referência simples, mas ainda há espaço para melhorias.


## 🤔 Dúvidas?

Esperamos que esta experiência tenha sido enriquecedora e que você tenha aprendido mais sobre Machine Learning aplicado a problemas reais. Se tiver alguma dúvida, não hesite em abrir uma issue neste repositório ou entrar em contato com a equipe da DIO.
