# Network Analysis on Twitter

Esse reposítório consiste na coleta de tweets referentes ao assunto da Tensão entre Rússia e Ucrânia onde uma rede de retweets foi construída e analisada para avaliar quais são os usuários que possuem maior número de retweets em suas postagens e quais usuários realizam mais retweets sobre o assunto.

Para executar e/ou adaptar o código, é necessário:

* Criar uma conta de Desenvolvedor no Twitter e requisitar acesso à API;
* Python;
* Twython para executar a API em Python;
* Pandas para construir DataFrames;
* Itertools para realizar a coleta iterativa dos Tweets;
* NetworkX para escrever o grafo;
* Gephi para visualizar, analisar e realizar o deploy do grafo em questão.

Sobre o código, é necessário incluir suas próprias chaves API. Além disso, dada a limitação de coleta de tweets sendo de no máximo 7 dias anteriores, é necessário adaptar as datas na parte que realiza a coleta. A pesquisa no objeto twitter.search pode ser modificado para procurar assuntos diferentes.

O código consiste em uma coleta de tweets sobre o assunto em questão usando uma lógica booleana na pesquisa (nesse caso, "Russia AND Ukraine" foi utilizado). 
Dado o limite de requisições a cada 15 minutos, o código possui um tempo de sleep(900), para superar a barreira de limitação.
Por fins de alcançar um maior número de tweets, foi determinado utilizar um range de datas para limitar a busca.
Os tweets coletados passam por dois filtros: um para recuperar apenas os retweets, e outro para eliminar resultados duplicados.

É possível utilizar mais funções dentro do Pandas e do NetworkX para realizar análises mais profundas.

![image](https://user-images.githubusercontent.com/30414428/154771439-c423d4b5-868e-42d6-acbe-d933d2d7d951.png)


Para visualizar o grafo no Gephi, é necessário salvar o grafo construído no código.

Por fim, para executar o deploy do grafo gerado via Gephi, é preciso executar o seguinte comando

```
python -m http.server
```
![image](https://user-images.githubusercontent.com/30414428/154771407-1ac4868d-68ff-46c3-85ad-5b853b3e43aa.png)

Código e projeto foi baseado no seguinte repositório de Ivanocvitch Silva
https://github.com/ivanovitchm/network_analysis_2021
