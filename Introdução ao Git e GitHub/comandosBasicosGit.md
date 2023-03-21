# Pequena Referência de Comandos Git
Link pra a [documentação do Git](https://git-scm.com/doc) - link direto para o livro [Pro Git](https://git-scm.com/book/pt-br/v2)

### Gerando chaves ssh

``ssh-keygen -t ed25519 -C "your_email@example.com"``

### Iniciar o agente ssh em background
$ eval "$(ssh-agent -s)"
> Agent pid 59566
> 
### Indicar a chave ssh privada para o ssh-agent
``ssh-add ~/.ssh/id_ed25519``  > colocar o caminho para sua chave

Após a geração das chaves, a chave pública (nomeChave.pub) 
tem que ser informada no github em:
Settings -> SSH and GPG keys

Mais detalhes no [link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

### Configurações básicas

``` git config --global user.email "email@email.com"```

```git config --global user.name "Nome do Usuário"```

**Remover nome ou email**

Usar o parâmetro --unset seguido do que quer remover
ex:
``git config --global --unset user.name "Nome do usuário"``

**Verificar as configurações**

``git config --list``

### Inicializar repositório local

``` git init ```

### Adicionar arquivos e commit

``git add nome-do-arquivo`` >> pode se passar mais de um arquivo separado por espaço.

``git add * `` >> adiciona todos os arquivos listados como untracked 

``git commit -m "Mensagem do Commit"`` 

### Checando estado dos arquivos

``git status``

### Adicionar repositório remoto ao repositório existente.

``git remote add origin url-do-repositorio.git``

### Visualizar os repositórios remotos cadastrados.

`git remote -v`

Fazendo commit para repositório remoto

``git push origin main``

ou

``git push -u origin main`` >> o -u adiciona referência upstream(rastreamento)

### Puxar os arquivos no repositório remoto

``git pull origin master``

### Clonando repositórios

``git clone url-do-repositorio.git``

















