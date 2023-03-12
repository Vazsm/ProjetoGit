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
