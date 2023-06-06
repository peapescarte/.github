<p align="center">
  <img
    width="392"
    height="124" 
    align="center"
    src="https://user-images.githubusercontent.com/44469426/230446665-7e83ce6c-4f94-416a-9ec3-7c1e43961cf8.svg"
    alt="Logo PEA Pescarte com os 10 peixinhos"
  />
</p>

# PEA Pescarte

## Tabela de Conteúdos

Aqui você pode achar links diretos para as seções desse documento!

1. [Descrição do Projeto](#description)
2. [Subprojetos](#subprojects)
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

### [Plataforma Pescarte][ pescarte-plataforma ]

<a id="api" />

O projeto é implementado de ponta a ponta com [Elixir][ elixir-site ], usando o [framework web][ framework-meaning ] chamado [Phoenix][ phoenix-site ]. A aplicação é um monolito e não há intenção de quebrar em microsserviços pois temos pouca escala. Apesar disso existem outros dois subprojetos que são a parte da plataforma, porém serão integradas em breve. Desejamos quebrar algumas partes da plataforma em bibliotecas para melhor manutembilidade, como os componentes do [Design System][ ds-meaning ].

Neste projeto é implementado os componentes criados no [Design System][ ds-meaning ] do PEA Pescarte, e os layouts definidos por nossa pessoa Designer que trabalha no projeto, o [Anthony](https://www.linkedin.com/in/anthonyymuller/).

### [Pescarte CLI](https://github.com/peapescarte/pescarte-cli)

> WIP - trabalho em progresso

Ferramenta de linha de comando para gerenciar novos serviços pescarte.

Em construção...

### [Pescarte Tags](https://github.com/peapescarte/pescarte-labeler)

<a id="labeler" />

Em construção...

### [Pescarte Cotação de Pescados](https://github.com/peapescarte/cotacao-api)

<a id="price" />

Em construção...

## Guia para Contribuições

<a id="contribution-guides" />

Os guias de contribuição, junto com os requisitos e links extras de documentações e materiais para estudos estão separados em cada projeto.

Para contribuir com a Plataforma (PLataforma Pescarte), sigas as intruções descritas [aqui](https://github.com/peapescarte/pescarte-plataforma/blob/main/CONTRIBUTING.md).

Esperamos que se divirta com suas contribuições, aprenda novos tópicos e tecnologias e se desenvolva em sua carreira!

### Linux e terminal

- [Curso completo de linux (en)](https://www.youtube.com/watch?v=sWbUDq4S6Y8)
- [PDF de comandos básicos para terminal (en)](https://bjpcjp.github.io/pdfs/devops/linux-commands-handbook.pdf)
- [O que são gerenciadores de pacotes (en)](https://www.youtube.com/watch?v=0W8-3RwvJwc)
- [Comandos básicos linux (terminal) (pt-br)](https://www.youtube.com/watch?v=JEhVB4VHsTI)
- [Linux, primeiros passos (pt-br)](https://www.youtube.com/watch?v=6nN2EglOqCM&list=PLHz_AreHm4dlIXleu20uwPWFOSswqLYbV)
- [Aprenda Linux - para iniciantes (pt-br)](https://www.youtube.com/watch?v=K05CssAbQgo&list=PLZsjaJhVZaxX9xCXhZDJnhFcIL4ncLjVj)
- [Curso de linux avançado (pt-br)](https://www.youtube.com/watch?v=11MiDMES140&list=PLGw1E40BSQnRZufbzjGVzkH-O8SngPymp)
- [Comandos essenciais de terminal para pessoas desenvolvedoras (pt-br)](https://www.youtube.com/watch?v=TQ01CHNzq7o)
- [Terminal para pessoas desenvolvedoras (pt-br)](https://www.youtube.com/watch?v=yIExip79lLM)
- [NixOS, um sistema operacional para pessoas desenvolvedoras (pt-br)](https://www.youtube.com/watch?v=J8uH_6WY3WA)
- [15+ comandos de terminal para pessoas desenvolvedoras (en)](https://www.youtube.com/watch?v=CV-ven_rxhw)
- [Guia de terminal para pessoas desenvolvedoras frontend (en)](https://www.joshwcomeau.com/javascript/terminal-for-js-devs/)
- [Linha de comando para iniciantes (en)](https://www.freecodecamp.org/news/command-line-for-beginners/)

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

### Lógica matemática e algoritmos

- [Introdução a lógica matemática (pt-br)](https://www.youtube.com/watch?v=tiARjzPh2pI&list=PL7RjLI0hJPfClF1VUbV6rxEKhisvGKeiI)
- [Noções de lógica (pt-br)](https://www.youtube.com/watch?v=PltqUuwR9ec&list=PLEfwqyY2ox85ShbZ1O0fXmkUxavBmSNaK)
- [Lógica matemática (pt-br)](https://www.youtube.com/watch?v=pU4I8sC-2WM&list=PLvLkxtdUefNxVJRFVNBNLtNs7NvpkMlX0)
- [Curso lógica de programação (pt-br)](https://www.youtube.com/watch?v=8mei6uVttho&list=PLHz_AreHm4dmSj0MHol_aoNYCSGFqvfXV)
- [Introdução a lógica de programação (pt-br)](https://www.youtube.com/watch?v=SrKTnlKdLrQ&list=PLpaKFn4Q4GMNlLZQcOjt_-xxz6BTmugdU)
- [Introdução a algoritmos, 3rd edição (en)](https://sd.blackball.lv/library/Introduction_to_Algorithms_Third_Edition_(2009).pdf)
- [Trilhas e exercícios para aprender linguagens de programação - Elixir incluso (en)](https://exercism.org/)
- [Algoritmos: uma introdução usando programação funcional (en)](https://github.com/yiqiaowang/learning/blob/master/Algorithms-A-Functional-Programming-Approach.pdf)
- [Algoritmos para programação funcional (en)](https://github.com/yiqiaowang/learning/blob/master/2018_Book_AlgorithmsForFunctionalProgram.pdf)

### Introdução a Programação Funcional

Vídeos, artigos e ferramentas para entender e praticar programação funcional, tanto com Elixir quanto com TypeScript!

- [Curso Elixir (pt-br)](https://www.youtube.com/watch?v=WRGvPgCHMfI&list=PLv3nyCBtlWP8I9rknIrfcJWrO05yEzknD)
- [Canal computerphile (en)](https://www.youtube.com/@Computerphile)
- [Explicando a máquina de turing (en)](https://www.youtube.com/watch?v=dNRDvLACg5Q)
- [Explicando cálculo lambda - base da prog funcional (en)](https://www.youtube.com/watch?v=eis11j_iGMs)
- [Programação funcional com javascript (en)](https://www.youtube.com/watch?v=BMUiFMZr7vk&list=PL0zVEGEvSaeEd9hlmCXrk5yUyqUag-n84)
- [Aprenda programação funcional com javascript (en)](https://www.youtube.com/watch?v=R_-nUkpatwM)
- [O que é programação funcional (pt-br)](https://www.alura.com.br/artigos/programacao-funcional-o-que-e)
- [Introdução a programação funcional (pt-br)](https://inside.contabilizei.com.br/introdu%C3%A7%C3%A3o-a-programa%C3%A7%C3%A3o-funcional-cec510f515cd)
- [Guia de introdução a programação funcional (pt-br)](https://medium.com/true-henrique/programa%C3%A7%C3%A3o-funcional-pura-ruby-e-monads-i-introdu%C3%A7%C3%A3o-b16687db63d)
- [Introdução a programação funcional com Elixir (pt-br)](https://www.youtube.com/watch?v=dB6M4Hwv6cY)
- [Introdução a programação funcional com Elixir (slides) (pt-br)](https://www.slideshare.net/ArthurBraga/introduo-a-programao-funcional-com-elixir-v2)
- [O que é Programação funcional (pt-br)](https://www.youtube.com/watch?v=53Lv3efp7Rk)
- [Programação funcional exemplos em JS e Elixir (pt-br)](https://www.youtube.com/watch?v=8TC-40hWGcs)
- [Aprendendo programação funcional com Elixir (pr-br)](https://www.youtube.com/watch?v=DYszf5MF8fA&list=PLxdiLpHsLM4SKmruij4mLLf8tYItLff5a)
- [Estruturas de Dados puramente funcionais (en)](https://github.com/yiqiaowang/learning/blob/master/Purely-Functional-Data-Structures.pdf)

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
