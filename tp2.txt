UNIVERSIDADE FEDERAL DE MINAS GERAIS
Instituto de Ciências Exatas
Departamento de Ciência da Computação

DCC207 -- Algoritmos 2
Prof. Renato Vimieiro

Trabalho Prático 1 -- Manipulação de sequências

Objetivos
---------

Nesse trabalho serão abordados os aspectos práticos relacionados à implementação
de algoritmos aproximativos. Especificamente, abordaremos o problema dos k-centros,
útil na tarefa de agrupamento em aprendizado de máquinas.

Abordaremos também questões de comparação empírica de algoritmos/programas. Nesse
sentido, vamos comparar a implementação do algoritmo 2-aproximado para o problema
do k-centro com o algoritmo clássico para o problema de agrupamento (K-Means). As
comparações deverão avaliar tanto aspectos de demanda computacional quanto de qualidade
de solução.

Tarefas
-------

Os alunos deverão implementar o algoritmo 2-aproximado visto em aula usando a
linguagem Python 3. Deverão ser implementadas também todas as funções auxiliares
envolvidas no algoritmo. Isto é, deverão ser implementadas funções para o cálculo
de distâncias.

Os alunos deverão implementar a função de distância de Minkowski, a qual deverá ser avaliada
nos experimentos com diferentes valores de p≥1 (obrigatoriamente deverão ser testados p=1 e 2,
as quais equivalem, respectivamente, a distância Manhattan e Euclidiana). A implementação
deverá ser feita usando funções vetoriais com a biblioteca NumPy.

Tendo implementado o algoritmo para agrupamento e a métrica de distância, o próximo passo
é a avaliação empírica do método. O método deverá ser avaliado com conjunto de dados
obtidos na UCI Machine Learning Repository (referência abaixo). Devem ser escolhidos
10 conjuntos de dados com, no mínimo, 700 exemplos (instâncias). Os conjuntos de dados
devem ser exclusivamente numéricos para a tarefa de classificação (o atributo classe/label)
deve ser ignorado durante o agrupamento cálculo de distância; o número de valores distintos
para essa variável determina o número de grupos/clusters a buscar. Embora o algoritmo seja
2-aproximado, a escolha dos centros é arbitrária e pode influenciar na qualidade da solução.
Dessa forma, para cada conjunto de dados, deverão ser realizados 30 testes/execuções do
algoritmo (note que a matriz de distância deve ser computada uma única vez, pois essa
nunca se altera). A cada execução deve-se armazenar o raio da solução e também computar
duas medidas clássicas em avaliação de agrupamentos: silhueta e índice de Rand ajustado.
Essas duas últimas métricas não precisam ser implementadas, devendo ser usadas as implementações
da biblioteca Scikit Learn (https://scikit-learn.org/stable/index.html). Além das métricas
de qualidade, deverão ser armazenados também o tempo de processamento de cada execução.

A título de comparação da qualidade da solução, os experimentos acima deverão ser repetidos
com a implementação do algoritmo K-Means também disponível no Scikit Learn 
(https://scikit-learn.org/stable/modules/clustering.html#k-means). Observe que todas
as medidas de desempenho também deverão ser computadas para essa implementação.

Finalmente, os resultados dos experimentos devem ser agregados em uma tabela com as
respectivas médias e desvios-padrão por experimento, e também por algoritmo/implementação.
Em seguida, deve ser feita uma análise dos experimentos, descrevendo as observações da
comparação (qualidade de resposta, tempo de execução etc). Para essa etapa, deve ser
feito um relatório em formato de artigo científico com: uma introdução ao problema, uma
descrição dos métodos e métricas usadas, a descrição da implementação, a descrição dos
experimentos, incluindo as bases de dados, e apresentação e análise dos resultados, e
uma conclusão. Esse artigo deve ter entre 5 e 8 páginas no formato da SBC (link abaixo).

O que entregar?
---------------

Devem ser entregues todos os arquivos fonte usados na implementação. O artigo contendo
o relatório deve ser entregue em formato pdf. As bases de dados usadas não devem ser
entregues, mas devem ser reportados claramente no relatório, permitindo que sejam
recuperadas posteriormente. OS ARQUIVOS NAO DEVEM SER COMPRIMIDOS EM HIPOTESE ALGUMA. 
Cada arquivo deve ser anexado individualmente.

Política de Plágio
------------------

Os alunos podem, e devem, discutir soluções sempre que necessário. Dito isso,
há uma diferença bem grande entre implementação de soluções similares e cópia
integral de ideias. Trabalhos copiados na íntegra ou em partes de outros alunos
e/ou da internet serão prontamente anulados. Caso hajam dois trabalhos copiados
por alunos diferentes, ambos serão anulados.

Datas
-----

Entrega Teams: 17/07/2022 às 23h59


Política de atraso
------------------

Haverá tolerância de 30min na entrega dos trabalhos. Submissões feitas depois
do intervalo de tolerância serão penalizados. 
- Atraso de 1 dia: 50%
- Atraso de 2+ dias: não aceito

Serão considerados atrasos de 1 dia aqueles feitos após as 0h30 do dia de entrega.
A partir daí serão contados o número de dias passados da data de entrega.


Referências
------------------

- https://en.wikipedia.org/wiki/Minkowski_distance
- https://archive.ics.uci.edu/ml/index.php
- https://www.sbc.org.br/documentos-da-sbc/category/169-templates-para-artigos-e-capitulos-de-livros