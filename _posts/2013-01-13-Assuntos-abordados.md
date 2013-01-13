---
layout: post
title: Assuntos abordados
tags:
- futuro
- webstack
- async/await
- webapi
- asp.net
- azure
- entity framework
- signalr
- knockoutjs
- sammyjs
- toastr
- momentjs
- typescript
---

####Sobre o que falar
Bom, eu iria escrever no notepad sobre o que eu quero falar nos meus posts, mas acho que fica melhor postar aqui e compartilhar. A medida que eu for postando, atualizo esse post e fica como uma espécie de índice.<!--break-->

####Server-side
Apesar de estar gostando dessa onda de desenvolvimento client-side, é claro que precisamos do servidor para quase tudo, portanto vou focar bastante em como otimizar o server-side para fazer com o client-side fique mais responsivo e que a [latência percebida](http://www.codeofhonor.com/blog/reducing-perceived-latency) seja a menor possível.

Vou falar sobre coisas como o [async / await](http://msdn.microsoft.com/en-us/library/vstudio/hh191443.aspx), que é uma abstração do já existente framework de programação assíncrona do .NET e sobre MVC e WebApi, que fazem parte do [webstack do asp.net](http://aspnetwebstack.codeplex.com/).

Vou falar muito sobre [Entity Framework](http://entityframework.codeplex.com/) também, já que é o ORM que eu escolhi pra trabalhar (e tem maior integração com o Azure).

Vou mostrar o novíssimo [SignalR](http://www.asp.net/signalr), que eu acho que foi o melhor lançamento do webstack em 2012 e vai bombar demais em 2013. Essa biblioteca abstrai pro desenvolvedor todos os pormenores de se criar uma aplicação em real-time. [SignalR](http://www.asp.net/signalr) te deixa trabalhar com a certeza de que existe uma conexão persistente entre o cliente e o servidor, de modo que tanto o cliente pode chamar um método no servidor (que é que fazemos na web desde sempre), quanto o servidor pode chamar o método no cliente e isso é muito legal. Não é mais necessário ficar 'pingando' o servidor de um em um segundo para saber se algo aconteceu. O servidor te informa quando acontecer.

####Windows Azure
Vou utilizar o [Windows Azure](http://www.windowsazure.com) em praticamente todos os exemplos.
Serviços como o [Windows Azure Web Sites](http://www.windowsazure.com/home/features/web-sites/), que permite que você esteja preparado para botar um site na internet em **SEGUNDOS** e o [SQL Azure](http://www.windowsazure.com/pt-br/home/features/data-management/), que é uma versão do sql server 2012 (com algumas limitações) na nuvem!
Tem também o [Blob Storage](http://www.windowsazure.com/en-us/develop/net/how-to-guides/blob-storage/) que permite que você salve e gerencie arquivos e o [Table Storage](http://www.windowsazure.com/en-us/develop/net/how-to-guides/table-services/) que é o que a Microsoft apresentou para concorrer com os outros [bancos de dados NoSQL](http://nosql-database.org/).

####Client-Side
Aqui é que tudo vai ficar muito interessante, pois ainda é um paradigma novo para muitos. Muita gente ainda tá deixando para renderizar todo o html no servidor. Talvez isso ainda faça sentido para alguns cenários muito específicos, como é caso do twitter que [voltou para a arquitetura de renderização no servidor](http://engineering.twitter.com/2012/05/improving-performance-on-twittercom.html) para garantir uma experiência mais parecida em todos os computadores. Notem que isso não quer dizer que eles estão buscando a **melhor** experiência, e sim uma experiência mais **uniforme** para todos.

Mas quero apresentar algumas tecnologias que estou testando e usando em projetos reais e que facilitam muito a vida do desenvolvedor que deseja partir para o desenvolvimento client-side.

É preciso entender, primeiro, um novo conceito. O conceito de SPA (Single Page Applications - olhem esse [link do John Papa](http://www.johnpapa.net/building-single-page-apps-with-knockout-jquery-and-web-api-ndash-the-story-begins/)).
O melhor exemplo de SPA, por ser amplamente usado, é o [gmail](http://www.gmail.com). A primeira vez que ele carrega na sua máquina, ele já baixa **TODO** o conteúdo necessário para que a aplicação funcione. Daí pra frente, é só uma questão de trocar dados entre cliente-servidor. 

A primeira dela, e a que mais estou gostando de aprender e utilizar é o [KnockoutJS](http://knockoutjs.com/). Essa biblioteca, desenvolvida pelo [Steven Sanderson](https://twitter.com/stevensanderson) que trabalha para a Microsoft, é uma biblioteca que, utilizando o padrão MVVM (Model, View, ViewModel), vincula uma ViewModel (objeto javascript) à uma View (html). Isso quer dizer que toda vez que o valor mudar na viewmodel, a view terá o pedaço de html vinculado alterado para representar o novo valor. E isso é **MUITO** legal. Quando você pensa nas possibilidades disso, com atualizações automáticas com [SignalR](http://www.asp.net/signalr), a histórica fica muito divertida.

Além do KnockoutJS, andei usando [SammyJS](http://sammyjs.org/), que é uma biblioteca que ajuda muito quem está desenvolvendo SPA's. Essa biblioteca tem um suporte muito bom às rotas (sim, galera de ruby-on-rails e mvc, essas rotas!), e algumas coisas a mais como a possibilidade de se vincular a um evento e executar alguma ação quando esse evento acontecer.

Tem também o [MomentJS](http://momentjs.com/) que tira todo esse trauma de trabalhar com datas em javascript e o [toastr](https://github.com/CodeSeven/toastr) que virou meu sistema preferido de informar algo para o usuário.

Vai ser muito JavaScript, heim... Vou escrever quase todo esse javascript utilizando o [Typescript](http://www.typescriptlang.org/), que é um superset (duvido que você consiga traduzir isso) de JavaScript. Ou seja, não reinventaram o JavaScript, nem quiseram substituí-lo. A única proposta do TypeScript é trazer o mundo das linguagens estáticas para o JavaScript, fazendo com que muitos dos erros que só são percebidos em tempo de execução possam ser pegos em tempo de compilação. Sim, o TypeScript é uma linguagem compilada. E é compilada em JavaScript válido e seguindo várias das melhores práticas.

####Finalizando
Eu duvido que teria escrito isso tudo no notepad, mas essa introdução de assuntos já é super válida. Só lendo isso tudo, já dá pra sair pesquisando muita coisa legal na internet.

É isso! Se alguém tiver mais alguma sugestão de temas, é só deixar nos comentários.