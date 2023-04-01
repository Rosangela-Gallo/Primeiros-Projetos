

<h1 align="center"> Projeto Aprimoramento:  </h1>

### 

### Uma Análise dos dados de imóveis do Airbnb Nova York

O Objetivo é aprimorar as técnicas de ETL, pipeline, big data, e DataViz.

O projeto foi construído com a ferramenta Google Colab e utilizando principalmente a linguagem python com pandas e pyspark  e teve sua base e finalização disponibilizada na plataforma GCP utilizando o CloudSorage, o BigQuery e o DataStudio.



Descrições de arquivo

Os dados são referentes a Airbnb - Empresa que disponibiliza uma plataforma estabelecendo uma ligação entre pessoas que querem viajar e se hospedar, com anfitriões que desejam alugar seus imóveis de maneira prática.

Os dados são disponibilizados de forma aberta e para esta análise utilizaremos o arquivo 4.csv que contém os dados da plataforma Airbnb contendo 48896 registros com 16 colunas, traz informações de imóveis para alugar em nova york; Todos os dados estão no idioma inglês e traz dados até 2019.

**![](https://lh6.googleusercontent.com/E3Nl-1Uib9RQNxvpWXdQysyTFdfsSphtcqDzA6c31Zv_-ham7DArVls9tmqQwRuA51PHZcRdHXARW7FuG8ggSqthySdvVWh6Qiuux34W_nBXwbUDVLjToX_G2JEy39XiaXD5x03CGcRu5ZJJQKLe4Q=s2048)**

Como primeira etapa deste projeto é importante entender o que são estes dados e como estão estruturados em cada uma das colunas do arquivo.



id - número de id gerado para identificar o imóvel;

name - nome da propriedade anunciada;

host_id - número de id do proprietário (anfitrião) da propriedade;

host_name - nome do anfitrião;

neighbourhood_group - esta coluna não contém nenhum valor válido;

neighbourhood - nome do bairro;

latitude - coordenada da latitude da propriedade;

longitude - coordenada da longitude da propriedade;

room_type - informa o tipo de quarto que é oferecido;

price - preço para alugar o imóvel;

minimum_nights - quantidade mínima de noites para reservar;

number_of_reviews - número de reviews que a propriedade possui;

last_review - data do último review;

reviews_per_month - quantidade de reviews por mês;

calculated_host_listings_count - quantidade de imóveis do mesmo anfitrião;

availability_365 - número de dias de disponibilidade dentro de 365 dias.

Para trabalhar estes dados utilizei a IDE Google Colab, trazendo um Jupyter Notebook com todos os códigos seguindo as etapas de ETL para análise de dados dos imóveis disponibilizados pela plataforma.

**![](https://lh6.googleusercontent.com/7NqrGni0JLmScG2eIuHnBt2jk3COYLZn7FvmoZAiZ30p7y_MXDAjFk90eK2LEifilo3W8Oh-KS5D8nZ-cxdeZHV4qeacM5GdxAl9lQvi7KeQo6Eu6TvKBKTe2S5KuXscLdPphCR5XQ539ziIqvutXA=s2048)**



caminho - Tratar os dados de forma que facilite o entendimento dos dados

Então eu fiz a tradução (do inglês para pt-br) 

**![](https://lh5.googleusercontent.com/7uXEIjDQmazEYTmcq1s-lYngNnGGnYNrJIr5A23bD8SnTZDRcgzsZDAEnptUZAwWHtYaIHt7pbT3ANxoRrtq8p7PvrkAWxNUPYgjAiOHfdv5dsR2WypbbLpPp3ofnTKCMmUEnX0XMyApR85y7vlAqA=s2048)  

AUTOMATIZAÇÃO

![](https://lh5.googleusercontent.com/gQ673zEk983Q3c9ABn-xYvE3M_-LAETMgnB8QXFX3yKwU2o2imJ7DcvtEtp9tb_i9gKAdYIg3CfDunpKR8QUXBOrY6WFzO1rJzBXHds8c5fZX3RWrTFyQylt9UbRiSmi2ngobbf83TmjLVC7c_S97g=s2048)**

e limpeza de inconsistências e reorganizei esses dados através de filtros de forma que se possa extrair detalhes com dados mais precisos destas informações.

**

RESULTADO DO TRATAMENTO (antes e depois)

![](https://lh3.googleusercontent.com/oy7RshSKfUQBrLZ8Cx6dj5nshMDdAsqspP49M2L9NAwSbFqALztWHgxGM08uFNFetdI3x06FjYu_neGs9LRlgdJF-P0V3_QDJL78gA0OJZN5SndwqfwV97t9BWds1_pWUR0nIeW0D6sx3qv9gXIpXw=s2048)![](https://lh5.googleusercontent.com/yWTgIsNZLtaztiTJdd0tVBn5tifl3rnqlG8KQsSGlyaSOsFeGhkNGJIbtgq6wVg6c3bcu5hQryDm8vZepgEP_QCEdVA7iCKyQxk0w4vf4p9iN-Gi2GHIrA5OUFIZlDmlGf6t-i6uSGRMAbeb0DFl2g=s2048)

******



### Critérios:

Para exclusão dos dados: 

- Não impactar na redução de dados  

- Apenas  colunas irrelevantes aos insights

- Não causar novas inconsistências 

Para inclusão dos dados: 

- Permitir que dados importantes façam parte dos cálculos 

- criar dados cruzados e relevantes
  
  
  
  

Insights  -  vamos descobrir informações como:

Qual a média dos preços de aluguel?

Qual o tipo de imóvel mais alugado?

Qual a localidade mais cara?

Qual a média do mínimo de noites para aluguel?

**

ONDE TEM MAIS IMÓVEIS PRA ALUGAR ? - PLOTADO EM PANDAS

![](https://lh5.googleusercontent.com/qthsNvuVWGcwcBxId-at9i61QCYkFX6ILSaAw4OqHrf8crkSoI0DET_9U77JC_EXG0Uwz2O7jD40keGepggqq3TWJqPMsTJyMUV76qAvBawVL8jhzUqKJB8mh6A91CLNxUxYPtRa_TbCtMMTVT6Szg=s2048)![](https://lh6.googleusercontent.com/xbqRicakHFRKRSTu1NLXI6J7XVsjEjRSmaYFLaWKs0kpO1Gaq38BfMISkTjHXblPLkKUcAvi94lbLMhFRVAjduBvb2m6voF9Zep5VsLa9jQBsC_pXAHwgk8HBfBp8Hf4vd0K9viEDFy_5Dz5ZRL5Zg=s2048)  

dbairro

Rossville                1

Silver Lake              1

Richmondtown             1

Willowbrook              1

Fort Wadsworth           1

                      ... 

Hell's Kitchen        1446

Bushwick              1449

Harlem                1734

Williamsburg          2052

Bedford-Stuyvesant    2482

**

**

PYSPARK

![](https://lh3.googleusercontent.com/oEluAJuT80IDJP6NBmbsTnsFbDFCh_CgXYOw5oFi7j-I_JfCgGcLyNAy4K3WTfCZ_B00t44TpeA2WW92nd1n7P9KDER38Lzwau_FZ4xKOuiLaKoc9vxEN_wKak_7uyrTS1Fa7OcfqZto3F5Vkfm1EA=s2048)

**![](https://lh4.googleusercontent.com/h-cxc1zD_b6ehieCcMs4Arw7nCMqL3QfqA-dRMgIR_JC1riNhuClyK9wdESrcsjlZdO94SEjhoRGE4LKpDmgvkW9kLVCeqU2Ndrt9GJXmFhOsTMguPJ0G1zltJUBUgmbrPJ6PkGqEbhvw8VS6vCXsg=s2048)**

**![](https://lh5.googleusercontent.com/pNJUC5ZBeOzQC6s6XTuS2SX5FIxOBKnIrxIWYYuBjm4ueJOaxgfYq-01cijkcpmat9ZkcZ7QzuNnS8k4ZxtOumi69QB_i_WzLXfUyTS_ruQIxPnpUq4iAVcdlFL6L0Sq1niu_9Gf5GFB5bG0er4vYw=s2048)![](https://lh5.googleusercontent.com/Wp5IP3yJq62qNszkJudGKz8E-pTtX2FQhr1qLz_3OtC31Qdta1nepJA3Bn5qFMu9HqhTmoAPMCJeCnHTzTHHuxl0IeRbZHDmJnp4guPv1Iiz9S3SuyRsfcGlDnajCPTJI9OJ7P4n0U9smDGRJf7Yqw=s2048)****![](https://lh5.googleusercontent.com/bglvVLHaDjeWiqF__0t9dgKZqghCDHvY8dUl1b9AcJuQre83GtG8ovbSq4a-f5tBAd4zbNuD18XPV2EKdK9PkxtjfNdX4E9DzPPQ7Y80XSDpmEczZ_E9bhsS1QZZ9mYEi2cIdYArKSkwDkguG7UEEA=s48)****

**![](https://lh4.googleusercontent.com/Q2TEUAxsLdPB726VihI4BnoYHu1Enzwo3VStlDKvxAg_F9oW116bhQJ_iW_R_Eu4VGBheXY8VnaSRdNXB0oRwNYfr8Ptjw3ODJCfjpB4wuHJhuWSGsP1qUADjQd025xNN1Av2xki5V1_GHmynqY0Pg=s2048)![](https://lh3.googleusercontent.com/suSJNFqaz9xv1nnqRJySWZJqFEnifas6nsdh4L4I34DhXgTQE7VgRdakjwuxBcdDG4APkHZ3Rdij43aJr0YmFo5XIKjUed_LsQrPT5cZ6-eag8D0ATvc4tiKPkSdB0_n815FKtFOi_GJJsQctTPjlA=s2048)**

![0d4ebb9a-51af-42bf-95f7-c82c74f9003e](file:///C:/Users/rosan/Pictures/Typedown/0d4ebb9a-51af-42bf-95f7-c82c74f9003e.png)



Este projeto requer o Python 3.xe  com as seguintes bibliotecas instaladas:



pandas, NumPy, translator

matplotlib - para imprimir alguns gráficos iniciais

pyspark - para a filtragem dos dados

SQL - BigQuery - gerar dados específicos para os gráficos

DataStudio - construção de gráficos para visualização dos dados

O código foi desenvolvido no Google COLAB e nele deixei documentado os passos para implementação em python. 







Autores e Agradecimentos



Crédito - Rosangela Gallo

Agradecimento -  Airbnb pelos dados abertos.
