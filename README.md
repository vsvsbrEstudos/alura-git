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

Enviar e fazer o ligação com o branch local: `git push -u origin nome_branch`

Mostrar branches remotas `git branch -r`

Baixar uma branch remota e ligar com uma branch local: `git branch -t nome_branch origin/nome_branch`
