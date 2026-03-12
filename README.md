# health_insurance_classification
# Problema de Negócio
Identificar quais clientes têm maior probabilidade de adquirir um Seguro de Saúde, utilizando padrões históricos e comportamentais para orientar estratégias comerciais da seguradora. A meta é priorizar campanhas e abordagens direcionadas, aumentando a taxa de conversão e otimizando recursos de marketing e vendas.

# Sobre o Cliente
A seguradora deseja lançar ou expandir a oferta de Seguro de Saúde para clientes atuais ou potenciais. No entanto, não é viável oferecer de forma massiva para todos os clientes devido a custos e recursos limitados. É necessário entender padrões de comportamento e características de clientes que indicam maior propensão à compra.

# Descrição dos Dados
<img width="839" height="580" alt="image" src="https://github.com/user-attachments/assets/25462ad1-2e2d-4180-afe2-f2f4a2ecb55e" />

# Estratégia da Solução
Para garantir uma entrega rápida e eficiente do primeiro modelo, com o objetivo de trazer valor para a empresa e permitir decisões ágeis por parte da Equipe de Negócio, foi adotado o método CRISP-DM.

O método CRISP-DM é composto por 9 etapas cíclicas, em que a cada iteração dessas etapas, o resultado de negócio é aprimorado, buscando entregas cada vez mais rápidas e de maior qualidade, com maior precisão. Isso possibilita que as equipes que utilizarão os resultados desenvolvidos tenham um produto minimamente utilizável já na primeira entrega, e que seja aprimorado ao longo do tempo.

<img width="774" height="430" alt="image" src="https://github.com/user-attachments/assets/089fe305-a699-475c-a048-a25e85f5b49c" />

CRISP-DM:

1. Problema de Negócio: Esta etapa tem como objtive receber o problema de negócio que será resolvido. É nesta etapa que é recebido a pergutna ou o pedido feito pelo dono do problema, que no caso deste projeto, é o CFO da rede Rossmann.

2. Entendimento de Negócio: Esta etapa tem como objetivo entender a dor do dono do problema e qual a sua real necessidade. Nesta etapa podem surgir protótipos da solução para validar com o dono do problema o que ele deseja como solução.

3. Coleta de Dados: Esta etapa tem como objetivo realizar a coleta dos dados, buscando eles nas tabelas do(s) banco(s) de dados da empresa.

4. Limpeza dos Dados: Esta etapa tem como objetivo remover toda e qualquer sujeira nos dados. Um dado sujo pode ser entendido como um dado que irá atrapalhar a performance final do algoritmo de Machine Learning. Tomando o cuidado entender bem o fenômeno que está sendo estudado para que não sejam removidos dados importantes para a modelagem do problema.

5. Exploração dos Dados: Esta etapa tem como objetivo entender os dados e como eles se relacionam entre si. Normalmente, são criadas hipóteses acionáveis de negócio que são posteriormente validadas utilizando técnicas de análise de dados. Além da criação de novas features que serão utilizadas na etapa de Modelagem de Dados.

6. Modelagem dos Dados: Esta etapa tem como objetivo preparar os dados para que eles sejam utilizados pelos algoritmos de Machine Learning. É nesta etapa que são feitos as transformações e encodign dos dados, a fim de facilitar o aprendizado do algoritmo utilizado.

7. Aplicação de Algoritmos de Machine Learning: Esta etapa tem como objetivo selecionar e aplicar algoritmos de Machine Learning nos dados preparados nas etapas anteriores. É nesta etapa que são selecionados os algoritmos e feito a comparação de performance enetre eles, para selecionar o algoritmos que melhor performou como algoritmo final.

8. Avaliação de Performance: Esta etapa tem como objetivo verificar a performance do algoritmo selecionado na etapa anterior com os resultados atuais, ou base line atual. Neste momento é feito a tradução da performance do algoritmo para perfomance de negócio. Ou seja, quanto a solução criada tratrá de retorno financeiro para a empresa. Caso a performance seja aceitável, o algoritmo é publicado e é retornado para a etapa de entendimento de negócio novamente, a fim entender melhor possíveis lacunas e assim melhorar a performance do algoritmo selecionado. Caso a performance não seja aceitável, o algoritmo não é publicado e é retornado para a etapa de entendimento de negócio para fazer uma nova iteração e assim melhorar a performance da solução.

9. Publicação da Solução: Esta etapa tem como objetivo publicar o algoritmo selecionado, deixando publico e utilizável a solução criada.

# Mindmap e Principais Insights

<img width="895" height="639" alt="image" src="https://github.com/user-attachments/assets/d24a54f2-3b8d-4899-9a94-aa6a115dcf2b" />

# Análise Exploratorio de Dados

1.0 Quanto mais velho o cliente, maior é a possibilidade de querer um plano de saúde.

**Falso**: As pessoas entre 40 e 50 estão mais interessadas em ter plano de saúde.
  
<img width="804" height="383" alt="image" src="https://github.com/user-attachments/assets/5ba44ec7-31c9-45ed-be2b-54d7fd46ab57" />

2.0 Clientes com seguro de carro são mais tímidos para obter seguro de saúde.

**Falso**: Clientes sem seguro de carro são mais propensos a obter seguro de saúde. Neste banco de dados, 99,7% dos clientes estão segurados anteriormente.

<img width="801" height="387" alt="image" src="https://github.com/user-attachments/assets/13afa4be-eb58-4906-b6d6-71dc33c288f8" />

3.0 Gênero influencia a adesão ao seguro de saúde

**Verdadeiro**: Clientes do gênero masculino apresentam maior propensão a adquirir o seguro de saúde em comparação com clientes do gênero feminino.

<img width="801" height="383" alt="image" src="https://github.com/user-attachments/assets/d6ff69b8-edfd-4846-8095-ebe0cbb36a2b" />

# Definição de Modelos de Machine Learning

No primeiro ciclo do projeto, foram selecionados cinco algoritmos para teste, visando identificar o algoritmo com melhor desempenho e custo de implementação. Nessa etapa inicial, optou-se pela simplicidade, considerando que era o primeiro ciclo do projeto e o objetivo principal era entregar uma solução mínima utilizável para a equipe de negócios e pelo CFO.

Os algotitmos selecionados foram: 

* K-Nearest Neighbors (KNN)

* Logistic Regression

* Extra Trees Classifier

* Random Forest

* LightGBM (LGBM)


