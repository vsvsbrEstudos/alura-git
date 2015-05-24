## aula 1

Cobriu instalação, configuração básica (ssh-keygen, bash) e...

```
#!bash
git clone
git branch
git checkout [branch]
git diff [branch1] [branch2]
git blame [file]

```

## aula 2 - Ciclo básico



```
#!bash
git init

git add .
git add -i
git commit -m
```



##aula 3 - Repositórios remoto

Alterações no git
```
git log
git whatchanged -p
```

Criou um repositório no GitHub

**Bitbucket**:
```
#!bash
git remote add origin              git@bitbucket.org:vsvsbrEstudoJava/alura-git.git
  --->         nome local          remoto

git push origin master
```

**GitHub**:
```
#!bash
git remote add github git@github.com:vsvsbrEstudos/alura-git.git


git push github master
```




remoto
```git clone git@bitbucket.org:vsvsbrEstudoJava/alura-git.git```

```
#!bash

git clone
git pull
git push
```

##aula 4 - Branches

Mostrar branches locais e a usada correntemente: `git branch`

Criar uma branch: `git branch nome_branch`

Alternar entre branches: `git checkout nome_branch`

Criar uma branch e alternar em um comando: `git checkout -b nome_branch`

Enviar para repositório remoto: `git push origin nome_branch`

Enviar e fazer o ligação (track) com o branch local: `git push -u origin nome_branch`

Mostrar branches remotas `git branch -r`

Baixar uma branch remota e ligar com uma branch local: `git checkout -t origin/nome_branch` ou `git branch -t nome_branch origin/nome_branch`

Apagar branch remota: `git push origin :nome_branch` ou `git push origin --delete nome_branch`

##aula 5 - Merge - resolução de conflito

O GIT faz merge automático, porém as vezes, há conflitos. Os arquivos com conflitos aparecem com marcações em seu conteúdo, indicando o conteúdo local e o remoto. 

```
<<<<<<< HEAD [alteração local]
Linhas alteradas localmente
======= [separador do commit]
Linhas alteradas remotamente
>>>>>>> [sha do commit remoto]
```

Facilitar o merge com `git mergetool -t meld`.

Exibe o arquivo alterado localmente na **esquerda**, no **meio** mostra o _mergeado_ e o remoto, com alterações do servidor, à **direita**.

Configurar a ferramenta de merge padrão: `git config --global merge.tool meld`

ref.: http://www.gitguys.com/topics/merging-with-a-gui/

##aula 6 - Boas práticas

Antes da implementação de uma tarefa:
1. cria-se uma branch -- _branch_local_
2. Faz as alterações
3. Volta para a master
4. Faz o pull para ver atualizações 
5. Havendo atualizações faz se o rebase `git rebase master branch_local`
  1. havendo conflitos, vai para a branch local
  2. resolve o conflito
  3. continua o rebase com `git rebase --continue`
6. Volta para a master
7. Faz o merge com `git merge branch_local`
8. envia para o servidor

O que faz o rebase:
> O objetivo com comando git rebase é fazer com que a branch em que se está,
> tenha um novo HEAD que está em outra branch. Ou seja, a base da branch, a
> partir da qual você vai realizar seus commits, deverá ser modificada. Para
> isso, caso haja commits novos na branch que terá a base trocada, o Git
> coloca seus commits em um local temporário, e em seguida começa a aplicar a
> nova base. Após a atualização do HEAD, o Git começa a aplicar seus commits
> sobre a nova base.

Opções do rebase:
```
When you have resolved this problem run "git rebase --continue".
If you would prefer to skip this patch, instead run "git rebase --skip".
To restore the original branch and stop rebasing run "git rebase --abort".
```


Novos comandos dessa aula:
```
git merge
git rebase master desenvolvimento
git rebase --continue
```



