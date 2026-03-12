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

Após a seleção dos algoritmos, procedemos com o treinamento e teste de cada um deles para avaliar sua performance. Além disso, utilizamos o método de seleção de features RFE para identificar as variáveis mais relevantes e impactantes na base de dados.

Top K Precisão: A Top K Precisão é uma métrica de avaliação utilizada em modelos de classificação e sistemas de recomendação que mede a proporção de itens relevantes entre os K primeiros resultados previstos pelo modelo. Ela indica quantos dos casos recomendados ou classificados entre as primeiras posições realmente pertencem à classe positiva. Valores mais altos indicam que o modelo é mais preciso ao priorizar os resultados mais relevantes.

Recall Top K: O Recall Top K é uma métrica que avalia a capacidade do modelo de identificar os casos positivos dentro dos K primeiros resultados classificados. Ele mede quantos dos verdadeiros positivos presentes no conjunto de dados foram recuperados entre as primeiras recomendações do modelo. Valores mais altos indicam que o modelo consegue capturar uma maior quantidade de casos relevantes nas posições mais importantes da classificação.

Top K F1-Pontuação: A Top K F1-Pontuação é uma métrica que combina Top K Precisão e Recall Top K, calculando a média harmônica entre essas duas medidas. Ela fornece uma avaliação equilibrada do desempenho do modelo, considerando tanto a precisão das recomendações quanto a capacidade de recuperar os casos positivos. Valores mais altos indicam que o modelo apresenta um bom equilíbrio entre identificar corretamente os casos relevantes e cobrir uma maior proporção deles dentro do Top K.

<img width="346" height="139" alt="image" src="https://github.com/user-attachments/assets/5e143ba4-5189-423c-b5ed-8ae101a5776b" />

#  Escolha do Modelo

Após a comparação dos modelos, a Logistic Regression apresentou o melhor desempenho, alcançando um Precision@20 de 0,5238, superando os demais algoritmos avaliados. Esse resultado indica que aproximadamente 52% dos clientes classificados entre os 20 primeiros possuem resposta positiva real, demonstrando maior capacidade do modelo em priorizar corretamente os clientes mais relevantes.

Dessa forma, a Regressão Logística foi selecionada como o modelo final do projeto, por apresentar melhor desempenho na tarefa de ranqueamento e identificação dos clientes com maior probabilidade de resposta, tornando-se a melhor opção para apoiar estratégias de decisão baseadas em dados.

<img width="351" height="56" alt="image" src="https://github.com/user-attachments/assets/c0724a3f-7f99-46ba-b315-1dffedcba394" />

# Curvas de Rankeamento

## Cummulative Curve Manually

Avalia o desempenho acumulado do modelo, mostrando como a taxa de acertos evolui conforme aumentamos a proporção de casos analisados.

<img width="1002" height="519" alt="image" src="https://github.com/user-attachments/assets/bf2f6d60-3173-48ff-96d8-2b71c2d8eaf0" />

## Lift Curve Manually

Mede o ganho do modelo em relação a uma seleção aleatória, indicando quão melhor ele identifica positivos em diferentes faixas de probabilidade.

<img width="996" height="522" alt="image" src="https://github.com/user-attachments/assets/8de1ed4c-d90d-40c2-a312-aa591b12b90b" />


# Hiperparâmetros

Foi empregada a técnica de Random Search para otimizar a busca dos melhores hiperparâmetros. A fim de identificar o parâmetro ideal, optei por utilizar uma amostra referente a um período de 1 ano. Essa escolha permite aumentar o número de iterações em um espaço de tempo reduzido, maximizando a probabilidade de localizar um mínimo global.

# Resultados 

Qual é a proporção de clientes que demonstram interesse em contratar o seguro automotivo? A equipe de vendas consegue alcançá-los com 20.000 ligações?  
i. O banco de dados contém 46.876 clientes (12,3%) com interesse em planos de saúde e 334.232 (87,7%) sem interesse.
ii. O modelo apresenta uma taxa de acerto de 24,10% (24,14% em cenário favorável e 24,06% em cenário desfavorável). Com esse desempenho, em 20.000 chamadas, a equipe consegue falar com cerca de 4.820 clientes interessados (variando entre 4.812 e 4.828). O recall é bastante alto, em torno de 98,31% (±0,0016).

Se a equipe tiver capacidade para realizar 40.000 chamadas, quantos clientes interessados em seguro automotivo poderão ser contatados?  
Com 40.000 ligações, o modelo permite alcançar aproximadamente 9.640 clientes interessados (entre 9.624 e 9.656, dependendo do desempenho).

Quantas chamadas são necessárias para atingir 80% dos clientes que desejam adquirir o seguro automotivo?  
O modelo conseguiu identificar 98,31% dos clientes interessados (46.084 pessoas) dentro de um universo de 381.109 clientes. Para chegar a 80% dos interessados, é preciso realizar cerca de 155.064 chamadas, garantindo contato com aproximadamente 37.501 clientes.


