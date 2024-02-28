Ensino do git e git hub que é uma ferramenta de versionamento de código muito importante

md é a extensão mark down e é uma linguagem de marcação que se utiliza para escrever os readme (instruções e orientações que não ficam no código do projeto)
na sua pasta de projetos abrir o git bash aqui
nele digitar git init para criar o repositório
irá aparecer que foi inicializado um repositório vazio do git e em frente a pasta aberta apareceu (master) ou (main). Esse master siginifica que agora já está na branch master, ou seja, é a linha de código principal, a qual é a Main
na pasta em que está o projeto, como item oculto está a pasta do .git e nele tem todas as informações necessárias par o projeto funcionar
o repositório criado está vazio, ou seja não há nenhum Commit(algo salvo/postado, os pontos na história, as versões da linha do tempo), assim precisamos da primeira versão para começar a editar
dentro do git, digite git add, o qual vai mandar os arquivos para a área de stayding (chama você que estava lá nos fundos para ficar na frente do palco (commit), pronto para se apresentar)
digite git add + os arquivos que quer maandar para a área de stayding onde será feito o commit (git add Readme.md)
para verificar, coloque git status, para verificar e mostrará que não há commits ainda, porém nas mudanças fala que há um novo arquivo, o qual é o readme.md que está em stayding, esperando
agora no git bash, digite git commit -m "Título do commit"
assim será feito/criado o commit no repositório
nisso havia dado erro, porque o Git não reconhecia, assim teve que colocar os comandos:
git config --global user.email "meu email"
git config --global user.name "meu nome"
voltando ao commit, para verificar agora, colocar git status e vai dizer que não há nada para commitar/juntar, porque tudo está atualizado e não há nada na área de stayding
vamos renomear a branch em que está para main usando: git branch -M "main"
no site do git há o GUI Clients, o qual mostra toda a parte visual do commit e branch do que está acontecendo por trás como o python.tutor, porém dá para fazer isso no git hub também
Foi criado então na nossa máquina um repositório (pelo git init) e agora vamos criar um no github para que todo o repositório feito na máquina vá para o github, sendo de visualização e edição pública ou privada. O github é uma plataforma para se hospedar os códigos
Após criar o repositório agora no github, apareceu o restante dos códigos (página de inicialização), os quais serão colocados no git bash
 git remote add origin https://github.com/JonnCobblepot/Primeiro_Projeto_com_GIT.git 
 Entendendo esse código colocado: o git é porque está fazendo um comando no git; o remote é a conexão entre o repositório local (máquina) e o do github; add adiciona; o origin é o apelido ou nome que está dando para o repositório do github e o link dele.
 como pode-se ver o link do seu repositório no github sempre começa com https://github.com/"nome do seu usuário no github"/"Nome do seu projeto".git
 Não dá para dar um ctrl V no git bash, então pode-se teclar a tecla Insert ou ctrl+shift+v
 Agora, o último comando é o git push -u origin main
 O push é aquele empurrão que dá nos commits que estão no repositório local para o do github
 Após dar o enter, aparecerá uma aba para fazer o login no github. O link do repositório para criar o remote é padrão, então alguma pessoa que sabe seu username e o nome do repositório poderia enviar coisas para ele, porém existe a privacidade que só você pode mexer no seu repositório a não ser que seja concedida a permissão para tal.
 Agora será feito o login com o Browser para a segurança pedindo a sua senha do GitHub
 Para confirmação que deu certo, será enviado um e-mail para sua conta cadastrada no git e além disso no git bash mostrará uma nova mensagem automaticamente que funcionou
 Agora entre na sua página do github novamente e dê um refreash (recarregue a página)
 O primeiro commit aparecerá na plataforma, vindo do Readme.md que foi configurado no git bash
Até agora só foi feito um commit e o repositário embora esteja salvo, não está atualizado
Criamos uma nova pasta, que é o projeto realmente que desenvolveremos em código
Para limpar o git bash, digite clear

Vamos dar git add, para mandar para a área de stayding; git add .  esse ponto indica que vai atualizar ao repositório todos os arquivos
damos o git status para ver como está
Agora digite git commit -m "criação do projeto"
Esse commit já está no repositório da máquina, agora vamos enviá-lo ao github
git push origin main
Não precisou dar o remote, porque o remote é feito apenas uma vez, que é a conexão entre os repositórios; para o repositório apelidado de origin
Pronto

Agora vamos ao conceito de Branch, a ramificação da linha principal (main) do seu código.
Digite: git checkout -b "branch_novo_botao"
com esse comando está sendo criada uma ramificação, uma nova branch chamada branch_novo_botao e o comando do checkout automaticamente sai da branch principal (main)
E agora, volta tudo novamente as configurações depois que criou o botao e tudo os códigos dele, por exemplo, agora vai as atualizações do projeto
git add .
git commit -m "novo botao"
git push origin branch_novo_botao (coloca agora o nome da branch e não mais a main)
para voltar para a main e trabalhar nela, digitar: git checkout main
para voltar novamente para a outra branch: git checkout branch_novo_botao
agora para juntar a branch com a main, digitar git merge branch_novo_botao
após juntar as duas, agora irá mandar todas as informações atualizadas e alteradas para o repositório
para isso digite git push origin main

Pegando o repositório próprio do Github ou de outra pessoa e puxar diretamente para a sua máquina:
ao entrar no perfil de outra pessoa, entrar num repositório, no ícone verde CODE, clicar e estará ali o clone, vai copiar o link dali.
crie uma nova pasta na sua área de trabalho, a criada teve o nome Git
nele abra com o git bash
no git bash digite: git clone https://link do projeto copiado .git
assim está tudo certo, só abrir agora a pasta com o VS CODE e tem o arquivo que copiou
Agora, se você tem esse arquivo em código na sua máquina, porém o autor fez alguma atualização nele no github, o que você tem na sua máquina está desatualizado
estavamos dentro da pasta do clone do git, e para entrarmos no GitTutorial em que foi feito o clone vamos dar um comando:
cd gittutorial
o comando cd troca entre pastas
após isso é só dar git pull e tudo sera puxado para seu código, puxa todas as alterações feitas pelo autor

se quiser que esse repositório de alguma pessoa do GitHub vá para o seu GitHub, é só dar um fork (garfo) e adicionar ao seu perfil, assim nos seus repositórios aparecerá ele também, mas como sendo um forked
Se quiser também, você pode alterar o fork que você fez, em alguma característica do projeto. Além disso, você pode enviar essa alteração para o autor de quem você fez o fork, e isso é chamado de pull request, ou seja, você está enviando uma solicitação ao autor para ver a alteração que você fez e se quiser puxar ela para o repositório dele. É uma requisição para puxar os dados que você alterou, podendo ou não adicionar ao seu projeto, vai de sua escolha.
então você da o fork, altera em algo, faz o commit, clique em contributed (para contribuir) e assim dar um pull request, e assim você cria um pull request e avisa a pessoa no comentário oq fez a sua mudança e tals.
No seu repositório ao lado dos Codes, há os pull requests que você recebeu também, para aceitar depois de ver qual foi a alteração é só clicar em merge pull request

Para dúvidas entrar no site e ver a documentação do Git