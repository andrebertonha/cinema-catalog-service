# Cinema Catalog Service
  api para consulta de cinemas filmes e sessoes por cidade
  <p> projeto para aprendizado, microservice integrado com movies_services </p>
  
### Instruções 
    + Faça clone deste repositório e do movies_service (siga as instruções do repositório https://github.com/andrebertonha/movies_service)
    + npm install
    
### Schema
```nodejs
     
 {
     _id: ObjectId("sasacsa85s7sdc7sd"),
     cidade: "Porto Alegre",
     uf: "RS",
     pais: "BR",
     cinemas: [
        {
           _id: ObjectId("68df5gd5g6ddf"),
           nome: "Cinemark Bourbon Ipiranga",
           salas: [
              {
                 nome: 1,
                 sessoes: [
                    {
                       data: ISODate("2018-06-01T09:00:00Z"),
                       idFilme: ObjectId("9ds68dsvdsvs876v"),
                       filme: "Vingadores: Guerra Infinita",
                       valor: 25.00,
                       assentos: [
                          { numero: 1, disponivel: true },
                          { numero: 2, disponivel: false },
                       ]
                    },
                    {
                       data: ISODate("2018-06-01T11:00:00Z"),
                       idFilme: ObjectId("9ds68dsvdsvs876v"),
                       filme: "Vingadores: Guerra Infinita",
                       valor: 25.00,
                       assentos: [
                          { numero: 1, disponivel: true },
                          { numero: 2, disponivel: true },
                       ]
                    }
                 ]
              }
           ]
        }
     ]
  }
     
```
     
 + Tenha certeza de estar usando idFilme correspondente aos filmes cadastrados no outro micro service 'movies_service'
 + Para testar as rotas e bateria de testes deve ser feito um insert seguindo o padrão do Schema (exemplo acima)
 + execute mongod --dbpath /pasta-do-seu-microservice/data --port 27018 em seu terminal a partir do diretório bin do MongoDB
 + Com o container movie_service rodando:
    + npm start
    + npm test
