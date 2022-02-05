## Comandos importantes para realizar a transferência de dados local para o servidor

**Git Status**

Exibe os caminhos que têm diferenças entre o arquivo do índice e o commit atual no HEAD, 
os caminhos que têm diferenças entre a árvore de trabalho e o arquivo do índice, 
os caminhos na árvore de trabalho que não são rastreados pelo Git (e não foram ignorados pelo gitignore[5]). 
O primeiro é o que você confirmaria executando o comando git commit;
o segundo e o terceiro são os que você pode confirmar, 
executando o comando git add antes de executar o comando git commit.

**Git Add**

Este comando atualiza o índice usando o conteúdo atual encontrado na árvore de trabalho, para preparar o conteúdo preparado para o próximo commit. Ele normalmente adiciona o conteúdo atual dos caminhos existentes como um todo, mas com algumas opções também pode ser usado para adicionar conteúdo com apenas parte das alterações feitas nos arquivos da árvore de trabalho aplicadas ou remover caminhos que não existem na árvore de trabalho não mais.

O "índice" contém um instantâneo do conteúdo da árvore de trabalho, e é esse instantâneo que é obtido como o conteúdo do próximo commit. Assim, depois de fazer qualquer alteração na árvore de trabalho e antes de executar o comando commit, você deve usar o addcomando para adicionar quaisquer arquivos novos ou modificados ao índice.

Este comando pode ser executado várias vezes antes de um commit. Ele apenas adiciona o conteúdo do(s) arquivo(s) especificado(s) no momento em que o comando add é executado; se você quiser que as alterações subsequentes sejam incluídas no próximo commit, você deve executar git addnovamente para adicionar o novo conteúdo ao índice.

O git status comando pode ser usado para obter um resumo de quais arquivos têm alterações que são preparadas para o próximo commit.

O git addcomando não adicionará arquivos ignorados por padrão. Se algum arquivo ignorado foi especificado explicitamente na linha de comando, git addfalhará com uma lista de arquivos ignorados. Arquivos ignorados alcançados por recursão de diretório ou globbing de nome de arquivo executado pelo Git (cite seus globs antes do shell) serão ignorados silenciosamente. O comando git add pode ser usado para adicionar arquivos ignorados com a -fopção (force).

**Git commit**

O Git commit permite que você crie um commit, ou seja, você consegue guardar o estado do seu repositório naquele momento. Existem diferentes estratégias para fazer commits, mas a ideia principal é que a cada ponto em que o seu código esteja funcionando com uma nova pequena funcionalidade, exista um commit. 

Dessa forma, ao longo do tempo, você vai conseguir ver uma “história” do seu repositório e o que aconteceu para que chegasse do jeito que está hoje. Um commit, além de mostrar um snapshot do seu repositório, tem outros metadados, como autoria, uma mensagem, timestamp, entre outros.

**Git push**

O comando git push é usado para enviar o conteúdo do repositório local para um repositório remoto. O comando push transfere commits do repositório local a um repositório remoto. É o oposto do comando git fetch, que importa commits para branches locais, enquanto o comando push exporta commits para branches remotos. Os branches remotos são configurados usando o comando git remote. O comando push tem o potencial de sobrescrever modificações e, assim, deve ser usado com cuidado. Esses itens são discutidos abaixo.

**Site útil sobre comandos do Git**

https://comandosgit.github.io/
