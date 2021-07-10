<h2>Catálogo de Jogos - API ASP.NET</h2>

Este API foi desenvolvido em aula proporcionada pela Digital Innovation One, através do desenvolvedor Thiago Campos de Oliveira.

Em relação ao projeto desenvolvido em aula, fiz os seguintes acréscimos:

- ---

Procurei retirar do projeto algumas particularidades que não se referiam ao Http e comunicação com o Banco de Dados, além da manutenção do Swagger para teste das funcionalidades da API, como forma de exercitar e desenvolver o núcleo mais importante de uma API em C# com o ASP.NET.

Criei a tabela a seguir no SQL Server:

Nome da Coluna		Tipo de Dados		Permitir Nulos

Id									uniqueidentifier	Não
Nome							nvarchar(50)		   Não
Produtora					 nvarchar(50)		  Não
Preco							 decimal(18, 2)	     Não
Avaliacao					  int						     Não

Conectei o banco de Dados a API, para poder verificar e desenvolver com funcionamento integral.

A coluna Avaliacao for acrescentada ao projeto. Ela permite avaliar o catálogo de jogos com 1 a 5 estrelas.

Fiz também diversas pequenas mudanças para possibilitar rodar o programa (havia sido desenvolvido em versão anterior do .NET).

Ao acrescentar a coluna acima, foi necessária modificação em quase todas as classes e interfaces do projeto.

Também acrescentei ao controller o método [HttpGet("{avaliacao}")] para permitir a busca por avaliação. Por exemplo, quais itens do catálogo receberam 3 estrelas. Esta mudança também permitiu exercitar o desenvolvimento de diversos métodos na API, desde a criação do httpGet, passando pela busca no Banco de Dados e finalizando com o retorno ao cliente.

Vários desafios foram superados, com a prática ou aquisição de um conjunto de conhecimentos: SQL Server (criação de tabela, conexão com o Visual Studio e desenvolvimento dos métodos SQL), entendimento do funcionamento do Swagger, métodos de retorno da classe ControllerBase e criação de rotas Http.

----------------

* Visual Studio 2019 com todas as dependências;
* SQL Server Database, com Tabela acima.
* .NET 5.0.
