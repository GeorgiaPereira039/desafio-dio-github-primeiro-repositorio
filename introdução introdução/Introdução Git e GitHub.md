### Olá seja bem vindo como anotações sobre meu estudo introdutório ao Git e GitHub 👾



Antes de começar devemos conhecer os comandos que será usado e para que serve.

**Windows**                                                                     **Unix**

###### ✔**CD - (..)**  Muda de diretório (voltar)                     ✔**CD - (..)**  Muda de diretório (voltar) ######

###### ✔**DIR**  - Lista repositórios									      ✔**LS -** Lista repositórios 		 ######       

###### ✔**MKDIR -** Cria diretório											✔**MKDIR -** Cria diretório  ######         

###### ✔**DEL / RMDIR** - Deleta										      ✔ **RM -RF -** Delata ######          



👾 **INICIANDO O GIT NA PRÁTICA**

Comandos a ser usado

✔**Git init -** Iniciar o repositorio

✔**Git add -** Adicionar arquivos e dar inicio ao versionamento 

✔**Git commit -** O comando **git commit** é usado para confirmar as alterações na cabeça. 

Comando ***git commit –m “coloque sua mensagem aqui”***

✔ **Git Push -** Em tradução livre significa ***Empurre.*** É outro dos comandos git básicos mais usados. Um simples envio, envia as alterações feitas para o ramo mestre do repositório remoto associado ao diretório de trabalho

✔**Git Pull - ** Usado para mesclar todas as alterações presentes no repositório remoto para o diretório de trabalho local, o comando pull é usado. 

✔**Git Config -** Usado para definir valores de configuração específicos do usuário como e-mail, algoritmo preferido para diff, nome de usuário e formato de arquivo etc.

✔**Git Clone -** Comando **git clone** é usado para fins de verificação de repositório. Se o repositório está em um servidor remoto poderá ser usado

✔**Git Status - ** O comando **git status** exibe a lista de arquivos alterados juntamente com os arquivos que ainda não foram adicionados ou confirmados. 

✔**Git remote**  O comando **git remote** permite que um usuário se conecte a um repositório remoto. O comando a seguir lista os repositórios remotos atualmente configurados: 

Comando ***git remote –v***

✔**Flag -a** Use para ver pastas ocultas 



#### 🐱‍💻 **GIT - SISTEMA DE CONTROLE DE VERSÃO DISTRIBUIDO** 🐱‍💻

O Git trabalha com arquitetura de **Branch** ou **Ramificações**
Cada novo **Commit** ou seja *alteração* no código cria um novo ponto na ramificação / branch original.
Ao criar uma nova filial trabalhando em uma nova funcionalidade se cria nova uma ramificação baseada em outra já existente e os compromissos realizados nessa nova ramificação não existira na ramificação original.
Os arquivos geralmente ficam em um **repositório remoto**

#### ⚙SHA-1

Sha significa **Secure hash algorithm** (Algoritmo de dispersão seguro), trata se de um conjunto de funções *Hash* criptográficas.

Sha1 produz um valor de dispersão de 160 [bits](https://pt.wikipedia.org/wiki/Bit) (20 [bytes](https://pt.wikipedia.org/wiki/Byte)) conhecido como resumo da mensagem. Um valor de dispersão SHA-1 é normalmente tratado como um número [hexadecimal](https://pt.wikipedia.org/wiki/Hexadecimal) de 40 dígitos.

SHA-1 faz parte de várias aplicações e protocolos de segurança amplamente utilizados, incluindo [TLS](https://pt.wikipedia.org/wiki/Transport_Layer_Security) e [SSL](https://pt.wikipedia.org/wiki/SSL), [PGP](https://pt.wikipedia.org/wiki/PGP), [S/MIME](https://pt.wikipedia.org/w/index.php?title=S/MIME&action=edit&redlink=1) e [IPsec](https://pt.wikipedia.org/wiki/IPsec). Tais aplicações podem também usar MD5; Ambos MD5 e SHA-1 descendem de MD4. O hashing de SHA-1 também é utilizado em sistemas de [controle de revisão distribuídos](https://pt.wikipedia.org/wiki/Sistema_de_controle_de_versão) como [Git](https://pt.wikipedia.org/wiki/Git), [Mercurial](https://pt.wikipedia.org/wiki/Mercurial) e [Monotone](https://pt.wikipedia.org/w/index.php?title=Monotone&action=edit&redlink=1) para identificar revisões, assim como detectar corrupção ou adulteração de dados. 



📚**OBJETOS INTERNOS DO GIT / BLOB / TREE / COMMIT**



**Blob**

Armazenamento de conteúdo. Este tipo de objeto é chamado de *blob*

Um **blob** (objeto binário grande) do **Git** é o tipo de objeto usado para armazenar o conteúdo de cada arquivo em um repositório. O hash SHA-1 do arquivo é calculado e armazenado no objeto do **blob**. Estes pontos de extremidade permitem ler e escrever objetos do **blob** em seu banco de dados d **Git** em **GitHub**.

A API de blob do Gist permite criar e obter um blob do Git (objeto binário grande), o tipo de objeto usado para armazenar o conteúdo de cada arquivo em um repositório.



**Árvore de Objetos - TREE - Armazena** **blobs**

O próximo que iremos ver é a *um* **grupo de arquivos**, que resolve o problema de conexão com o nome de arquivo e também permite a conexão de um grupo de arquivos. O Git armazena o conteúdo em uma maneira semelhante a um sistema de arquivos UNIX, porém um pouco simplificado. Todo o conteúdo é armazenado como objetos **tree** **e** **blob** , com as **árvores** correspondendo a entradas de um diretório UNIX e *blobs* correspondendo mais ou menos a *códigos* ou conteúdos de arquivos. Um objeto único *tree* contém uma ou mais entradas, cada uma contendo uma referência SHA-1 para um *blob* ou *subtree* com seu modo, tipo e nome de arquivos associados.

Conceitualmente, os dados são armazenados pelo Git é algo assim

<img src="C:\Users\Geo Silva\Downloads\data-model-1.png" alt="data-model-1" style="zoom: 50%;" />

O comando **git commit** é usado para confirmar as alterações na cabeça. Tenha em atenção que quaisquer alterações efetuadas não irão para o repositório remoto. Uso

<img src="C:\Users\Geo Silva\Downloads\Imagem sem título.png" alt="Imagem sem título" style="zoom: 80%;" />

![magem sem título](C:\Users\Geo Silva\Downloads\magem sem título.png)

**CHAVE SSH - FORMA SEGURA DE ESTABELECER UMA CONEXÃO ENCRIPTADA ENTRE DUAS MÁQUINAS**



🐱‍👤**Como gerar a chave**

1. Acesse: https://github.com/settings/keys

1. Dentro do Git Bash digite: **ssh-keygen -t ed25519 -C (e-mail)**
2. Pressione Enter e escolha o local ou press enter novamente
3. Crie uma senha (A senha não fica visível)
4. A chave pública e privada será gerada



🛑**Após criada use os comandos**

1. **cd /c/Users/Geo Silva/.ssh/** - No meu caso como meu user apresenta espaço ele faz com que o comando entenda que tem 2 argumentos. Só colocar ' simples dessa forma **cd '/c/Users/Geo Silva/.ssh'**

2. Use o comando **"ls"** para listar os arquivos. E verá as chaves - **id_ed25519 id_ed25519.pub**

3. Para ver o **conteúdo** da chave publica use o comando **cat id_ed25519.pub -**

4. Ao ver token acesse o Github e gere a chave



🐱‍👤**Para fazer a chave funcionar é necessário inacializar o Ssh agent. Para isso**

 

1. Digite **eval $(ssh-agent -s)** Ao gerar o agent - **Agent pid 2089**

2. É preciso passar o caminho do locar e entregar a chave privada a ele, para isso digite **ssh-add  id_ed25519**

3. Coloque a senha da chave e a entidade será adicionada - **Identity added:     id_ed25519 (mail)**

_________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________





Repositório - Fiz meu primeiro repositório inserindo alguns links de músicas do Youtube. Poderá ver clicando em [Meu primeiro repositório](https://github.com/GeorgiaPereira039/lista-music.git)



⚙Passo usado para criar o repositório

Passo 1️⃣ Criando as pastas através do comando: **mkdir**

```
mkdir Music 

$ cd /c/Music/lista-musica
```



Passo 2️⃣ Iniciando o repositório através do comando: **init**

```
$ git init

Initialized empty Git repository in C:/Music/lista-music/.git/

$ ls -a

./ ../ .git/
```



Passo 3️⃣ Configurando um name e um e-mail, para que seja fornecido as commits um autor. Comando usado **Git Config**

```
Geo Silva@DESKTOP-6S2KG1T MINGW64 /c/Music/lista-music (master)

$ git config --global user.email "email"

Geo Silva@DESKTOP-6S2KG1T MINGW64 /c/Music/lista-music (master)

$ git config --global user.name &&&&&


```

4️⃣ Iniciando o versionamento, comando usado **git add \*** e  **git commit -m ""**

```
Geo Silva@DESKTOP-6S2KG1T MINGW64 /c/Music/lista-music (master)
$ git add *

Geo Silva@DESKTOP-6S2KG1T MINGW64 /c/Music/lista-music (master)
$ git commit -m "commit inicial"
[master (root-commit) 2dabecb] commit inicial
 1 file changed, 42 insertions(+)
 create mode 100644 play/walls.md

Geo Silva@DESKTOP-6S2KG1T MINGW64 /c/Music/lista-music (master)
$ ls
play/

Geo Silva@DESKTOP-6S2KG1T MINGW64 /c/Music/lista-music (master)
$ git status
On branch master
nothing to commit, working tree clean

```

Passo 5️⃣ Add o READme, comando usado **echo >**

```
$ echo > README.md
README.md  play/

$ git add *
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

Geo Silva@DESKTOP-6S2KG1T MINGW64 /c/Music/lista-music (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   README.md

```

Passo 6️⃣ Subindo o repositório local para o remoto 

```
No GithHub vá em
Menu > "Meus repositórios" >  "Novo"
Copiar o link HTTPS
```

Passo 7️⃣ No Git Bash use o comando  **git remote add origin** e adicione o link copiado Depois use o comando **Git push origin master** para empurrar para área remota.



### Feito!! 😁 ###

_____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

#### **E se ocorrer algum conflito? **😮 ####

 um conflito de **merge** no Git ocorre quando dois desenvolvedores alteram o mesmo trecho de código e a única maneira de resolver este conflito é através de uma intervenção manual, alterando o código em questão e submetendo um novo commit. Conflitos podem acontecer tanto ao mesclar branches (ramos), quanto ao mesclar commits dentro da mesma branch.



🧨Para resolver o conflito use o comando **git pull**

```
$ git pull origin master
```

Faça a alteração que deve ser feita, de mais alguns comandos

```
$ git add *
```

```
$ git commit -m ""
```

```
$ git push origin master
```

___________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

Links úteis:

 [Sha-1](https://pt.wikipedia.org/wiki/SHA-1)

[Comandos básicos do Git](https://www.hostinger.com.br/tutoriais/comandos-basicos-de-git?ppc_campaign=google_performance_max&gclid=CjwKCAjw_b6WBhAQEiwAp4HyIMHJFnbyt6BgS5p2eQhUXLZbpwcyvenlFr4d4hl1gVYCIxjJ83mmThoCpgIQAvD_BwE)

[Sintaze Markdown](https://www.markdownguide.org/basic-syntax/)

[Resolvendo conflitos no GIT](https://metring.com.br/guia-resolvendo-conflitos-no-git)

[Conflitos git merge](https://www.atlassian.com/br/git/tutorials/using-branches/merge-conflicts)





