// Restrição de ID para usuários

CREATE CONSTRAINT usuario_id_unico IF NOT EXISTS FOR (u:Usuário)
REQUIRE u.id IS UNIQUE;

// Cria uma restrição de id único para cada usuário SE NÃO JÁ EXISTIR, requerindo que a propriedade "id" seja única.

//  CRIAÇÃO DOS FILMES E SÉRIES 
//  COM SUAS PROPRIEDADES (título, data de lançamento, avaliação média na plataforma, duração/temporadas)

CREATE
(f:Filme {
    título: "A fuga",
    lançamento: 2021,
    `avaliação média`: 7.5,
    `duração em minutos`: 89
}),
(s:Série {
    título: "O Escritório",
    lançamento: 2007,
    `avaliação média`: 9,
    temporadas: 3
});
// ________________________________________

//  GÊNEROS 

CREATE
(g1:Gênero {nome: "ação"}),
(g2:Gênero {nome: "comédia"});

// ________________________________________

//  ATORES E SUAS PROPRIEDADES

CREATE
(a1:Ator {nome: "Matthew", idade: 26, nacionalidade: "Alemã"}),
(a2:Ator {nome: "Iryna", idade: 29, nacionalidade: "Ucraniana"}),
(a3:Ator {nome: "Scott", idade: 31, nacionalidade: "Britânica"}),
(a4:Ator {nome: "John", idade: 25, nacionalidade: "Britânica"});

// ________________________________________

//  DIRETORES E SUAS PROPRIEDADES

CREATE
(d1:Diretor {nome: "Polanski", idade: 48, nacionalidade: "Holandesa"}),
(d2:Diretor {nome: "Gervall", idade: 39, nacionalidade: "Francesa"});

// ________________________________________

//  USUÁRIOS E SUAS PROPRIEDADES

CREATE
(u1:Usuário {id: "U-001", nome: "Maria", idade: 27, nacionalidade: "Venezuelana"}),
(u2:Usuário {id: "U-002", nome: "Lucas", idade: 22, nacionalidade: "Brasileira"});

// ________________________________________

//  RELACIONAMENTOS 

// atuações
CREATE
(a1)-[:ACTED_IN]->(f),
(a2)-[:ACTED_IN]->(f),
(a2)-[:ACTED_IN]->(s),
(a3)-[:ACTED_IN]->(s),
(a4)-[:ACTED_IN]->(s);

// direções
CREATE
(d1)-[:DIRECTED]->(f),
(d2)-[:DIRECTED]->(s);

// gêneros
CREATE
(f)-[:IN_GENRE]->(g1),
(s)-[:IN_GENRE]->(g2);

// visualização dos usuários
CREATE
(u1)-[:WATCHED {`avaliação pessoal`: 4.4}]->(s),
(u1)-[:WATCHED {`avaliação pessoal`: 7.1}]->(f),
(u2)-[:WATCHED {`avaliação pessoal`: 7.8}]->(f);
