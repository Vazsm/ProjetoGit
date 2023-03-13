md = markdown #É uma linguagem de marcação normalmente utilizada para
arquivos readme
Pode salvar utilizando Ctrl S

git --version #prints the version of your git, if it is the latest version and if it is correctly installed.
Vamos na pasta do projeto git e clicamos com o botão direito e clicamos em 'Git Bash Here'
Inicializamos um Repositório Git Vazio digitando:

git init
Cria uma pasta oculta com o nome .git no nosso projetogit
Não devemos apagar essa pasta, pois ela que contém as informações e configurações do nosso git
Todas as informações para o versionamento
Temos acesso a nossa Branch Master
Nosso repositório está vazio, sem commits(publicações/versões)
Então temos que digitar o comando:
git add Readme.md
Esse comando envia os arquivos para a área de staging, que é uma área de espera para os arquivos que estão prestes a serem postos em cena, para os arquivos que serão 'commitados' (publicados)
Nesse casso, nós enviamos para a área de staging o arquivo Readme.md
Para vermos os status do nosso git, nós digitamos:
git status
Nós vamos ver que estamos na branch master, sem commits ainda.
Se você digitou o nome do arquivo errado, com a letra inicial maiúscula, por exemplo,  ele dirá 'Untracked files'. Vai sugerir o nome do arquivo existente que mais se aproxima do nome digitado errado. E vai falar que não há nada adicionado para commit.
Caso tenha digitado corretamente, ele irá reconhecer a presença de um novo arquivo: readme.md
Já que sabemos que o arquivo certo está no staging, podemos dar commit:
git commit -m 'primeiro commit'

seguindo a sintaxe:
git commit -m "text/title"
Ele avisará que o x arquivos mudaram, com y inserções 
Ele dirá que a alteração foi feita na master branch/root
Talvez para dar commit você tenha que digitar:

git config --global user.email "email"
git config --global user.name "username"
Isso serve para registrar o usuário que fez a alteração/commit
Vendo o git status novamente, não terá nada adicionado para commitar, pois já commitamos o arquivo.
Digitando:

git branch -M "main"
Alteramos o nome da nossa branch master para main (que passou a ser utilizada recentemente?)
Nós podemos baixar versões mais visuais, com GUI Clients do site do GIT
------
Vamos acessar nossa página de repositórios no github e criar um novo repositório
Criaremos uma pasta com o mesmo nome do nosso projeto ProjetoGit
ele nos dará um link virtual dessa página, nos dirá os comandos git que utilizamos, e nos dará mais dois códigos
Você pode digitar:
git remote add origin <link> #para colar o link use ctrl, shift insert
Ou você pode colar o código já pronto que o github lhe dá
git corresponde a um comando do git
remote corresponde à conexão entre o repositório git da nossa máquina com o repositório do github
add corresponde a adicionar
origin corresponde ao nome padrão do repositório do github
e o link é o url específico do nosso repositório no github

Com isso, realizamos a conexão entre o repositório git da nossa máquina e o repositório do github.
No entanto, ainda não foi enviado nenhum arquivo para o github
Para isso, utilizaremos o segundo comando que o github nos manda usar:

git push -u origin main
push corresponde a um empurrão dos commits que estão no repositório local para o repositório github
-u corresponde ao comando de upload ou update?
origin é o nome padrão do repositório github
main corresponde à branch que estamos utilizando, nesse caso é a main
O git pedirá a confirmação de seu usuário no github e lhe enviará um e-mail confirmando que o arquivo foi enviado.
Atualizamos o site e nosso commit está lá
clear
limpa o git bash
git add . #Vai mandar todos os os arquivos para a área de staging, sem precisar inserir o nome de todos eles.
Depois de sincronizarmos nosso git com o github, não precisamos usar novamente o git remote add origin <link>
Só precisamos utilizar o push:
git push origin main

Para criarmos uma nova branch, utilizamos:
git checkout -b <'nome da branch'>
exemplo:
git checkout -b 'novo-botão'
Esse comando cria uma nova branch e já altera para que as novas modificações sejam feitas nela.
A nova branch pode servir para um novo recurso, criando outro arquivo. Ou pode ser uma branch com alterações em cima de arquivos já existentes.
Criada uma nova branch, podemos realizar o processo de envio:
git add . 
git status
git commit -m 'v2.2 branch botao'
git push origin novo-botão #pois é o nome da branch que estamos utilizando agora

Agora, nosso github foi atualizado e temos duas branchs nele:
a Main e a Novo-botão. O gituhub nos indica quantos commits a nova branch está à frente da branch Main.
Podemos acessar a nova branch e os arquivos atualizados que ela tem.

No git bash, podemos alternar entre branchs, utilizando o comando:
git checkout <nome da branch>
exemplo:
git checkout main
git checkout novo-botão

Podemos juntar/fundir branchs indo na branch que você quer atualizar, nesse caso a main, e escrever o comando:
git merge novo-botão 
Então, utilizando/modificando a branch main, iremos fundir ela com a nova branch novo-botão.
Agora precisamos enviar essa atualização da Main para o github, utilizando o comando:
git push origin main

Para copiar um projeto do github, crie uma pasta no seu computador, e dentro dela abra o git bash. Vá no repositório do projeto e clique em <code>, copie o link https do clone e digite o comando no git:
git clone <link>
Pronto, agora sua pasta já possui o projeto clonado.

Para obter uma versão atualizada de algum projeto do github que você já tenha no seu computador, vá na pasta e abra o git desse projeto. Agora:
cd <nome do projeto>
exemplo:
cd gittutorial
Esse comando é para abrir o repositório do projeto, para poder modificar as branchs.
A pasta do projeto está fechada quando não há o nome da branch que você está utilizando. Para isso, utilize o comando acima.
Agora que a pasta já está aberta, digite:
git pull
Esse comando vai puxar as novas atualizações/versões do projeto.

Fork será a cópia do projeto/repositório do github de alguém para o seu próprio github. Sempre será avisado que o projeto foi de um fork em alguém.

Pull request é quando alguém faz alterações no projeto de outra pessoa e envia as alterações para a pessoa, para ela aceitar ou recusar as alterações no projeto dela.
Byee

testando