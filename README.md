# Cinema Catalog Service
  api para consulta de cinemas filmes e sessoes por cidade
  <p> projeto para aprendizado, microservice integrado com movies_services </p>
  
### Instruções 
  + Faça clone deste repositório e do movies_service 
  + siga as instruções do repositório: https://github.com/andrebertonha/movies_service
  + npm install
    
### Schema
```nodejs     
 {
    cidade: String,
    uf: String,
    pais: String,
    cinemas: [
        {
            nome: String,
            salas: [
                {
                    nome: String,
                    sessoes: [
                        {
                            data: Date,
                            idFilme: ObjectId,
                            filme: String,
                            valor: Number,
                            assentos: [
                                {
                                    numero: Number,
                                    disponivel: Boolean
                                }
                            ]
                        }
                    ]
                }
            ]
        }
    ],
}     
```     
 + Tenha certeza de estar usando idFilme correspondente aos filmes cadastrados no outro micro service 'movies_service'
 + Para testar as rotas e bateria de testes deve ser feito um insert seguindo o padrão do Schema (exemplo acima)
 + execute mongod --dbpath /pasta-do-seu-microservice/data --port 27018 em seu terminal a partir do diretório bin do MongoDB
 + Com o container movie_service rodando:
    + npm start
    + npm test
    
   <p><b>créditos</b>: LuizTools https://www.luiztools.com.br/post/arquitetura-de-micro-servicos-em-node-js-mongodb-2/ </p>
