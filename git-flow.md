# Como trabalhamos com o Git?

É senso comum entre desenvolvedores que o Git é uma ferramenta poderosa, tornando-se mesmo indispensável em projetos colaborativos.

Mas para obter resultados de alta performance e uma produtividade capaz de atender as nossas demandas, nós não apenas utilizamos o Git, mas adotamos uma metodologia de controle de versão conhecida como **Git-Flow**.

# Como funciona o fluxo de desenvolvimento?

A branch _master_ é aquela onde o código do nosso produto final está armazenado. Tudo o que vai para lá precisa ser cautelosamente revisado, a fim de evitar conflitos, bugs e códigos não performáticos.

Para entregar uma tarefa, uma nova funcionalidade no sistema ou a correção de um bug, um desenvolvedor precisa que o seu código seja enviado à branch _master_.

Num cenário onde **não se utiliza o Git-Flow**, esses seriam os comandos necessários para que o desenvolvedor enviasse o seu código à branch master:


```
On branch master
Your branch is up to date with 'origin/master'.

$ git add .
$ git commit -m "adicionando uma nova função"
$ git push
```

E pronto! O código escrito por este desenvolvedor estaria na branch _master_, sem a necessidade da revisão de nenhum colega de trabalho.

# Na prática, o que fazemos de diferente?

Nós valorizamos a qualidade da nossa codebase (base de código), e por isso sabemos que nenhum trecho de código deve ser inserido nela sem a devida revisão.

Assim, ao iniciar uma nova tarefa, ou tendo um bug corrigido, nós criamos uma nova **branch** com o código que escrevemos.

```
On branch master
Your branch is up to date with 'origin/master'.

$ git checkout -b newFeature/addFooMethod
$ git add .
$ git commit -m "newFeature: adicionando uma nova função"
$ git push --set-upstream origin newFeature/addFooMethod
```

Ao final, teremos criado uma nova branch no repositório remoto, com o exato código que escrevemos e adicionamos. Agora, para que o nosso código seja enviado para _master_, teremos que abrir um Pull Request.

# O que é um Pull Request?

Literalmente, é uma requisição de _pull_ (do inglês, "puxar"). Em outras palavras, estamos solicitando que o nosso código, o código da nova branch criada, seja _enviado para master_.

Para que esse código seja de fato _enviado,_ precisaremos que nossos colegas façam a **revisão** do código e, finalmente, aprovem a nossa solicitação.

Assim, estabelecemos um fluxo de trabalho que ajuda a garantir a qualidade do código enviado ao nosso produto final.

# Finalmente, a padronização de commits

Nossos commits dizem muito sobre a seriedade com que levamos o Git-Flow.

Por isso, utilizamos uma convenção que nos permite assegurar que temos commits legíveis e coerentes. Veja o link abaixo:

[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0-beta.2/
)
