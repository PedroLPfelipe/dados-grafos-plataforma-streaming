# dados-grafos-plataforma-streaming
Este repositório contém a solução de um desafio de código do bootcamp da DIO focado em modelagem de dados em grafos utilizando Neo4j. O projeto demonstra a construção de um modelo de dados em grafo para representar informações de uma plataforma de streaming, explorando como entidades e relacionamentos podem ser estruturados e consultados dentro do ecossistema do Neo4j.

## REQUISITOS DO DESAFIO
**- Entidades (nós): User, Movie, Series, Genre, Actor, Director.**

**- Conexões (relacionamentos): WATCHED (com propriedade rating/avaliação), ACTED_IN, DIRECTED, IN_GENRE.**

## RASCUNHO DA MODELO
Modelagem do grafo com a ferramenta [Arrows App](https://arrows.app/)

![image alt](https://github.com/PedroLPfelipe/dados-grafos-plataforma-streaming/blob/5a1af2d8c3260fb76398c2398e18bb126dd1eb9e/grafo_plataforma_streaming.png)

Nesse modelo, **filmes e séries são o núcleo do grafo**, enquanto outras entidades se conectam a eles através de relações específicas.
Principais tipos de nós (entidades)

## AS CATEGORIAS DE NÓS:

● Filme – representa um filme com propriedades como título, ano de lançamento, avaliação média e duração.

● Série – representa uma série com propriedades como título, lançamento, avaliação e número de temporadas.

● Ator – pessoas que atuaram em filmes ou séries.

● Diretor – responsáveis pela direção das produções.

● Usuário – pessoas que assistiram aos conteúdos e forneceram avaliações pessoais.

● Gênero – categoria do conteúdo, como ação ou comédia.

## TIPOS DE RELACIONAMENTOS:

● ACTED_IN - conecta atores aos filmes ou séries em que atuaram

● DIRECTED - conecta diretores às produções que dirigiram

● IN_GENRE - associa filmes ou séries a seus gêneros

● WATCHED - liga usuários aos conteúdos que assistiram, incluindo uma avaliação pessoal

## Neo4j aura

A plataforma [Neo4j aura](https://neo4j.com) permite navegar facilmente entre conexões, como:

● encontrar todos os atores de uma série

● descobrir quais usuários assistiram ao mesmo filme

● identificar conteúdos de um determinado gênero
