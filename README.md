 # Projeto < Clima e saúde>

## Project < Climatic and Healthy>

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

Ruben Hernan Alcivar Ullon


## Video do projeto

https://drive.google.com/file/d/162rskPRvc0Ap1H90L5hTd58whU9q7zAJ/view?usp=sharing


## 1. Introdução e motivação


Um tema muito recorrente atualmente são as mudanças climáticas que o mundo vem sofrendo ao longo do tempo. Aquecimento global, efeito estufa e derretimento de geleiras
polares são efeitos associados ao tema em questão.
A atividade humana está  diretamente ligada á essas alterações climáticas aumentando a concentração de gases tóxicos como dióxido de carbono na atmosfera devido a queima de combustíveis fósseis e de florestas  contribuindo para o aumento do efeito estufa.
Por outro lado essas mudanças climáticas afetam diretamente a saúde das pessoas como por exemplo em períodos de maior estresse térmico (longos períodos com temperaturas muito baixas ou muito altas) ou acidentes naturais como enchentes e tempestades e também de forma indireta afetando a qualidade do ar , da água , interferindo nos vetores de transmissão de doenças [4].
Partindo desse principio que as mudanças climáticas afetam diretamente a saúde humana o presente projeto pretende calcular três indicadores principais através das medidas coletadas de temperatura e umidade : Humidex, ondas de calor, ondas de frio.



![Figura 1](https://github.com/hernanullon/ClimaticHealthy/blob/master/ambiente%20.png)


                                       Figura 1 - Ambiente





Na figura 2 é possível visualizar os principais problemas ocasionados pelas ondas de calor 


![Figura 2](https://github.com/hernanullon/ClimaticHealthy/blob/master/ilhas%20de%20calor.jpg)



                     Figura 2 - Problemas ocasionados pela presença das ilhas de calor
                     
Partindo deste contexto este projeto utiliza duas bases de dados, a base principal do projeto foi cedida pelo Centro de Pesquisas Meteorológicas e Climáticas aplicada a Agricultura (Cepagri), a Cepagri coleta dados de temperatura, umidade, direção do vento, intensidade de radição solar através de uma estação meteorológica que fica localizada dentro do Campus da Universidade Estadual de Campinas (Unicamp), na cidade de Campinas SP .
E uma segunda base de dados disponível no site da  Companhia Ambiental do Estado de São Paulo (Cetesb) também foi utilizada para comparar os dados de temperatura e umidade nos meses de março a maio de 2020 com os dados referentes a estas mesmas variáveis no periodo de 2017 a 2018.

A escolha do período de janeiro a maio de 2020 para analisar  se houve alterações climáticas, justifica-se  em virtude do isolamento social devido a pandemia causada pelo Covid 19.
Após a escolha dos datasets para o projeto foram estudadas e aplicadas técnicas para limpeza destes dados e por fim, aplicou -se a metodologia KDD (Knowledge Discovery in Databases – KDD) para obter conhecimento a partir dos dados (tais como níveis de temperatura e umidade ) e assim  calcular três principais indicadores de condições climáticas: Humidex, ilhas de calor, ilhas de frio.

A partir do cálculo destes indicadores realizar a classificação (clusterização) dos dados utilizados para se identificar condições climáticas saudáveis a partir de dados de temperatura e umidade e assim poder fazer recomendações para as pessoas dos cuidados que devem ser considerados para evitar que condições climáticas desfavoráveis como a presença de ondas de calor , ondas de frio e umidade relativa do ar baixa afetem a saúde das pessoas.



## 2. Pergunta de pesquisa

É possível a identificação de condições climáticas saudáveis  a  partir de dados de temperatura e umidade ?

## 3. Objetivos do projeto

* Realizar a análise exploratória dos dados de temperatura e umidade da base de dados do Cepagri e da Cetesb utilizando a técnica KDD

* Cálculo dos indicadores como humidex, ondas de calor, ondas de frio.

* Realizar a clusterização dos dados de acordo com os indicadores calculados e assim poder fazer recomendações de hábitos saudáveis para os dias de condições climáticas 
desfavoráveis.


## 4. Recursos e métodos


* 4.1. Bases de dados

|Base de dados   |Endereço na web   |Resumo e descrição de uso    |
|---|---|---|
| Base 1 - Cepagri da Unicamp  |  |Essa foi a principal base de dados utilizada no projeto, nessa base foram aplicadas técnicas para completar os dados faltantes, foram realizados cálculos para encontrar os indicadores humidex, onda de calor, onda de frio.   |
| Base 2  - Cetesb  |https://cetesb.sp.gov.br/ar/dados-horarios/  | Esta base de dados foi utilizada para efeitos de comparações entre os meses de janeiro  maio de 2020  e o mesmo período do ano passado  |


* 4.2 Ferramentas


| Ferramenta  | Endereço web  | Descrição de uso  |
|---|---|---|
|   |   |   |
|   |   |   |

* 4.3. Metodologia

A metodologia adotada neste projeto foi a Knowledge Discovery in Data (KDD) , que é a descoberta de conhecimento a partir de uma base de dados e pode ser ilustrada na figura 3

![Figura 3](https://github.com/hernanullon/ClimaticHealthy/blob/master/Processo%20KDD%20.jpg)


                                 Figura 3 - Processo de estração do conhecimento a partir do processo KDD 

Etapa 1 -  Entendimento do problema - Nesta etapa o objetivo principal é entender o motivo que justifica a escolha do processo KDD, portanto a pergunta de pesquisa é quem guiará o processo  do ponto de vista do que ou quem utilizará esse conhecimento. Neste projeto esta etapa foi cumprida por meio de reuniões da dupla e pesquisas na literatura para encontrar bases teóricas sobre os problemas ocasionados pelas mudanças climáticas na saúde humana.

Etapa 2 - Selection (Seleção)  - Nesta etapa foi feita a seleção do período do dataset que seria utilizado para realizar a análise.
Para o dataset fornecido pela Cepagri foram  escolhidos os meses de janeiro a dezembro para os anos de 2017 e 2018 , já para o dataset da Cetesb foram escolhido os meses de janeiro, fevereiro, março, abril e maio e as variáveis selecionadas em ambas as bases  foram temperatura e umidade


Etapa 3 - Preprocess - Após a etapa de seleção dos datasets foi realizado um pré processamento utilizando a técnica de interpolação dos valores no ano de 2017 e 2018 para completar os valores faltantes de temperatura e umidade da base fornecida
pelo Cepagri.
Foi implementado um algoritmo para apresentar a data em um formato adequado como por exemplo 26/06/2020 já que no dataset o formato da data era Dia Juliano                       103025 non-null int64.
Foi plotado em um gráfico as variaveis de temperatura e umidade para visualização da distribuição destas variáveis, foram cálculadas algumas estatisticas dos dados como média, desvio padrão.

Etapa 4 - Transformation - 
Nesta etapa foi realizada uma transformação dos dados, realizou -se o cálculo do indicador Humidex, e a partir desse cálculo foi possível classificar a condição climática em função desse indicador como : Confortable (confortável ) , some disconfort (algum desconforto)

O humidex foi proposto em 2016 e é descrito como uma métrica do desconforto térmico de uma pessoa em uma determinada condição de temperatura e umidade relativa do ar .

O humidex é definido pela fórmula:
H = T + (0:555:[E - 10]); (2)
onde T é a temperatura em Graus Celsius e E é a pressão de vapor de água em milibars.
A pressão de vapor é descrita pela fórmula:
E = 6:11.e^5417:7530:( 1 /273.16 -  1 /td+ 273.16)


água para que haja condensação em unidades de graus Celsius.
Utilizamos uma aproximação para o ponto de orvalho (td) que leva em consideração a temperatura e
a umidade relativa, descrita em [9], conforme apresentado na equação (4).
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



 
 
 





Etapa 5 - Data mining - Nesta etapa após realizar o pré processamento e a transformação dos dados dos datasets colocando esses dados num formato mais adequado para realizar a análise, foi criado atributos para clusterizar os dados de acordo com cada um dos  indicadores calculados humidex, ondas de frio e ondas de calor.
Após clusterizar os dados de temperatura e umidade, foi realizado o treinamento do aprendizado de máquina com 70 % dos dados e 30 % dos dados foi usado para testar a aprendizagem de máquina.

Etapa 6 - Knowledge Discovery - Nesta etapa utilizou -se  o conhecimento obtido a partir do dataset para classificar os dados de temperatura e umidade conforme o aprendizado na etapa de data mining.

## 5. Detalhamento do projeto

## 6. Evolução do projeto

Inicialmente  nossa intenção era de realizar o projeto com dados de poluição do ar atmosférico e classificar o ar de acordo com a quantidade de polentes no ar, porém diante da dificuldade em achar datasets com esse tipo de dados, optamos por trabalhar com dados de temperatura e umidade, uma vez que estão disponíveis pela Cepagri e no site da Cetesb.

## 7. Resultados e discussões

## 8. Conclusões

## 9. Trabalhos futuros

## 10.  Referências

[1] As cidades que queremos Disponível em : https://www.isglobal.org/es/

[2] J. L. GEIRINHAS, R. M. TRIGO, R. LIBONATI, AND L. F. PERES, Climatic Characterization of Heat
Waves in Brazil, Anuário do Instituto de Geociências - UFRJ, 41 (2018), pp. 333–350.
Climate change and human health - risks and responses. 
Disponível em < https://apps.who.int/iris/bitstream/handle/10665/44133/9789241598187_eng.pdf;jsessionid=F45966ED878C58D6CC7129FFE87DF3B0?sequence=1>

[3] S. RUSSO, A. DOSIO, R. G. GRAVERSEN, J. SILLMANN, H. CARRAO, M. B. DUNBAR, A. SINGLETON,
P. MONTAGNA, P. BARBOLA, AND J. V. VOGT, Magnitude of extreme heat waves in present climate and
their projection in a warming world, Journal of Geophysical Research: Atmospheres, 119 (2014),
pp. 12,500–12,512.

[4] I. P. O. C. CHANGE, Climate change 2001 ipcc third assessment report, Intergovernamental Panel
on Climate Change Geneva, IPCC Secretariat, (2001).

[5] W. H. ORGANIZATION, ed., Climate Change and Human Health - Risks and Responses, Genève, 2004.
OCLC: 254297040.

[6] J. A. OROSA, M. COSTA, RODRÍGUEZ-FERNÁNDEZ, AND G. ROSHAN, Effect of climate change on outdoor
thermal comfort in humid climates, Journal of Environmental Health Science and Engineering,
12 (2014), p. 46

[7] I. P. O. C. CHANGE, Climate change 2001 ipcc third assessment report, Intergovernamental Panel
on Climate Change Geneva, IPCC Secretariat, (2001).

[8] U. FAYYAD, G. PIATETSKY-SHAPIRO, AND P. SMYTH, From data mining to knowledge discovery in
databases, AI magazine, 17 (1996), pp. 37–37.

[9] Ueda  Hideki Lucas  Projeto Clima e saúde : Análise de dados climáticos


