# Lista de comandos Git em português
_Uma lista dos comandos Git mais usados_

## Índice
**[Obtendo & Criação de Projetos](#Obtendo-&-Criação-de-Projetos)**  
**[Obtenha um repositório](#Obtenha-um-repositório)**  
**[Básico](#Basico)**
**[Branching & Merging](#Branching-&-Merging)**
**[Sharing & Updating Projects](#Sharing-&-Updating-Projects)**
**[Inspeção & Comparação](#Inspeção-&-Comparação)**
**[Desfazendo Coisas](#Desfazendo-Coisas)**
**[Dicas Úteis](#Dicas-Úteis)**
**[Links Úteis](#Links-Úteis)**
---

### Obtendo & Criação de Projetos

| Comando | Descrição |
| ------- | --------- |
| `$ git init` | Inicializa um repositório Git local |
| `$ git clone <usuário@servidor:/caminho/para/o/repositório/.git>` | Cria uma cópia local de um repositório remoto |
|`$ git clone </caminho/para/o/repositório/.git>`|Cria uma cópia de trabalho em um repositório local|

### Básicos

| Comando | Descrição |
| ------- | --------- |
| `$ git status` | Checa o status |
| `$ git add <nome-arquivo.txt>` | Adiciona um arquivo para área de stage |
| `$ git add .` | Adiciona todos os arquivos novos ou modificados para a área de stage |
| `$ git commit -m "<Mensagem de Commit>"` | Comita as alterações |
| `$ git rm -r <nome-arquivo.txt>` | Remove um arquivo (ou pasta) |

### Branching & Merging

| Comando | Descrição |
| ------- | --------- |
| `$ git branch` | Lista as branches (o asterisco denota a branch atual) |
| `$ git branch -a` | Lista todas as branches (local e remoto) |
| `$ git branch [nome da branch]` | Cria uma nova branch |
| `$ git branch -d [nome da branch]` | Deleta uma branch |
| `$ git push origin --delete [nome da branch]` | Deleta uma branch remota |
| `$ git checkout -b [nome da branch]` | Cria uma nova branch e muda para ela |
| `$ git checkout -b [nome da branch] origin/[nome da branch]` | Clona uma branch remota e muda para ela |
| `$ git checkout [nome da branch]` | Seleciona uma branch |
| `$ git checkout -` | Muda para a última branch |
| `$ git checkout -- [nome-arquivo.txt]` | Descarta modificações de um arquivo |
| `$ git merge [nome da branch]` | Faz um merge de uma branch na branch atual |
| `$ git merge [source branch] [branch alvo]` | Faz um merge de uma branch em outra branch |
| `$ git stash` | Tirar o estado sujo do seu diretório de trabalho |
| `$ git stash clear` | Remove todas as entradas 'stash' |
| `$ git branch -f <nome-da-branch> <referencia>`| Move uma branch de acordo com uma referência. Obs: A <referencia> pode ser outra branch, tag ou o HEAD|

### Sharing & Updating Projects

| Comando | Descrição |
| ------- | --------- |
| `$ git push origin [nome da branch]` | Enviar uma branch para seu repositório remoto |
| `$ git push -u origin [nome da branch]` | Envia as alterações da branch informada para um repositório remoto (e selecionar a branch) |
| `$ git push` | Envia as alterações para o repositório remoto (branch atual) |
| `$ git push origin --delete [nome da branch]` | Deletar uma branch remota |
| `$ git pull` | Atualiza o repositório local para o último commit |
| `$ git pull origin [nome da branch]` | Recebe alterações do repositório remoto |
| `$ git remote add origin ssh://git@github.com/[usuario]/[nome-repositorio].git` | Adicionar um repositório remoto |
| `$ git remote set-url origin ssh://git@github.com/[usuario]/[nome-repositorio].git` | Seta um repositório da origin branch para o SSH |

### Inspeção & Comparação

| Comando | Descrição |
| ------- | --------- |
| `$ git log` | Ver modificações |
| `$ git log --summary` | Ver modificações (detalhadas) |
| `$ git diff [branch original] [branch alvo]` | Visualizar alterações antes de mesclar |

### Desfazendo Coisas
| Comando| Descrição|
| ------ | -------- |
|`$ git clean -n`| Exibe quais arquivos serão apagador com o comando abaixo|
|`$ git clean -f`| Apaga os arquivos exibidos no comando acima
|`$ git revert hash_do_commit_a_ser_revertido`| Reverter o que foi enviado. Este comando não apaga o commit, ele faz um novo commit desfazendo o que foi feito no commit escolhido. Usado para salvar sua sexta. :) |
|`$ git reset [--soft] [--mixed] [--hard] hash_do_commit_anterior_ao_que_se_quer_excluir`| Desfaz alterações|

> OBS: 
>   --soft: apaga o commit mas deixa os arquivos na fila para commitar novamente; 
>   --mixed: apaga o commit e retira os arquivos da fila para serem commitados; 
>   --hard: apaga o commit e as alterações nos arquivos; 

### Dicas Úteis
| Comando| Descrição|
| ------ | -------- |
|`$ gitk`|Interface gráfica padrão|
### Links Úteis
 - https://rogerdudler.github.io/git-guide/index.pt_BR.html
 - https://learngitbranching.js.org/
 - https://gist.github.com/davidalves1/2f7cb1e58197ba6da0436512f508b21a#visualizar-modifica%C3%A7%C3%B5es
 - https://gist.github.com/leocomelli/2545add34e4fec21ec16
 - https://git-scm.com/book/en/v2/Git-on-the-Server-Getting-Git-on-a-Server
 - https://stackoverflow.com/questions/2816369/git-push-error-remote-rejected-master-master-branch-is-currently-checked
