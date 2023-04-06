<img
  src="https://user-images.githubusercontent.com/44469426/230241106-5e51ce3f-069e-4140-92a6-9c946b1ae514.png"         width="392" 
  height="124" 
  align="center"
/>

# PEA Pescarte

## Tabela de Conteúdos

Aqui você pode achar links diretos para as seções desse documento!

1. [Descrição do Projeto](#description)
2. [Subprojetos](#subprojects)

  - [Pescarte API](#api)
    - [Por que usar Elixir?](#why-elixir)
    - [Diferença entre Concorrência e Paralelismo em Computação](#concurrency-parallelism)
    - [BEAM - máquina virtual do Erlang](#beam)
  - [Pescarte Tags](#labeler)
  - [Pescarte Cotação de Pescados](#price)

3. [Guias para Contribuições](#contribution-guides)
4. [Regras de Negócio](#business-rules)

## Descrição do Projeto

<a id="description" />

O _Projeto PESCARTE_ tem como sua principal finalidade a criação de uma rede social regional integrada por pescadores artesanais e por seus familiares, buscando, por meio de processos educativos, promover, fortalecer e aperfeiçoar a sua organização comunitária e a sua qualificação profissional, bem como o seu envolvimento na construção participativa e na implementação de projetos de geração de trabalho e renda.

Por meio do Projeto PESCARTE as comunidades pesqueiras que vivem nos municípios de Arraial do Cabo, Cabo Frio, Macaé, Quissamã, Campos dos Goytacazes, São João da Barra e São Francisco de Itabapoana são mobilizadas, incentivadas e orientadas a participar de diferentes ações e/ou atividades de natureza educativa. São ações e/ou atividades, cuja realização tem como objetivos: aperfeiçoar a atuação profissional dessas comunidades, na perspectiva, seja da ampliação de sua produtividade, seja para poder melhor se organizar e realizar atividades econômicas solidárias.

A intenção é reforçar as identidades produtivas dessas comunidades pesqueiras, de modo a favorecer a mitigação dos impactos negativos que as afetam e que são decorrentes das atividades realizadas, naquela região, pela indústria de exploração e produção de petróleo e gás natural.

## Subprojetos

<a id="subprojects" />

Atualmente contamos com 4 (quatro) subprojetos implementados no `GitHub` do Pescarte.

### [Pescarte API][pescarte-api]

<a id="api" />

Uma [API][ api-meaning ] (interface de aplicação programável) que expõe dados públicos para serem consultados por entidades externas, mas também fornece dados para nosso outros subprojetos.

É a aplição que se conecta com nossa base de dados, data lake e faz outras integrações com serviços externos como [AWS][ aws-meaning ].

A API do projeto é implementada com [Elixir][ elixir-site ], usando o [framework web][ framework-meaning ] chamado [Phoenix][ phoenix-site ].

#### Por que usar Elixir?

<a id="why-elixir" />

[Elixir][ elixir-site ] é uma [linguagem funcional][ functional-prog ], criada em 2011 pelo José Valim. Ela é baseada na [BEAM][ beam-meaning ], a máquina virtual do [Erlang][ erlang-meaning ]. O Erlang é conhecido por ser uma linguagem robusta, perfeita para aplicações que necessitam ser tolerantes à falhas, concorrentes - aproveitando todo o potencial da máquina - e escaláveis.

O [Elixir][ elixir-site ] surgiu com a proprosta de modernizar a sintaxe do [Erlang][ erlang-meaning ], que é fortemente herdada de [Prolog][ prolog-meaning ] - uma linguagem do paradigma lógico - e adicionar um gerenciador de depêndencias. Elixir e Erlang não são linguagens funcionais porque querem ser, e sim pois a concorrência e paralelismo num programa [POO][ oop-meaning ], [mutável][ immutability ] e [imperativo][ imperative-prog ], torna o gerenciamento das [threads][ thread-meaning ] algo que beira o impossível.

Vantagens da programação funcional:

- Imutabilidade
- Melhor testabilidade
- Programação declarativa
- Sintaxe mais humanamente amigável
- Funções puras, sem efeitos colaterais

##### Diferença entre Concorrência e Paralelismo em Computação

<a id="concurrency-parallelism" />

Imagine uma máquina de venda de refrigerantes, onde apenas uma lata sai por vez, ou seja, apenas uma pessoa pode ser "atendida" após a outra. Com o tempo, forma-se uma fila para comprar refrigerante, onde cada pessoa retira seu item e vai embora. Neste caso, temos um modelo de programação linear.

Fazendo a correlação deste cenário onde a máquina de refrigerante representa a [CPU][ cpu-meaning ] do computador e a fila de pessoas representa a fila de [processos](<https://pt.wikipedia.org/wiki/Processo_(inform%C3%A1tica)>) os quais essa CPU executa.

Agora imagine que temos 2 (duas) máquinas de refrigerante - ou seja, duas CPUs, ou de forma mais realista, dois [núcleos](https://canaltech.com.br/hardware/como-ativar-os-nucleos-do-processador/) dentro da CPU - e agora cada máquina de refrigerante possui sua própria fila de pessoas - processos da CPU. Neste caso, chamamos esse modelo de computação de [_Paralelismo_][ paralel-meaning ].

Num último caso, imagine que existe apenas 1 (uma) máquina de refrigerante (CPU) porém essa máquina é capaz de atender múltiplas filas de pessoas (processos), ou seja, mais de uma pessoa pode retirar seu item ao mesmo tempo da máquina. Para esse modelo de computação damos o nome de [_Concorrência_][ concurrency-meaning ].

A imagem a seguir exemplifica os conceitos de _Paralelismo_ e _Concorrência_:

![concorrencia_paralelismo](https://user-images.githubusercontent.com/44469426/230241225-60c9ac79-302d-4a19-96bd-b76585c5b902.png)

#### BEAM - máquina virtual do Erlang

<a id="beam" />

A [BEAM][ beam-meaning ] é a máquina virtual do [Erlang][ erlang-meaning ] (assim como a [JVM][ jvm-meaning ] do [JAVA][ java-meaning ]). Seu funcionamento básico é: ela divide cada ação do seu programa em pequenas ações, chamados de processos (não confundir com os processos do sistema operacional da máquina local). Esses processos são supervisionados pela própria BEAM, para que quando haja algum erro, o sistema se recupere sozinho e sem atrapalhar os outros processos.

Quando uma aplição Elixir/Erlang é iniciada, a BEAM cria um "Agendador" (Scheduler) para cada núcleo da CPU da máquina. Esses Agendadores também são processos, mas que supervisionam, agendam e gerenciam os outros processos da aplicação. A imagem a seguir exemplifica a crição dos Agendadores:

![beam_schedulers](https://user-images.githubusercontent.com/44469426/230241258-08aeb6d8-9038-4eda-89f0-fb13de077aa9.png)

### [Plataforma Pescarte][ pescarte-plataforma ]

<a id="frontend" />

Subprojeto onde é implementado o [frontend][ frontend-meaning ] do projeto Pescarte. Aqui se encontra a parte visual com qual as pessoas usuárias da nossa plataforma interage! Ela depende da [API do projeto][ pescarte-api ] e é implementada usando a tecnologia [Vue][ vue-meaning ] a partir do framework [Nuxt.JS][ nuxt-meaning ] em conjunto com [TypeScript][ ts-meaning ].

Neste projeto é implementado os componentes criados no [Design System][ ds-meaning ] do PEA Pescarte, e os layouts definidos por nossa pessoa Designer que trabalha no projeto, o [Anthony](https://www.linkedin.com/in/anthonyymuller/).

### [Pescarte Tags](https://github.com/peapescarte/pescarte-labeler)

<a id="labeler" />

Em construção...

### [Pescarte Cotação de Pescados](https://github.com/peapescarte/cotacao-api)

<a id="price" />

Em construção...

## Guia para Contribuições

<a id="contribution-guides" />

Os guias de contribuição, junto com os requisitos e links extras de documentações e materiais para estudos estão separados em cada projeto.

Para contribuir com o Backend (API Pescarte), sigas as intruções descritas [aqui](https://github.com/peapescarte/pescarte-api/blob/main/CONTRIBUTING.md).

Para contribuir com o Frontend (Plataforma Pescarte), sigas as intruções descritas [aqui](https://github.com/peapescarte/pescarte-plataforma/blob/main/CONTRIBUTING.md).

Esperamos que se divirta com suas contribuições, aprenda novos tópicos e tecnologias e se desenvolva em sua carreira!

### Introdução a Programação Funcional

Vídeos, artigos e ferramentas para entender e praticar programação funcional, tanto com Elixir quanto com TypeScript!

- [Canal computerphile (en)](https://www.youtube.com/@Computerphile)
- [Explicando a máquina de turing (en)](https://www.youtube.com/watch?v=dNRDvLACg5Q)
- [Explicando cálculo lambda - base da prog funcional (en)](https://www.youtube.com/watch?v=eis11j_iGMs)
- [Programação funcional com javascript (en)](https://www.youtube.com/watch?v=BMUiFMZr7vk&list=PL0zVEGEvSaeEd9hlmCXrk5yUyqUag-n84)
- [Aprenda programação funcional com javascript (en)](https://www.youtube.com/watch?v=R_-nUkpatwM)
- [O que é programação funcional (pt-br)](https://www.alura.com.br/artigos/programacao-funcional-o-que-e)
- [Introdução a programação funcional (pt-br)](https://inside.contabilizei.com.br/introdu%C3%A7%C3%A3o-a-programa%C3%A7%C3%A3o-funcional-cec510f515cd)
- [Guia de introdução a programação funcional (pt-br)](https://medium.com/true-henrique/programa%C3%A7%C3%A3o-funcional-pura-ruby-e-monads-i-introdu%C3%A7%C3%A3o-b16687db63d)
- [Introdução a programação funcional com Elixir (pt-br)](https://www.youtube.com/watch?v=dB6M4Hwv6cY)
- [Introdução a prprogramação funcional com Elixir (slides) (pt-br)](https://www.slideshare.net/ArthurBraga/introduo-a-programao-funcional-com-elixir-v2)
- [Técnicas de programação funcional com TypeScript (pt-br)](https://oieduardorabelo.medium.com/typescript-t%C3%A9cnicas-de-programa%C3%A7%C3%A3o-funcional-ad0e68b5e064)
- [TypeScript para pessoas programadoras funcionais (pt-br)](https://www.typescriptlang.org/pt/docs/handbook/typescript-in-5-minutes-func.html)
- [Introdução a programação funcional com TypeScripte JavaScript (pt-br)](https://dev.to/grubba/introducao-a-programacao-funcional-com-typescript-e-javascript-22b9)
- [Live Node.JS + TS com programação funcional (pr-br)](https://gist.github.com/fdaciuk/9e7eb058d999bb20caa769684ae76904)
- [Functional TypeScript - código com documentação (pt-br)](https://github.com/robertolima-dev/funcional-typescript)
- [O que é Programação funcional (pt-br)](https://www.youtube.com/watch?v=53Lv3efp7Rk)
- [Programação funcional exemplos em JS e Elixir (pt-br)](https://www.youtube.com/watch?v=8TC-40hWGcs)
- [Aprendendo programação funcional com Elixir (pr-br)](https://www.youtube.com/watch?v=DYszf5MF8fA&list=PLxdiLpHsLM4SKmruij4mLLf8tYItLff5a)
- [JavaScript funcional (pt-br)](https://www.youtube.com/watch?v=T89jpSLK-NM&list=PLv2oOZboUtKMn-xjAICBlINuqKwLmc13e)
- [Aprendendo programação funcional com JS (en)](https://www.youtube.com/watch?v=e-5obm1G_FY)

### Introdução ao Git e GitHub

Vídeos, artigos e ferramentas para entender e praticar versionamento de projetos e gerenciamento de repositórios remotos com Git e Github!

- [Aprenda comandos git visualmente (en)](https://learngitbranching.js.org/)
- [Conceitos básicos de git (en)](https://www.freecodecamp.org/news/learn-the-basics-of-git-in-under-10-minutes-da548267cc91/)
- [Guia completo GitHub (en)](https://www.youtube.com/watch?v=UbJLOn1PAKw)
- [git e github guia completo (en)](https://www.youtube.com/watch?v=RGOj5yH7evk)
- [Guia prático git (pt-br)](https://rogerdudler.github.io/git-guide/index.pt_BR.html)
- [Tutorial git para iniciantes (pt-br)](https://www.hostinger.com.br/tutoriais/tutorial-do-git-basics-introducao)
- [Documentação oficial git (en)](https://git-scm.com/doc)
- [Tutorial git e github para iniciantes (pt-br)](https://www.freecodecamp.org/portuguese/news/tutorial-de-git-e-github-controle-de-versao-para-iniciantes/)
- [Como usar git e github na prática (pt-br)](https://www.youtube.com/watch?v=2alg7MQ6_sI)
- [Guia git e github (pt-br)](https://terminalroot.com.br/git/)
- [Comandos git úteis (pt-br)](https://gist.github.com/leocomelli/2545add34e4fec21ec16)
- [Primeiros passos github, oficial (pt-br)](https://docs.github.com/pt/get-started/quickstart/hello-world)
- [Palestra do Linus Torvalds sobre git (en)](https://www.youtube.com/watch?v=4XpnKHJAok8)

## Regras de Negócio

<a id="business-rules" />

Em construção...

<!-- links alias -->

[api-meaning]: https://www.techtudo.com.br/listas/2020/06/o-que-e-api-e-para-que-serve-cinco-perguntas-e-respostas.ghtml
[aws-meaning]: https://aws.amazon.com/pt/what-is-aws/
[beam-meaning]: https://www.erlang.org/blog/a-brief-beam-primer/
[cpu-meaning]: https://pt.wikipedia.org/wiki/Unidade_central_de_processamento
[core-meaning]: https://canaltech.com.br/hardware/como-ativar-os-nucleos-do-processador/
[erlang-meaning]: https://coodesh.com/blog/dicionario/o-que-e-erlang/
[pescarte-api]: https://github.com/peapescarte/pescarte-api
[pescarte-plataforma]: https://github.com/peapescarte/pescarte-plataforma
[process-meaning]: https://pt.wikipedia.org/wiki/Processo_(inform%C3%A1tica)
[elixir-site]: https://elixir-lang.org
[phoenix-site]: https://www.phoenixframework.org
[paralel-meaning]: https://pt.wikipedia.org/wiki/Computa%C3%A7%C3%A3o_paralela
[concurrency-meaning]: (https://pt.wikipedia.org/wiki/Programa%C3%A7%C3%A3o_concorrente)
[framework-meaning]: https://www.lewagon.com/pt-BR/blog/o-que-e-framework
[java-meaning]: https://www.java.com/pt-BR/download/help/whatis_java.html
[jvm-meaning]: https://pt.wikipedia.org/wiki/M%C3%A1quina_virtual_Java
[prolog-meaning]: https://ww2.inf.ufg.br/~eduardo/lp/alunos/prolog/prolog.html
[thread-meaning]: https://pt.wikipedia.org/wiki/Thread_(computa%C3%A7%C3%A3o)
[oop-meaning]: https://www.alura.com.br/artigos/poo-programacao-orientada-a-objetos
[immutability]: https://medium.com/opensanca/imutabilidade-eis-a-quest%C3%A3o-507fde8c6686
[imperative-prog]: https://pt.wikipedia.org/wiki/Programa%C3%A7%C3%A3o_imperativa
[functional-prog]: https://pt.wikipedia.org/wiki/Programa%C3%A7%C3%A3o_funcional
[frontend-meaning]: https://www.totvs.com/blog/developers/front-end/
[vue-meaning]: https://blog.geekhunter.com.br/vue-js-so-vejo-vantagens-e-voce/
[nuxt-meaning]: https://pt.wikipedia.org/wiki/Nuxt.js
[ts-meaning]: https://kenzie.com.br/blog/typescript/
[ds-meaning]: https://brasil.uxdesign.cc/afinal-o-que-%C3%A9-design-system-448c257b0021
