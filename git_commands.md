O que é GIT?

    Git é um softwere para rastrear alterações em qualquer conjunto de arquivos, geralmente usado para coordenar o trabalho em programadores que desenvolvem codigo-fonte de forma colaborativa durante o desenvolvimento de doftwere. Seus objetivos incluem velocidade, integridade de dados e suporte para fluxos de trabalho não lineares distribuídos.

O que é GitHub?

    GitHub, inc. é um provedor de hospedagem na internet para desenvolvimento de softwere e controle de vresão usando Git. Ele oferece o controle de versão distribuída e a funcionalidade de gerenciamento de código-fonte do Git, além de seus próprios recursos.

    Pra que serve o GitHub?

        "Hostear" o seu código em um lugar seguro.

        Compartilhar seu projeto facilmente com outros devs.

        Outros devs podem colaborar com seu projeto.

        etc...

Por que ultilizar o Git?

    Todas as pessoas que trabalham com desenvolvimento de softwere usam ele.

    Para versionar o seu projeto, mantendo assim um histórico de tudo que foi feito e podendo voltar ou seguir para qualquer versão.

Repositório:

    Essencialmente git repositório é um diretório chamado .git dentro do seu projeto.

    Este repositório rastreia todas as mudanças feitas nos arquivos do seu projeto, construindo um histórico ao longo do tempo.

Commit:

    Básicamente o commit serve para fazermos as marcaçoes históricas no nosso projeto.

        MODIFIED:
            &git status ///// Ver todas as alterações no projeto.

        STAGING:
            &git add ///// Prepara a(s) alteração(ões) para serem comitadas.

        COMMITED:
            &git commit ///// Cria o ponto histórico

        PUSH:
            &git push //// Envia o ponto histórico para o projeto no GitHub.

Branch:

    Mostra todas as ramificações do meu projeto e me permite criar mais ramificações de qualquer ponto histórico.

Configurando o Git:

    &git config --global --list ////// Lista de identificação de clientes para saber quem enviou o commit.

    Adicionar cientes:

        &git config --global user.name "Your userName" ///// Seu nome

        &git config --global user.email "Your email" ////// Seu email

Criar um repositório:

    &git init ////  Cria um repositório git no projeto.

    (.git) é uma pasta que vai ficar observando seu projeto e alertando alterações(add, delete, update e create)

    Criar um repositório no GitHub:
        GitHub.com -> (Create new Repository -> Preencher -> Criar)
        Project file -> (git init -> git remote add origin -> git branch -M main -> git add -> git commit -> git push)

Colocando arquivos no STAGE(git add):

    É um lugar onde enviamos as alterações que já podemos comitar e para vermos todas as alterações basta digitar git status.

    &git add . //// add all changes to stage area.

    &git add file.html file.css //// Add a especifiques files to stage area.

Commit:

    O commit é o ponto histórico que queremos salvar no nosso projeto. No commit se pega tudo que esta na stage area e envia para o projeto no GitHub. Isso só funciona se voce tiver permição ou for o dono desse repositório se não voçê terá de fazer uma (PULL REQUEST).


    Envia o comit para o projeto no GitHub.
        &git commit -m 'ADD(index.html,style.css) UPDATE(config.json) REMOVE(default.svg)'



    &git log //// Exibe todos os pontos salvos.

    &git log --oneline ///// Exibe todos os pontos salvos apenas com o id do commit e a mensagem do commit.



    Voltar a um commit sem oque foi foito apos(&git checkout <commitID>).

    Reverte um commit(&git revert <commitID>).

    Voltar a um commit, mas tudo que foi feito continua só que fora do stage(&git reset <commitID>).

    Exclui o commit(&git reset <commitID> --hard)

Ignorando arquivos:

    Basta criar a arquivo .gitignore na raiz da aplicação e colocal o caminho para os arquivos ou pastas a serem ignoradas

Branch(Feature):

    Branch seria as ramificações temporais, ou seja, quando vamos implementar uma nova feature(uma nova funcionalidade que será implementada) criamos uma branch para trabalharmos sem o risco de errar na branch principal e quando terminarmos de fazer a nossa feature podemos enviar para a branch principal.

    Básicamente uma branch cria uma cópia da branch em questão para podemos implementar novas funcionalidades apartir de um commit sem cometer erros na branch principal.

    &git branch ///// Lista de todas as branchs dentro da branch main.

    &git branch <branchName> ///// Criar uma branch.

    &git branch -d/-D <branchName> ///// Excluir uma branch.

    &git checkout <branchName> ///// Entrar na branch desejada.

MERGE:

    Entre na branch em questão e execute esse comando: &git merge <branchName>

    Esse comando junta a branch em que voçẽ está com a branch informada no comando.

    Quando ocorrer conflitos teremos que decidir que branch fica e que branch sai e podemos juntar umas partes de uma branch e umas partes da outra branch e fazer o merge.
    
    Quando resolvemos conflitos apenas comitamos as alterações sem uma mensagem pois a mensagem é a padrão do git apos uma resolução de um conflito.









