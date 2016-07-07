# Teste_API
Small Test Project

  Esta pequena API consiste em trabalhar dados adquiridos através de pedidos feitos a uma plataforma. A plataforma OST (One.Stop.Transport) à qual fazemos pedidos, fornece-nos dados estáticos de transportes públicos de funcionamento previsível.
  
  Como objetivo de tratamento de dados há dois tipos de requests. Um sem a Localização da API e outro com. A sem localização devolve-nos uma lista de pontos de referencia, no outro caso é nos devolvido apenas os pontos de referencia num certo range à posição da API.
  
  
  
# Aplicação (implementação ainda incompleta)

  Primeiro tem um menu simples, nome da API e botão “List” para passar à listagem de todos os pontos de acesso. Clicando no botão passamos a um novo menu. Este contem dois botões e uma lista de posições. Um dos botões “show all” mostra uma lista de pontos de referencia sem localização da API, o outro botão “on range”, mostra a lista de pontos de acesso dentro do range. É utilizado como default dado o valor de range=10 como fornecido. A Lista de posições ainda não esta trabalhada e apresenta a informação bruta fornecida pelo request feito. Botão “on range” ainda não funcional tendo um erro de indentação quando tenta saber a posição da API. Nomeadamente quando se faz o pedido ao “locationListener”, este pedido foi experimentado tanto com “NETWORK_PROVIDER” como “GPS_PROVIDER”.



# Como implementado e como complementar

  Em primeiro lugar foi necessário registar na plataforma da OST e criar uma chave para ter acesso developer aos dados da plataforma. Tendo esta chave foi modificado o url de request.
  
  São feitos dois tipos de pedidos, consoante o botão carregado. Um sem localização, em que apenas acrescentamos a chave de developer. E outro que alem de ter a chave de acesso, é adicionado também a localização da API e o range.
  
  Depois de obtido o request, seria tratado o resultado e listado por nome e respetivas coordenadas. Ao clicarmos neste botão da lista seria mostrado uma descrição adicional sobre o lugar.  Quando a lista tivesse nu mínimo um elemento seria disponibilizado um terceiro botão, invisível a priori, que nos fornecia um mapa e respetivas localizações da lista. Para este mapa utilizaríamos a libraria GoogleMap, onde seria adicionada uma descrição com o nome do local em cada “alfinete” marcado no mapa. Posição dos “alfinetes” marcado com as coordenadas de cada local. No caso de usarmos a opção sem localização todos os alfinetes teriam a mesma cor e seria usado um zoom de aproximação ao mapa standart. No caso com localização, a posição actual teria uma cor e as posições em range uma cor diferente. O zoom neste caso seria usado a aproximar a posição atual.
  
