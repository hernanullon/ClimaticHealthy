## Projeto <Clima e saúde>

## Descrição resumida do projeto :

Este projeto consiste na análise de dados de temperatura e umidade para mapear condições climáticas saudáveis que contribuam para 
o bem estar das pessoas que vivem na cidade de Campinas SP.
Para realização deste projeto foram utilizadas duas bases de dados principais : A base de dados da Cepagri que possui dados de temperatura e umidade
no período de 1997 a 2018 e a base de dados da Cetesb nos meses de janeiro a maio de 2020.
Foi realizado  o pré processamento dos dados  para correção os dados faltantes em ambas as bases e foram realizados cálculos para encontrar três
indicadores que caracterizam o conforto térmico de uma pessoa com relação ao ambiente, são eles : humidex, ondas de calor, ondas de frio.
Após ter encontrado os indicadores foram aplicados algoritmos de clusterização para identificar condições saudáveis de clima que contribuam para o bem estar das pessoas.

## Abstract :

This project consists of analyzing temperature and humidity data to map healthy climatic conditions that contribute to
the welfare of people living in the city of Campinas SP.
To carry out this project, two main databases were used: The Cepagri database, which has temperature and humidity data
from 1997 to 2018 and the Cetesb database from January to May 2020.
Pre-processing of data was performed to correct missing data in both databases and calculations were performed to find three
Indicators that characterize a person's thermal comfort in relation to the environment are: humidex, heat waves, cold waves.
After finding the indicators, clustering algorithms were applied to identify healthy climate conditions that contribute to people's well-being.

## Equipe :
Daniel Filipe Vieira RA : 262720

Ruben Hernan Alcivar Ullon RA: 262729


## Video do projeto

https://drive.google.com/file/d/162rskPRvc0Ap1H90L5hTd58whU9q7zAJ/view?usp=sharing


## 1. Introdução e motivação


Um tema muito recorrente atualmente são as mudanças climáticas que o mundo vem sofrendo ao longo do tempo. Aquecimento global, efeito estufa e derretimento de geleiras
polares são efeitos associados ao tema em questão [1].
A atividade humana está  diretamente ligada á essas alterações climáticas aumentando a concentração de gases tóxicos como dióxido de carbono na atmosfera devido a queima de combustíveis fósseis e de florestas  contribuindo para o aumento do efeito estufa [2].
Por outro lado essas mudanças climáticas afetam diretamente a saúde das pessoas como por exemplo em períodos de maior estresse térmico (longos períodos com temperaturas muito baixas ou muito altas) ou acidentes naturais como enchentes e tempestades e também de forma indireta afetando a qualidade do ar , da água , interferindo nos vetores de transmissão de doenças [3].
Partindo desse principio que as mudanças climáticas afetam diretamente a saúde humana o presente projeto pretende calcular indicadores através das medidas coletadas de temperatura e umidade : Humidex, ondas de calor.



![Figura 1](https://github.com/hernanullon/ClimaticHealthy/blob/master/ambiente%20.png)


                                       Figura 1 - Ambiente





Na figura 2 é possível visualizar os principais problemas ocasionados pelas ondas de calor.


![Figura 2](https://github.com/hernanullon/ClimaticHealthy/blob/master/ilhas%20de%20calor.jpg)



                     Figura 2 - Problemas ocasionados pela presença das ilhas de calor
                     
Partindo deste contexto este projeto utiliza duas bases de dados, a base principal do projeto foi cedida pelo Centro de Pesquisas Meteorológicas e Climáticas aplicada a Agricultura (Cepagri), a Cepagri coleta dados de temperatura, umidade, direção do vento, intensidade de radição solar através de uma estação meteorológica que fica localizada dentro do Campus da Universidade Estadual de Campinas (Unicamp), na cidade de Campinas SP .
E uma segunda base de dados disponível no site da  Companhia Ambiental do Estado de São Paulo (Cetesb) também foi utilizada para comparar os dados de temperatura e umidade nos meses de março a maio de 2020 com os dados referentes a estas mesmas variáveis no periodo de 2017 a 2018.

A escolha do período de janeiro a maio de 2020 para analisar  se houve alterações climáticas, justifica-se  em virtude do isolamento social devido a pandemia causada pelo Covid 19.
Após a escolha dos datasets para o projeto foram estudadas e aplicadas técnicas para limpeza destes dados e por fim, aplicou -se a metodologia KDD (Knowledge Discovery in Databases – KDD) para obter conhecimento a partir dos dados (tais como níveis de temperatura e umidade ) e assim  calcular três principais indicadores de condições climáticas: Humidex, ilhas de calor, ilhas de frio.

A partir do cálculo destes indicadores realizar a classificação (clusterização) dos dados utilizados para se identificar condições climáticas saudáveis a partir de dados de temperatura e umidade e assim poder fazer recomendações para as pessoas dos cuidados que devem ser considerados para evitar que condições climáticas desfavoráveis como a presença de ondas de calor , ondas de frio e umidade relativa do ar baixa afetem a saúde das pessoas .



## 2. Pergunta de pesquisa

É possível a identificação de condições climáticas saudáveis  a  partir de dados de temperatura e umidade ?

## 3. Objetivos do projeto

* Realizar a análise exploratória dos dados de temperatura e umidade da base de dados do Cepagri e da Cetesb utilizando a técnica KDD

* Cálculo dos indicadores como humidex e ondas de calor.

* Identificar condições climáticas desfavoráveis de acordo com os indicadores calculados, para fazer recomendações de hábitos saudáveis nas pessoas.


## 4. Recursos e métodos


* 4.1. Bases de dados

|Base de dados   |Endereço na web   |Resumo e descrição de uso    |
|---|---|---|
| Base 1 - Cepagri da Unicamp  |  |Essa foi a principal base de dados utilizada no projeto, nessa base foram aplicadas técnicas para completar os dados faltantes, foram realizados cálculos para encontrar os indicadores humidex, onda de calor, onda de frio.   |
| Base 2  - Cetesb  |https://cetesb.sp.gov.br/ar/dados-horarios/  | Esta base de dados foi utilizada para efeitos de comparações entre os meses de janeiro  maio de 2020  e o mesmo período do ano passado  |


* 4.2 Ferramentas

Toda a análise foi feita na ferramenta de notebook jupyter na linguagem de programação Python (Versão 3.6), no entanto, vale mencionar as bibliotecas externas usadas no projeto:

| bibliotecas  | Endereço web  | Descrição de uso  |
|---|---|---|
| tslearn  | https://tslearn.readthedocs.io/en/stable/index.html  |   |
| scikit-learn  | https://scikit-learn.org/stable/  |   |

* 4.3. Metodologia

A metodologia adotada neste projeto foi a Knowledge Discovery in Data (KDD) , que é a descoberta de conhecimento a partir de uma base de dados[7].
E pode ser ilustrada na figura 3

![Figura 3](https://github.com/hernanullon/ClimaticHealthy/blob/master/Processo%20KDD%20.jpg)


                                 Figura 3 - Processo de estração do conhecimento a partir do processo KDD 

Com base nessa metodologia, __técnicas estatísticas__ como histogramas e medidas de dispersão foram utilizadas nas etapas de seleção e pré-processamento, com o objetivo de conhecer e manipular o conjunto de dados da melhor maneira. Além disso, __técnicas matemáticas e de visualização__ seriam aplicadas no estágio de pré-processamento para evitar todo tipo de missing data ou a presença de outliers.

Posteriormente, já em fase de transformação, novos parâmetros foram calculados, como os índices Humidex e as ondas de calor. Para os quais foram considerados os seguintes critérios:

O __Humidex__ foi proposto em 2016 e é descrito como uma métrica do desconforto térmico de uma pessoa em uma determinada condição de temperatura e umidade relativa do ar  [6].

O humidex é definido pela fórmula:
H = T + (0:555:[E - 10]); (2)
onde T é a temperatura em Graus Celsius e E é a pressão de vapor de água em milibars.
A pressão de vapor é descrita pela fórmula:
E = 6:11.e^5417:7530:( 1 /273.16 -  1 /td+ 273.16)

água para que haja condensação em unidades de graus Celsius.
Utilizamos uma aproximação para o ponto de orvalho (td) que leva em consideração a temperatura e
a umidade relativa, descrita em [7].
td = T - 100 - RH/5
Onde T é a temperatura e RH é a umidade relativa

Ele pode ser classificado conforme a tabela 1

|Valor de humidex    |Sensação térmica             |   
|---                 |---                          |
| Menor que 29       |Sem desconforto              |   
| De 30 a 39         |Desconforto ameno            |   
  De 40 a 45           |Desconforto, evitar esforço  |
  Acima de 45          |  Perigo                     |
  Acima de 54          |  Insolação iminente         |

Como as informações que temos são definidas em função do tempo, os algoritmos de __aprendizado de máquina__ foram adaptados para reconhecer padrões e comportamentos na forma de __séries temporais__.

## 5. Detalhamento do projeto

__Etapa 1 -__  Entendimento do problema - Nesta etapa o objetivo principal é entender o motivo que justifica a escolha do processo KDD, portanto a pergunta de pesquisa é quem guiará o processo  do ponto de vista do que ou quem utilizará esse conhecimento. Neste projeto esta etapa foi cumprida por meio de reuniões da dupla e pesquisas na literatura para encontrar bases teóricas sobre os problemas ocasionados pelas mudanças climáticas na saúde humana.

__Etapa 2 - Selection (Seleção)  -__ Nesta etapa foi feita a seleção do período do dataset que seria utilizado para realizar a análise.
Para o dataset fornecido pela Cepagri foram  escolhidos os meses de janeiro a dezembro para os anos de 2017 e 2018 , já para o dataset da Cetesb foram escolhido os meses de janeiro, fevereiro, março, abril e maio e as variáveis selecionadas em ambas as bases  foram temperatura e umidade

![Figura 5 Base de dados da Cepagri](./figuras/DB_cepagri.PNG)
![Figura 6 Base de dados da Cetesb](./figuras/DB_cetesb.PNG)

Link de notebook 1 [Selection]

__Etapa 3 - Preprocess -__ Para uma análise de séries temporais, é muito importante que cada um dos registros tenha sua data e hora em que essas informações foram registradas. O formato da data e hora do conjunto de dados foi dividido em três campos: Ano, Dia Juliano e Hora-Minuto. Portanto, foi necessário aplicar um algoritmo que alterasse esse formato para: __AAAA/mm/dd HH:MM__, a técnica utilizada foi baseada no seguente codigo:
~~~python
from datetime import datetime
jdate = year+'-'+julian_day+'-'+hour+'-'+minute
fmt = '%Y-%j-%H-%M'
date_time = datetime.strptime(jdate, fmt)
~~~
Após foi realizado um pré processamento utilizando a técnica de interpolação dos valores no ano de 2017 e 2018 para completar os valores faltantes de temperatura e umidade da base fornecida pelo Cepagri. Um exemplo da perda de dados é amostrada na Figura 4.

![Figura 5](./figuras/missing_data.PNG)

Por outro lado, a detecção de outliers foi realizada apenas para dados extremamente anômalos, pois se nosso estudo se basear na busca por condições climáticas extremas incomuns, um processo como o boxplot nos deixaria sem informações relevantes. Portanto, apenas através de estatisticas como a visualização da distribuição das variáveis, média e desvio padrão, tais problemas foram identificados.

__Etapa 4 - Transformation -__ Essa etapa começou com a integração dos 2 conjuntos de dados mencionados anteriormente, já pensando no que seriam os grupos de treinamento e teste dos algoritmos de aprendizado de máquina. Na Figura 6, podemos visualizar a integração.

![Figura 6](./figuras/transformation_integration.PNG)

Posteriormente, novos parâmetros, como o índice Humidex, foram calculados para cada medição de temperatura e umidade, usando o seguinte segmento de código:
~~~python
def get_humidex(T,H):
    z = 6.112*(10**((7.5*T)/(237.7+T)))*(H/100)
    return T+((5/9)*(z-10))
~~~
A partir desse cálculo foi possível classificar a condição climática em função desse indicador como : Confortable (confortável ) , some disconfort (algum desconforto). No entanto, os dados do Humidex precisavam ser preparados para um processo posterior de aprendizado de máquina, em que cada linha do Dataframe representaria uma data e cada coluna o valor para cada hora ao longo do dia, ou seja, cada linha formaria uma série temporal. Um exemplo é amostrado na Figura 6.

![Figura 6](./figuras/transformation_humidex.PNG)


__Etapa 5 - Data mining -__ Nesta etapa após realizar o pré processamento e a transformação dos dados dos datasets colocando esses dados num formato mais adequado para realizar a análise, a técnica de clusterização foi aplicada de acordo com o indicador Humidex.

O algoritmo de agrupamento escolhido para esse processo foi o K-Means adaptado para séries temporais. Onde sua implementação será descrita nas seguintes etapas:

O algoritmo K-Means precisa ajustar certos parâmetros, como métrica de distância, inicialização e número do cluster Apriori.
...1. A métrica de distância foi escolhida com base em seu desempenho no final da clusterização, onde a métrica Soft-DTW superou as demais. Uma ilustração de como essa métrica funciona é mostrada abaixo.

![Figura 7](./figuras/soft_dtw.PNG)

...2. Uma vez escolhida a métrica, a inicialização acordada para este estudo foi aleatória.
...3. Para definir o número ideal de grupos (K), a técnica do cotovelo foi utilizada com base na soma dos quadrados dos erros em que foi escolhido um K = 2. No entanto, essa etapa não terminaria até a escolha do parâmetro de aprendizado da métrica Soft-DTW, para a qual foi utilizado o critério do maior coeficiente de silhueta.

![Figura 8](./figuras/elbow_silhouette.PNG)

...4. Finalmente, o algoritmo K-Means foi executado com os seguentes parâmetros:
* K = 2
* metric = softdtw
* gamma = 1e-4
* init = random

Eles garantiram o melhor desempenho no conjunto de dados, com um coeficiente de silhueta de 0.7351. 

## 6. Evolução do projeto

Inicialmente  nossa intenção era de realizar o projeto com dados de poluição do ar atmosférico e classificar o ar de acordo com a quantidade de polentes no ar, porém diante da dificuldade em achar datasets com esse tipo de dados, optamos por trabalhar com dados de temperatura e umidade, uma vez que estão disponíveis pela Cepagri e no site da Cetesb.

## 7. Resultados e discussões

Um resultado da clusterização é mostrado na Figura 9.

![Figura 9](./figuras/clustering_series_temporales.PNG)

__Etapa 6 - Extract Knowledge -__ Nesta etapa utilizou -se  o conhecimento obtido a partir do dataset para classificar os dados de temperatura e umidade conforme o aprendizado na etapa de data mining.

Após clusterizar os dados de temperatura e umidade, foi realizado o treinamento do aprendizado de máquina com 70 % dos dados e 30 % dos dados foi usado para testar a aprendizagem de máquina.

## 8. Conclusões

## 9. Trabalhos futuros

## 10.  Referências




[1] W. H. ORGANIZATION, ed., Climate Change and Human Health - Risks and Responses, Genève, 2004.
OCLC: 254297040.
Disponível em < https://apps.who.int/iris/bitstream/handle/10665/44133/9789241598187_eng.pdf;jsessionid=F45966ED878C58D6CC7129FFE87DF3B0?sequence=1>

[2] As cidades que queremos Disponível em : <https://www.isglobal.org/es/ciudadesquequeremos?gclid=Cj0KCQjw1Iv0BRDaARIsAGTWD1s8PaszWCMZQG9CKFIHkiV-2PVh2Q8oZ8vWFKcxVEHfRHLJwXDFVOQaAvi8EALw_wcB#efectossalud>




[3] S. RUSSO, A. DOSIO, R. G. GRAVERSEN, J. SILLMANN, H. CARRAO, M. B. DUNBAR, A. SINGLETON,
P. MONTAGNA, P. BARBOLA, AND J. V. VOGT, Magnitude of extreme heat waves in present climate and
their projection in a warming world, Journal of Geophysical Research: Atmospheres, 119 (2014),
pp. 12,500–12,512.

[3] I. P. O. C. CHANGE, Climate change 2001 ipcc third assessment report, Intergovernamental Panel
on Climate Change Geneva, IPCC Secretariat, (2001).



[4] J. A. OROSA, M. COSTA, RODRÍGUEZ-FERNÁNDEZ, AND G. ROSHAN, Effect of climate change on outdoor
thermal comfort in humid climates, Journal of Environmental Health Science and Engineering,
12 (2014), p. 46


[5] U. FAYYAD, G. PIATETSKY-SHAPIRO, AND P. SMYTH, From data mining to knowledge discovery in
databases, AI magazine, 17 (1996), pp. 37–37.

[6] Ueda  Hideki Lucas  Projeto Clima e saúde : Análise de dados climáticos

[7] M. G. LAWRENCE, The Relationship between Relative Humidity and the Dewpoint Temperature in Moist
Air: A Simple Conversion and Applications, Bulletin of the American Meteorological Society, 86
(2005), pp. 225–234.
