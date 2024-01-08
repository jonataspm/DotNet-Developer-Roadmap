# Roteiro do Desenvolvedor .NET 2024.

Este é um guia passo a passo para se tornar um Engenheiro .NET, com links para recursos de aprendizado relevantes.

Se você deseja saber mais sobre as tecnologias .NET, certifique-se de se inscrever na [minha newsletter](https://newsletter.techworld-with-milan.com/).

## Aviso Legal

> Este roteiro tem o objetivo de fornecer uma ideia sobre o panorama. O roteiro o guiará se você precisar de esclarecimentos sobre o que aprender a seguir, em vez de incentivá-lo a escolher o que é popular e moderno. É útil adquirir uma compreensão de por que uma ferramenta seria mais adequada para alguns casos do que a outra, lembrando que popular e moderno nem sempre significa o mais adequado para o trabalho.

## Dê uma Estrela! :star:

Se você gostar ou estiver usando este projeto para aprender ou iniciar sua solução, por favor, dê uma estrela. Obrigado!

## Roteiro (por nível de experiência)

Observe que, por nível de experiência, significa:

- **Júnior**: Conceitos básicos
- **Médio**: Conceitos avançados
- **Sênior**: Conceitos especializados

![Roteiro](NET%20Roadmap.png)

Baixe a [versão em PDF](NET%20Roadmap.pdf).

## Versão Minimalista

Abaixo você encontra uma versão mínima que todo desenvolvedor júnior .NET precisa conhecer, com materiais de aprendizado incluídos e clicáveis na versão em PDF.

![Roteiro](NET%20Developer%20Roadmap%202024.%20Minimal.png)

Baixe a [versão em PDF](NET%20Developer%20Roadmap%202024.%20Minimal.pdf).

## Sumário

- [Compreensão do ecossistema .NET](#compreensão-do-ecossistema-net)
  - [Runtimes .NET](#runtimes-net)
    - [Framework .NET](#framework-net)
    - [Core .NET](#core-net)
    - [O .NET Único - .NET 5](#o-net-único---net-5)
    - [O atual - .NET 8](#o-atual---net-8)
  - [Padrão .NET](#padrão-net)
- [Recursos de Aprendizado](#recursos-de-aprendizado)
  - [1. C#](#1-c)
  - [2. Habilidades Gerais de Desenvolvimento](#2-habilidades-gerais-de-desenvolvimento)
  - [3. ASP.NET Core](#3-aspnet-core)
  - [4. .NET do Lado do Cliente](#4-net-do-lado-do-cliente)
  - [5. Bancos de Dados](#5-bancos-de-dados)
  - [6. ORM](#6-orm)
  - [7. Caching](#7-caching)
  - [8. Logging](#8-logging)
  - [9. Comunicação](#9-comunicação)
  - [10. Tarefas em Segundo Plano](#10-tarefas-em-segundo-plano)
  - [11. Mapeamento de Objetos](#11-mapeamento-de-objetos)
  - [12. Testes](#12-testes)
  - [13. Observabilidade](#13-observabilidade)
  - [15. Containerização](#15-containerização)
  - [14. Nuvem](#16-nuvem)
  - [15. Integração Contínua e Entrega (CI/CD)](#17-integração-contínua--entrega-cicd)
  - [16. Bibliotecas .NET](#18-bibliotecas-net)
  - [Considerações Adicionais](#considerações-adicionais)
    - [Melhores Práticas de Desempenho](#melhores-práticas-de-desempenho)
    - [Perfilamento e Diagnósticos](#perfilamento-e-diagnósticos)
    - [Melhores Práticas de Segurança](#melhores-práticas-de-segurança)
  - [Recursos Adicionais de Aprendizado](#recursos-adicionais-de-aprendizado)
    - [Livros](#livros)
    - [Canais do YouTube](#canais-do-youtube)
    - [Blogs](#blogs)
    - [Podcasts](#podcasts)
    - [Outros Criadores de Conteúdo .NET](#outros-criadores-de-conteúdo-net)
- [Ferramentas](#ferramentas)

## Compreensão do ecossistema .NET

Antes de entrar em detalhes, é necessário ter uma compreensão sólida do **Ecossistema .NET**. Aqui estão alguns pontos que você deve entender:

## Runtimes .NET

Nesta seção, examinaremos os principais runtimes .NET. Consideramos runtime .NET qualquer coisa que implemente o **[Padrão ECMA-335 para o .NET](https://github.com/dotnet/coreclr/blob/master/Documentation/project-docs/dotnet-standards.md)**.

### Framework .NET

O [.NET Framework](https://dotnet.microsoft.com/en-us/download/dotnet-framework) é um framework de desenvolvimento de software para construir e executar aplicativos no Windows. O .NET Framework consiste no Common Language Runtime (CLR), na Biblioteca de Classes do .NET Framework e nas cargas de trabalho da aplicação (WPF, Windows Forms e ASP.NET). O CLR faz parte de uma infraestrutura compartilhada que executa código, realiza just-in-time compilation (C#, VB.NET, F#), etc. O código que o CLR gerencia é chamado de código gerenciado. O código é compilado para a Linguagem Intermediária Comum (CIL) e armazenado em assemblies (com extensão .exe ou .dll). Quando um aplicativo é executado, o CLR pega um assembly e usa um compilador just-in-time (JIT) para transpilar o código de máquina em código que pode ser executado em uma arquitetura de computador específica.

É possível usá-lo tanto para desenvolvimento desktop quanto web, mas é limitado ao desenvolvimento no Windows e vem pré-instalado no Windows.

### Core .NET

O [.NET Core](https://dotnet.microsoft.com/en-us/download) é um dos runtimes no Ecossistema .NET. Foi lançado em 2016 e é [código aberto](https://github.com/dotnet/core). Não representa uma nova versão do .NET Framework e não o substituirá. É uma versão totalmente independente, construída para permitir a capacidade de desenvolvimento cross-platform. O .NET Core consiste em um App Host (dotnet.exe) que executa o CLR e a Biblioteca. Ele possui um tempo de execução de linguagem comum (CoreCLR) e a Biblioteca de Classes do .NET Core. Ele suporta diferentes cargas de trabalho de aplicativos, como ASP.NET Core (MVC e API), aplicativos de console e UWP (atualmente).

O .NET Core pode ser executado em diferentes plataformas: Windows Client, Server, IoT, Linux, Ubuntu, FreeBSD, Tizen e Mac OSX, e pode ser instalado lado a lado de diferentes versões por máquina ou usuário.

### O Único .NET - .NET 5

O [.NET 5](https://dotnet.microsoft.com/en-us/download/dotnet/5.0) foi lançado em novembro de 2020 com o objetivo de unificar o desenvolvimento para desktop, Web, nuvem, dispositivos móveis, jogos, IoT e aplicativos de IA. O objetivo inicial era produzir um único tempo de execução e framework .NET, cross-platform, integrando as melhores características do .NET Core, .NET Framework, Xamarin e Mono. No entanto, devido à pandemia global de saúde, a unificação foi adiada para o .NET 6. O .NET 5 é uma base de código compartilhada para .NET Core, Mono, Xamarin e futuras implementações do .NET. Além disso, os nomes dos frameworks de destino (TFMs), que expressam qual versão do .NET está sendo direcionada, foram atualizados, então agora temos net5.0. Isso é para código que roda em todos os lugares. Ele combina e substitui os nomes netcoreapp e netstandard e net5.0-windows que representam variantes específicas do .NET 5 que incluem net5.0 mais vinculações específicas do sistema operacional.

### O Atual - .NET 8

O [.NET 8](https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-8) é o runtime mais recente no Ecossistema .NET. Foi lançado em novembro de 2023 e unifica o desenvolvimento para desktop, Web, nuvem, dispositivos móveis, jogos, IoT e aplicativos de IA. O .NET 8 consiste em um App Host (dotnet.exe) que executa o CLR e a Biblioteca. Ele possui um tempo de execução de linguagem comum (CoreCLR) e a Biblioteca de Classes do .NET 8. Também inclui o ASP.NET Core 8. O .NET 8 tem suporte de plataforma quase idêntico ao .NET Core 3.1 para Windows, macOS e Linux.

O .NET 8 é um **Suporte de Longo Prazo (LTS)**. Essas versões têm suporte por três anos após o lançamento inicial.

O .NET 7 foi uma versão de **Suporte Padrão**, com suporte por seis meses após um lançamento subsequente de STS ou LTS.

## Padrão .NET

Diferentes runtimes usam bibliotecas de classes diferentes, por exemplo, o .NET Framework usa a biblioteca de classes do .NET Framework, enquanto o .NET Core contém sua própria biblioteca de classes, assim como o Xamarin com sua biblioteca de classes. Dessa forma, é difícil compartilhar código entre diferentes runtimes, pois eles usam APIs diferentes. A solução da Microsoft é a **biblioteca .NET Standard**, lançada em 2016. Ela representa um conjunto de especificações (formais) que indicam quais APIs você pode usar e todos os runtimes a implementam. É a evolução das Bibliotecas de Classes Portáteis (PCL). Runtimes específicos implementam versões específicas do .NET Standard (implementando APIs específicas). Por exemplo, o .NET Framework 4.8.1 implementa o .NET Standard 2.0, e o .NET 7 implementa o .NET Standard 2.1 ([link](https://learn.microsoft.com/en-us/dotnet/standard/net-standard?tabs=net-standard-1-0#net-implementation-support)).

Para saber mais sobre o Ecossistema .NET, confira [este post no blog](https://milan.milanovic.org/post/a-brief-walk-through-net-ecosystem/).

**Cronograma de Lançamento do .NET pela Microsoft:**

![Cronograma de Lançamento do .NET pela Microsoft](release-schedule.png)


## Recursos de Aprendizado

### 1. C#

C# é uma linguagem de programação desenvolvida pela Microsoft. É a escolha principal para construir desde aplicativos desktop e jogos (usando Unity) até soluções baseadas em nuvem e serviços web. Com um forte suporte para programação orientada a objetos e uma biblioteca rica, é projetada para ser fácil e eficiente.

A versão mais recente é a **[C# 12](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-12)**, lançada em novembro de 2023.

Confira a linha do tempo completa

# Verifique a linha do tempo completa do C#:

![Linha do Tempo do C#](csharp-timeline.png)

Você precisa entender diferentes **recursos da linguagem C#**, tais como:

- Programação orientada a objetos (classes, objetos, interfaces, herança, polimorfismo)
- Variáveis, tipos de dados e operadores
- Tipos de referência e tipos de valor
- Fluxo de controle (condicionais, loops)
- Genéricos
- Tratamento de exceções
- Delegados e eventos
- Assemblies
- Coleções
- LINQ (Consulta Integrada à Linguagem)
- Programação assíncrona com Async/Await

Mas também as **bibliotecas e APIs .NET** para:

- E/S de arquivos e serialização
- Coleções e estruturas de dados
- Rede
- Multithreading e paralelismo de tarefas
- Segurança e criptografia

**Recursos**:

- [Aprenda C# da Microsoft](https://dotnet.microsoft.com/learn/csharp).
- [Fundamentos de C# para Iniciantes Absolutos da Microsoft](https://learn.microsoft.com/en-us/shows/c-fundamentals-for-absolute-beginners/).
- [C# 101 da Microsoft](https://learn.microsoft.com/en-us/shows/csharp-101/)
- [Udemy C# para Iniciantes - Codificando do Zero (.NET Core)](https://www.udemy.com/course/c-and-net-core-for-beginners/)
- [Fundamentos de C# para Iniciantes: Aprenda os Fundamentos do C# Codificando](https://www.udemy.com/course/csharp-tutorial-for-beginners/)
- Aprenda o [dotnet CLI](https://docs.microsoft.com/dotnet/core/tools)
- Gerenciador de pacotes [NuGet](https://learn.microsoft.com/en-us/nuget/what-is-nuget)
- [Dot Net Perls](https://www.dotnetperls.com/s#c#) - Muitos exemplos de código em C#
- Conceitos avançados:
    - [Torne-se um Desenvolvedor .NET Full-stack - Tópicos Avançados](https://www.pluralsight.com/courses/full-stack-dot-net-developer)
    - [Async/Await](https://devblogs.microsoft.com/dotnet/how-async-await-really-works/) por Stephen Toub
    - [Threading em C#](https://www.albahari.com/threading/) por Joseph Albahari
    - [Concorrência](https://www.codeguru.com/csharp/thread-synchronization-c-sharp/) e [Locking](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/statements/lock)
- [Especificação da linguagem C# - ECMA-334](https://www.ecma-international.org/publications-and-standards/standards/ecma-334/)


### 2. Habilidades Gerais de Desenvolvimento

Dominar padrões de design, código limpo e controle de versão como o Git permite que você escreva código eficiente, sustentável e que funcione bem em um ambiente de equipe. É a diferença entre ser um programador e ser um engenheiro de software qualificado.

Aqui, você precisa conhecer diferentes princípios, como:

**Princípios SOLID**:
  - Princípio da Responsabilidade Única (SRP)
  - Princípio Aberto/Fechado (OCP)
  - Princípio da Substituição de Liskov (LSP)
  - Princípio da Segregação de Interface (ISP)
  - Princípio da Inversão de Dependência (DIP)

Mas também:

- DRY (Don't Repeat Yourself)
- KISS (Keep It Simple, Stupid)
- YAGNI (You Ain't Gonna Need It)
- Lei de Demeter (LoD) ou Princípio do Menor Conhecimento
- Composição sobre Herança
- O princípio do menor espanto
- Estilos e padrões de arquitetura de software (MVC, MVP)

**Recursos**:

- Aprenda [Git](https://newsletter.techworld-with-milan.com/p/how-to-learn-git)
- Aprenda [Estruturas de Dados e Algoritmos](https://amzn.to/3LTsZ6o)
- Aprenda [Código Limpo](https://amzn.to/3Qdj91J)
- Aprenda [Fundamentos de Refatoração](https://www.pluralsight.com/courses/refactoring-fundamentals)
- Aprenda [Padrões de Design do livro](https://amzn.to/3QcVQVS) ou [tutoriais em vídeo](https://www.pluralsight.com/paths/design-patterns-in-c) ou faça o [download da folha de dicas](Patterns.png).
  - Os padrões que você deve conhecer são:
    - Singleton
    - Factory Method
    - Adapter
    - Facade
    - Decorator
    - Proxy
    - Command
    - Template method
    - Strategy
    - Observer
- Aprenda [Principais princípios de design de software](https://newsletter.techworld-with-milan.com/p/main-software-design-principles-you)
- Aprenda [SOLID](https://www.pluralsight.com/courses/principles-oo-design) princípios de Design Orientado a Objetos em profundidade.
- Estilos de Arquitetura de Software
    - Aprenda [Fundamentos de Arquiteturas de Software](https://amzn.to/3rEtJWh)
    - Aprenda [Arquitetura em Camadas](https://www.oreilly.com/library/view/software-architecture-patterns/9781491971437/ch01.html)
    - Aprenda [Microservices](https://microservices.io/) e [DAPR](https://dapr.io/)
    - Aprenda [Design Orientado a Domínio](https://learn.microsoft.com/en-us/archive/msdn-magazine/2009/february/best-practice-an-introduction-to-domain-driven-design) ou do [livro](https://amzn.to/49jl0tm)

### 3. ASP.NET Core 

É uma estrutura de alto desempenho, multiplataforma, desenvolvida pela Microsoft para criar aplicativos da web, APIs e microsserviços. Você também pode executar seus aplicativos no Windows, Linux ou macOS. Foi projetada para flexibilidade e escalabilidade, com recursos como injeção de dependência integrada e um sistema de configuração robusto.

Aqui, você também precisa conhecer os **fundamentos do desenvolvimento web**, como:

- HTML, CSS e JavaScript para desenvolvimento front-end
- Protocolos HTTP, DNS, modelo de requisição/resposta e APIs RESTful
- Roteamento, middleware, autenticação e autorização

**Recursos**:

- Conceitos Básicos da Web:
    - [Como a Internet funciona](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work)
    - [O que acontece quando você digita uma URL no seu navegador?](https://newsletter.techworld-with-milan.com/p/what-happens-when-you-type-a-url)
    - [Como o DNS funciona](https://newsletter.techworld-with-milan.com/i/135973327/how-dns-works)
    - [Protocolo HTTP(S)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview) 
- [ASP.NET MVC](https://dotnet.microsoft.com/en-us/apps/aspnet/mvc)
- Curso [Fundamentos do ASP.NET MVC 5 por Scott Alen](https://www.pluralsight.com/courses/aspdotnet-mvc5-fundamentals)
- Curso [Fundamentos do ASP.NET Core por Scott Alen](https://www.pluralsight.com/courses/aspnet-core-fundamentals)
- [Middlewares](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/middleware)
- APIs
    - [Web API](https://dotnet.microsoft.com/en-us/apps/aspnet/apis)
    - [APIs Mínimas](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/minimal-apis?view=aspnetcore-8.0)
    - Protocolos
        - [REST](https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-web-api)
        - [GraphQL](https://graphql.org/)
        - [gRPC](https://grpc.io/)
    - [Melhores Práticas de Design para APIs REST](https://newsletter.techworld-with-milan.com/p/rest-api-design-best-practices)
    - [Compreensão dos Cabeçalhos REST](https://newsletter.techworld-with-milan.com/p/understanding-rest-headers)
- Injeção de Dependência
    - [Ciclos de Vida](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/dependency-injection)
    - [Microsoft Extensions Dependency Injection](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.dependencyinjection?view=dotnet-plat-ext-7.0)
    - [Autofac](https://autofac.org/)
    - [Scrutor](https://github.com/khellang/Scrutor)
- [Configurações e Configurações de Aplicativos](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/configuration)
- [Filtros e Atributos](https://docs.microsoft.com/en-us/aspnet/core/mvc/controllers/filters)
- Segurança
    - [Autenticação](https://docs.microsoft.com/en-us/aspnet/core/security/authentication) ou [este tópico do Reddit](https://www.reddit.com/r/dotnet/comments/we9qx8/a_comprehensive_overview_of_authentication_in/)
    - [Autorização](https://docs.microsoft.com/en-us/aspnet/core/security/authorization/introduction)
    - [IdentityServer](https://identityserver4.readthedocs.io/en/latest)
    - [Auth0](https://auth0.com)
    - [OIDC](https://openid.net/connect)

### 4. .NET do Lado do Cliente (Client Side)

Se você deseja construir interfaces do usuário em .NET, precisará desses frameworks. Razor é um mecanismo de modelo para criar HTML dinâmico, enquanto o Blazor leva isso para um nível superior, permitindo que você construa interfaces do usuário web interativas usando C# em vez de JavaScript. MAUI é um sucessor do Xamarin feito para construir aplicativos móveis multiplataforma. O Windows Presentation Foundation (WPF) é um framework de interface do usuário que cria aplicativos cliente para desktop. A Plataforma Uno é uma interface gráfica do usuário de código aberto multiplataforma que permite que o código baseado em WinUI e Universal Windows Platform (UWP) seja executado no iOS, macOS, Linux, Android e WebAssembly.

**Recursos**:

- [Razor](https://docs.microsoft.com/aspnet/core/mvc/views/razor)
- [Blazor](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor)
- [.NET MAUI](https://github.com/dotnet/maui)
- [WPF](https://learn.microsoft.com/en-us/dotnet/desktop/wpf/overview/?view=netdesktop-8.0)
- [WinUI](https://docs.microsoft.com/en-us/windows/apps/winui/winui3/)
- [Plataforma Uno](https://platform.uno/)
- [Avalonia](https://avaloniaui.net/)
- Nota: [UWP](https://docs.microsoft.com/en-us/windows/uwp/get-started/universal-application-platform-guide) e [WinForms](https://docs.microsoft.com/en-us/dotnet/desktop/winforms/overview/?view=netdesktop-8.0) também são tecnologias .NET do lado do cliente, mas estão mais próximas do fim de sua vida útil.


### 5. Bancos de Dados

Um bom design de banco de dados garante armazenamento eficiente de dados e rápida recuperação, tornando seu aplicativo mais suave e escalável. SQL, a linguagem padrão para interação com banco de dados, oferece o poder de consultar, atualizar e gerenciar os dados que você projetou cuidadosamente para armazenar.

Aqui, você precisa saber:

- Sintaxe SQL
- Noções básicas de design de banco de dados (formas normais, chaves, relacionamentos)
- A diferença entre Inner, Left, Right e Full Join
- Ordem de execução de consultas SQL
- O que é o Otimizador de Consultas

**Recursos**:

- [Design de banco de dados](https://www.youtube.com/watch?v=ztHopE5Wnpc)
- [Aprenda SQL](https://newsletter.techworld-with-milan.com/p/how-to-learn-sql)
- Bancos de dados relacionais
  - [SQL Server](https://www.microsoft.com/sql-server/sql-server-2019)
  - [PostgreSQL](https://www.postgresql.org)
  - [MariaDB](https://mariadb.org)
  - [MySQL](https://www.mysql.com)
  - [Azure SQL](https://azure.microsoft.com/en-us/products/azure-sql/database)
- Bancos de dados NoSQL
  - [MongoDB](https://docs.microsoft.com/aspnet/core/tutorials/first-mongo-app)
  - [RavenDB](https://github.com/ravendb/ravendb)
  - [Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db)
- Ferramentas:
  - [SQLFlow](https://sqlflow.gudusoft.com/#/) - uma ótima ferramenta para visualizar consultas SQL.

### 6. ORM

O mapeamento objeto-relacional (ORM) é como um tradutor entre o seu código C# orientado a objetos e o banco de dados relacional, eliminando a tarefa tediosa de escrever consultas SQL para operações básicas de CRUD. Usando frameworks ORM como o Entity Framework, você pode manipular dados como objetos em seu código, tornando-o mais legível e sustentável. Isso acelera o desenvolvimento, minimiza erros e permite que você se concentre na lógica de negócios complexa em vez de lidar com a sintaxe do banco de dados.

Para o **Entity Framework**, você precisa saber o seguinte:

- DbContext e DbSet para gerenciar conexões de banco de dados e consultar dados
- Abordagens Code-First e Database-First para definir modelos de dados
- Migrações para gerenciar alterações no esquema do banco de dados
- Consultar dados usando LINQ e SQL puro
- Rastreamento de alterações e salvamento de dados

**Recursos**:

- [Entity Framework Core](https://learn.microsoft.com/en-us/ef/core)
    - [Migrações Code First](https://learn.microsoft.com/en-us/ef/core/managing-schemas/migrations/?tabs=dotnet-core-cli)
    - [API Change Tracker](https://learn.microsoft.com/en-us/ef/core/change-tracking/)
    - [Carregamento Lazy, Eager e Explicit](https://learn.microsoft.com/en-us/ef/core/querying/related-data/) 
- [Dapper](https://github.com/StackExchange/Dapper)
- [LINQ](https://www.dotnetnakama.com/blog/understanding-the-dot-net-language-integrated-query-linq/)
- [ADO.NET](https://learn.microsoft.com/en-us/dotnet/framework/data/adonet/)

### 7. Caching

O cache é como a memória de curto prazo do seu aplicativo, armazenando dados acessados com frequência para que possam ser recuperados rapidamente sem sobrecarregar seu banco de dados. Ao reduzir a carga do banco de dados e acelerar o acesso aos dados, o cache dá ao seu aplicativo a vantagem competitiva necessária para atender às demandas dos usuários por responsividade e disponibilidade.

**Recursos**:

- [Cache de Memória](https://docs.microsoft.com/aspnet/core/performance/caching/memory)
- [Redis](https://redis.io/)
- Nível de Aplicação
   - [Integrado](https://learn.microsoft.com/en-us/aspnet/core/performance/caching/response)
   - [Caching de Saída](https://learn.microsoft.com/en-us/aspnet/core/performance/caching/output?source=recommendations)

### 8. Registro (Logging)

O registro captura informações em tempo de execução, erros e outros dados cruciais que podem ajudar você a identificar e corrigir problemas rapidamente, tornando seu aplicativo mais confiável e seguro. Frameworks de registro como NLog ou Serilog se integram perfeitamente ao .NET, proporcionando uma ferramenta de diagnóstico em tempo real indispensável para monitorar a saúde do aplicativo, solucionar problemas e até mesmo obter insights para desenvolvimentos futuros.

**Recursos**:

- [Serilog](https://github.com/serilog/serilog)
- [NLog](https://github.com/NLog/NLog)
- [Microsoft.Extensions.Logging](https://learn.microsoft.com/en-us/dotnet/core/extensions/logging)

### 9. Comunicação

No .NET, temos três tipos de comunicação: comunicação em tempo real, comunicação síncrona e comunicação assíncrona. Tecnologias de comunicação em tempo real, como o SignalR no ecossistema .NET, possibilitam essas funcionalidades mantendo uma conexão constante entre o servidor e o cliente. Elas são usadas em experiências interativas, como bate-papo ao vivo, notificações ou atualizações em tempo real. A comunicação síncrona é principalmente feita usando o HTTP Client, enquanto a comunicação assíncrona é feita por meio de diferentes estruturas e bibliotecas de mensagens e eventos. Sistemas de mensagens atuam como intermediários entre diferentes partes do seu sistema, permitindo que se comuniquem sem estar diretamente conectadas. Isso desacopla seus componentes, tornando mais fácil dimensionar, manter e adicionar novos recursos. Manipuladores de eventos, por outro lado, são usados para lidar com eventos dentro de um único aplicativo. Eles facilitam um modelo de publicador-assinante, onde uma parte do aplicativo pode disparar um evento ao qual outras partes podem reagir.

**Recursos**:

- Comunicação em tempo real:
    - [SignalR Core](https://docs.microsoft.com/aspnet/core/signalr)
    - [WebSockets](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/websockets) 
    - [Socket.IO](https://github.com/doghappy/socket.io-client-csharp)
- Comunicação síncrona: 
    - [HTTP Client](https://learn.microsoft.com/en-us/dotnet/api/system.net.http.httpclient?view=net-8.0)
- Comunicação assíncrona: 
    - Corretores de mensagens:
         - [Azure Service Bus](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-messaging-overview)
         - [RabbitMQ](https://www.rabbitmq.com/tutorials/tutorial-one-dotnet.html)
         - [ActiveMQ](https://activemq.apache.org/)
         - [NetMQ](https://netmq.readthedocs.io/en/latest/)
         - [Apache Kafka](https://kafka.apache.org/)
     - Barramento de mensagens:
         - [MassTransit](https://github.com/MassTransit/MassTransit)
         - [Azure Service Bus](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-messaging-overview)
         - [NServiceBus](https://learn.microsoft.com/en-us/azure/service-bus-messaging/build-message-driven-apps-nservicebus?tabs=Sender)
         - [EasyNetQ](https://easynetq.com/)
     - Manipuladores de eventos:
         - [Azure Event Hub](https://docs.microsoft.com/azure/event-hubs/event-hubs-about)
         - [Azure Event Grid](https://docs.microsoft.com/azure/event-grid/overview)
   
### 10. Tarefas em Segundo Plano

Esses serviços executam tarefas em segundo plano, liberando seu aplicativo para se concentrar nas interações do usuário. Seja processamento de dados, envio automático de e-mails ou limpezas periódicas, os serviços em segundo plano garantem que essas tarefas não afetem a velocidade ou interrompam a experiência do usuário.

**Recursos**:

- [Serviço em Segundo Plano](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/host/hosted-services)
- [HangFire](https://github.com/HangfireIO/Hangfire)
- [Quartz](https://github.com/quartznet/quartznet)

### 11. Mapeamento de Objetos  

Essas bibliotecas automatizam a tarefa de mapeamento entre objetos, eliminando a necessidade de código de mapeamento manual repetitivo e propenso a erros. Isso aumenta a produtividade e minimiza erros, especialmente ao lidar com modelos e DTOs (Objetos de Transferência de Dados) complexos.

**Recursos**:

- [AutoMapper](https://github.com/AutoMapper/AutoMapper)
- [Mapster](https://github.com/MapsterMapper/Mapster)

### 12. Testes

Os testes unitários concentram-se em partes isoladas do seu código, os testes de integração garantem que diferentes partes interajam bem, e os testes end-to-end validam toda a jornada do usuário dentro do seu aplicativo. Juntos, eles formam uma rede de segurança, identificando bugs precocemente, simplificando a depuração e tornando sua base de código robusta e fácil de manter.

Aqui você precisa conhecer:

- Frameworks de teste (xUnit, NUnit, MSTest)
- Executores de teste e exploradores de teste
- Asserts e atributos de teste
- Bibliotecas de simulação (Moq, NSubstitute, etc.)

**Recursos**:

- [Testes Unitários](https://www.pluralsight.com/courses/advanced-unit-testing)
    - Frameworks
      - [xUnit](https://xunit.net/)
      - [NUnit](https://nunit.org/)
      - [MSTest](https://docs.microsoft.com/dotnet/core/testing/unit-testing-with-mstest)
    - Simulação
      - [NSubstitute](https://github.com/nsubstitute/NSubstitute) - para novos projetos
      - [Moq](https://github.com/moq/moq4) - para projetos antigos ([por que](https://www.bleepingcomputer.com/news/security/popular-open-source-project-moq-criticized-for-quietly-collecting-data/))
    - Assert
      - [FluentAssertion](https://github.com/fluentassertions/fluentassertions)
      - [Shouldly](https://github.com/shouldly/shouldly)
    - Geradores de Dados de Teste
      - [Bogus](https://github.com/bchavez/Bogus)
      - [AutoFixture](https://github.com/AutoFixture/AutoFixture)
- Testes de Integração
    - [WebApplicationFactory](https://docs.microsoft.com/aspnet/core/test/integration-tests)
    - [TestServer](https://learn.microsoft.com/en-us/aspnet/core/test/integration-tests?view=aspnetcore-7.0)
    - [Testcontainers](https://dotnet.testcontainers.org/)
- Testes de Snapshot
     - [Verify](https://github.com/VerifyTests/Verify)
- Testes de Comportamento
     - [SpecFlow](https://github.com/techtalk/SpecFlow/tree/DotNetCore)
- Testes End-to-End
     - [Playwright](https://playwright.dev/)
- Testes de Desempenho
     - [K6](https://github.com/grafana/k6)
     - [JMeter](https://github.com/apache/jmeter)

### 13. Observabilidade   

Essas ferramentas fornecem insights em tempo real sobre o desempenho do seu aplicativo, o comportamento do usuário e as taxas de erro, permitindo que você resolva problemas antes que se tornem problemas graves de maneira proativa.

- **Monitoramento** concentra-se na saúde e disponibilidade de serviços e sistemas, muitas vezes disparando alertas para condições pré-definidas.

- **Telemetria** coleta, processa e transmite dados de sistemas, permitindo a análise de padrões, tendências e anomalias.

**Recursos**:

- [Prometheus](https://github.com/prometheus/prometheus)
- [Grafana](https://github.com/grafana/grafana)
- [Datadog](https://www.datadoghq.com)
- [ELK Stack](https://www.elastic.co/what-is/elk-stack)
- [OpenTelemetry](https://github.com/open-telemetry/opentelemetry-dotnet)
- [Jaeger](https://www.jaegertracing.io/)
- [Azure Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview)
- [Azure Log Analytics](https://docs.microsoft.com/azure/azure-monitor/logs/log-analytics-overview)

### 14. Containerização

Soluções de contêiner encapsulam sua aplicação .NET, bibliotecas e tempo de execução em contêineres isolados. Isso permite consistência em vários ambientes de desenvolvimento e produção, resolvendo problemas de dependência. Com recursos como sistemas de arquivos em camadas, você pode gerenciar facilmente imagens de contêineres para ASP.NET, .NET Core ou outros serviços .NET, otimizando tempos de compilação e utilização de recursos.

**Recursos**:
- Contêineres
    - [Docker](https://www.docker.com)
    - [Docker Compose](https://docs.docker.com/compose/)
    - [Docker Hub](https://hub.docker.com/)
    - [Registro de Contêineres do Azure](https://learn.microsoft.com/en-us/azure/container-registry/container-registry-intro)
- Orquestração
    - [Kubernetes](https://kubernetes.io)
    - [Azure Kubernetes Service (AKS)](https://azure.microsoft.com/en-us/products/kubernetes-service)
    - [Helm](https://helm.sh/)
    - [Azure Container Apps](https://docs.microsoft.com/en-us/azure/container-apps/overview)

### 15. Nuvem

Os provedores de nuvem fornecem uma camada de APIs para abstrair a infraestrutura e provisioná-la com base em limites de segurança e faturamento. A nuvem é executada em servidores em data centers, mas as abstrações dão a aparência de interação com uma "plataforma" única ou um grande aplicativo. A capacidade de provisionar, configurar e proteger rapidamente recursos com provedores de nuvem tem sido fundamental para o tremendo sucesso e complexidade da moderna DevOps.

Os provedores de nuvem mais populares no mercado são **AWS** e **Azure**, assim como o **Google Cloud**.

Aqui, você deve saber como gerenciar usuários e administração, redes, servidores virtuais, etc.

**Recursos**:

- [AWS](https://aws.amazon.com/)
- [Azure](https://azure.microsoft.com/)
- [Google Cloud](https://cloud.google.com/)

### 16. Integração Contínua e Entrega Contínua (CI/CD)

CI/CD automatiza as etapas de construção, teste e implantação em um pipeline simplificado e resistente a erros. Isso significa lançamentos mais rápidos, correções de bugs e mais tempo para se concentrar no desenvolvimento de recursos.

Aqui você precisa saber como:

- Ferramentas de construção e implantação (MSBuild, dotnet CLI)
- Sistemas de controle de versão (Git, Azure DevOps)
- Plataformas CI/CD (GitHub Actions, Azure Pipelines, Jenkins, TeamCity)

**Recursos**:

- [Conceitos de DevOps](https://newsletter.techworld-with-milan.com/p/devops-roadmap-2023)
- Serviços:
    - [GitHub Actions](https://github.com/features/actions)
    - [Gitlab CI](https://docs.gitlab.com/ee/ci)
    - [Azure Pipelines](https://azure.microsoft.com/en-us/services/devops/pipelines)
    - [Travis CI](https://travis-ci.org)
    - [Jenkins](https://www.jenkins.io)
    - [TeamCity](https://www.jetbrains.com/teamcity)

### 17. Bibliotecas .NET

Algumas bibliotecas .NET úteis. Observe que nem todas as bibliotecas serão usadas por todos, isso depende principalmente do projeto em que você está trabalhando.

- **[MediatR](https://github.com/jbogard/MediatR)** - Implementação do padrão Mediator em .NET.
- **[Polly](https://github.com/App-vNext/Polly)** - Biblioteca de manipulação de falhas que permite expressar políticas como Retry e Circuit Breaker.
- **[Fluent Validation](https://github.com/JeremySkinner/FluentValidation)** - Biblioteca de validação .NET para construir regras de validação fortemente tipadas.
- **[Benchmark.NET](https://github.com/dotnet/BenchmarkDotNet)** - Biblioteca .NET para benchmarking.
- **[Refit](https://github.com/reactiveui/refit)** - Transforma sua API REST em uma interface ao vivo.
- **[YARP](https://microsoft.github.io/reverse-proxy/)** - Servidor proxy reverso.
- **[Swashbuckle](https://github.com/domaindrivendev/Swashbuckle.AspNetCore)** - Ferramentas Swagger para documentar APIs construídas em ASP.NET Core.

## Considerações adicionais

Além disso, você também precisa saber o seguinte:

### Melhores Práticas de Desempenho

O desempenho desempenha um papel essencial em aplicativos .NET. Aqui, você precisa saber:

#### Perfis e diagnósticos

Essas ferramentas podem ajudar a identificar e depurar diferentes gargalos de desempenho em seu código. Para isso, você pode usar outras ferramentas, como:

- [PerfView](https://joshthecoder.com/2023/10/23/using-perfview-to-diagnose-high-cpu-in-an-aspnet-app.html)
- [Visual Studio Profiler](https://learn.microsoft.com/en-us/visualstudio/profiling/profiling-feature-tour?view=vs-2022)
- [dotTrace](https://www.jetbrains.com/profiler/) e [dotMemory](https://www.jetbrains.com/dotmemory/)

## Boas Práticas de Desempenho

Além das ferramentas, você deve estar ciente de diferentes boas práticas de desempenho para o .NET:

- **Caching** (usando Memory Cache ou Redis)

- **Otimização de Banco de Dados** (otimizar consultas, indexação adequada, pooling de conexões)

- **Programação Assíncrona** (deslocar todas as operações intensivas de CPU ou ligadas à E/S para o banco de dados, sistemas de arquivos, sistemas externos, etc.)

- **Utilizar o Entity Framework com sabedoria** (usar carregamento antecipado, projeções e otimizações como consultas compiladas)

- **Gerenciamento de Memória** (usar tipos de valor e ter cautela com grafos de objetos grandes. Usar o padrão dispose para conexões de banco de dados ou fluxos. Evitar boxing/unboxing. Usar StringBuilder em vez de String para um grande número de concatenações.)

- **Caching HTTP** (usar ETags, cabeçalhos Last-Modified)

- **Minimizar Viagens de ida e volta** (reduzir o número de solicitações HTTP e viagens de ida e volta do banco de dados)

- **CDNs (Content Delivery Networks)** (descarregar ativos estáticos (CSS, JavaScript, imagens) para CDNs para uma entrega mais rápida aos usuários)

- **Compressão** (ativar compressão GZIP ou Brotli para respostas HTTP para reduzir o tamanho da transferência de dados)

- **Logging e Tracing** (evitar log excessivo em produção. Usar rastreamento distribuído em microservices.)

- **Paralelismo e Concorrência** (utilizar paralelismo e multithreading para tarefas vinculadas à CPU usando a classe Parallel ou a Biblioteca de Tarefas Paralelas (TPL))

- **Otimização de Recursos** (otimizar imagens e ativos para a Web para reduzir os tempos de carregamento)

- **HTTP2 sobre SSL** (agora tomar decisões inteligentes sobre o conteúdo da página)

- **Medir e Monitorar o Desempenho** (usar Ferramentas de Diagnóstico do Visual Studio, App Insights ou BenchmarkDotNet)

- **Usar Span<> em vez de coleções** (spans podem representar uma seção contígua de memória; isso significa que podemos usá-los para operar sobre arrays)

## Segurança e Criptografia

A segurança desempenha um papel essencial no desenvolvimento de aplicativos. Os aspectos mais críticos da segurança no mundo .NET são:

- Conceitos de **Autenticação e Autorização**:
  - Cookies
  - ASP.NET Core Identity para gerenciamento de usuários
  - Middleware OIDC .NET
  - OAuth e OpenID Connect para autenticação de terceiros
  - JWT (Tokens Web JSON) para autenticação baseada em token
  - Autorização baseada em funções e reivindicações

- Conceitos de **Criptografia e Proteção de Dados**:
  - Algoritmos de criptografia simétrica e assimétrica
  - APIs de Proteção de Dados do .NET Core
  - Hashing e assinaturas digitais
  - Geração segura de números aleatórios

## Recursos adicionais de aprendizado

- [Plataforma de aprendizado Pluralsight](https://www.pluralsight.com/browse?q=C%20sharp&type=all&sort=highest) - Aprenda C#/.NET principalmente com MVPs da Microsoft.
- [Awesome .NET!](https://github.com/quozd/awesome-dotnet) - Uma coleção incrível de bibliotecas, ferramentas, frameworks e software .NET.
- [Guias de Arquitetura .NET da Microsoft](https://dotnet.microsoft.com/en-us/learn/dotnet/architecture-guides)

### Livros

- [Aprenda C# em um Dia e Aprenda Bem](https://amzn.to/3Qld3fT) - o melhor para iniciantes
- [C# em Profundidade: Quarta Edição](https://amzn.to/3ZPcZbq) por Jon Skeet - o melhor para intermediários
- [Concorrência em C# Cookbook: Programação Assíncrona, Paralela e Multithreaded](https://amzn.to/490EMtu) - o melhor para avançados
- [O Amarelo C#](http://www.csharpcourse.com

## Author

[Dr. Milan Milanović](https://milan.milanovic.org) - CTO at [3MD](https://3mdinc.com) and Microsoft MVP para Tecnologias de Desenvolvedor.

