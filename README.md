# Git
Git é um sistema de controle de versão distribuído gratuito e de código aberto projetado para lidar com tudo, desde projetos pequenos a muito grandes com velocidade e eficiência.

**Referências:**
<br>

Alguns links que podem ajudar entender melhor sobre Git, comandos e fluxos.

- [Git](https://git-scm.com/)
- [Git Docs](https://git-scm.com/docs)
- [Git Book](https://git-scm.com/book/en/v2)
- [Git Branch Model](https://nvie.com/posts/a-successful-git-branching-model/)
- [Gitflow](https://www.atlassian.com/br/git/tutorials/comparing-workflows/gitflow-workflow)

<br>

# Comandos básicos, intermediários e avançados
## config
| Comando | Descrição |
| ------ | ------ |
| `git config --global user.name "<nome-usuario>"` | Faz a configuração do nome de usuário. |
| `git config --global user.email "<email-usuario>"` | Faz a configuração do e-mail do usuário. |
| `git config --global --list` | Faz a listagem dos valores atribuídos na configuração. |
| `git config --global alias.<abreviacao> <comando-git>` | Cria uma abreviação para o comando do git. |
| `git config --global --unset alias.<abreviacao>` | Faz a remoção do alias cadastrado. |
| `git config --global alias.<abreviacao>` | Verifica o comando que foi cadastrado. |
| `git config --get-regexp` | Faz a listagem de todos os alias configurados. |
 
## init/clone/add/remove/commit/status
| Comando | Descrição |
| ------ | ------ |
| `git init` | Inicializa repositório Git. |
| `git clone ssh://git@github.com/<usuario>/<nome-repositorio>.git` | Faz a clonagem do repositório para a pasta corrente. |
| `git add --all` | Adiciona todos os arquivos para área de preparação. |
| `git add <nome-do-arquivo.extensao>` | Adiciona único arquivo para área de preparação. |
| `git remote add origin ssh://git@github.com/<usuario>/<nome-repositorio>.git` | Adicionar um repositório remoto. |
| `git remote set-url origin ssh://git@github.com/<usuario>/nome-repositorio>.git` | Seta um repositório da origin branch para o SSH. |
| `git rm -r <nome-do-arquivo.extensao>` | Remove arquivo ou pasta. |
| `git commit -m "<mensagem>"` | Salva mudanças no repositório local e adiciona mensagem de commit. |
| `git status` | Verifica estados dos arquivos do repositório |

## stash
| Comando | Descrição |
| ------ | ------ |
| `git stash` | Salva as mudanças ainda não comitadas em uma pilha temporária para uso posterior. |
| `git stash clear` | Remove todas as entradas 'stash'. |
| `git stash list` | Faz a listagem das mudanças salvas na pilha temporária. |
| `git stash apply` | Traz a alteração mais recente que foi salva para a branch atual. |
| `git stash apply stash@{X}` | Traz a alteração de posição X que foi salva para a branch atual. |
| `git stash drop` | Faz a remoção mais recente da pilha temporária. |
| `git stash drop stash@{X}` | Faz a remoção de posição X salva na pilha temporária. |
| `git stash pop` | Traz a alteração mais recente que foi salva para a branch atual e logo em seguida já faz a remoção dessa alteração da pilha. |

## log
| Comando | Descrição |
| ------ | ------ |
| `git log` | Mostra histórico de alterações em ordem cronológica. |
| `git log --summary` | Mostra modificações detalhadas. |
| `git log --stat` | Mostra histórico de alterações em ordem cronológica e quais arquivos foram alterados. |

## tag
| Comando | Descrição |
| ------ | ------ |
| `git tag` | Faz a listagem de tags. |
| `git tag <nome-da-tag>` | Faz a criação de uma tag no último commit da branch corrente. |
| `git tag <nome-da-tag> -m "<mensagem>"` | Faz a criação de uma tag no último commit da branch corrente juntamente com uma mensagem. |
| `git tag <nome-da-tag> <hash-do-commit>` | Faz a criação de uma tag no commit específico. |
| `git tag <nome-da-tag> <hash-do-commit> -m "<mensagem>"` | Faz a criação de uma tag no commit específico juntamente com uma mensagem. |
| `git tag -d <nome-da-tag>` | Faz a remoção da tag localmente. |

## diff
| Comando | Descrição |
| ------ | ------ |
| `git diff <commit-1> <commit-2>` | Mostra a diferença entre dois commits ou branchs. |

## branch
| Comando | Descrição |
| ------ | ------ |
| `git branch` | Faz a listagem de todas as branches locais. |
| `git branch -r` | Faz a listagem de todas as branches remotas. |
| `git branch -a` | Faz a listagem de todas as branches locais e remotas. |
| `git branch -d <nome-da-branch>` | Faz a remoção de um branch local. |
| `git branch -D <nome-da-branch>` | Força a remoção de um branch local. |
| `git branch -m <nome-antigo> <nome-novo>` | Renomeia uma branch específica localmente que não é a corrente. |
| `git branch -m <nome-novo>` | Renomeia a branch corrente. |

## checkout/pull/push
| Comando | Descrição |
| ------ | ------ |
| `git checkout -` | Muda para a última branch. |
| `git checkout <nome-da-branch>` | Muda para outra branch. |
| `git checkout -b <nome-da-branch>` | Cria uma nova branch e já faz checkout para a mesma. |
| `git checkout -b <nome-da-branch> origin/<nome-da-branch>` | Clona uma branch remota e muda para ela. |
| `git checkout index.html`  | As alterações no arquivo "index.html" que estão no Diretório de trabalho serão descartadas |
| `git checkout -- <file_name.txt>`  | Descarta modificações de um arquivo |
| `git pull` | Repositório local é atualizado com os dados do repositório remoto. |
| `git pull origin <nome-da-branch>` | Recebe alterações do repositório remoto. |
| `git push` | Faz o envio das mudanças comitadas localmente para a origem da branch rastreada. |
| `git push origin --delete <nome-da-branch>` | Faz a remoção de uma branch remota. |
| `git push -u origin <nome-da-branch>` | Faz o envio da branch para o servidor e rastreia com a branch local. |
| `git push --tags` | Faz o envio das tags locais para o servidor. |
| `git push origin <nome-da-tag>` | Faz o envio de uma única tag para o servidor. |
| `git push origin --delete <nome-da-tag>` | Faz a remoção de tag no servidor. |

## reset
| Comando | Descrição |
| ------ | ------ |
| `git reset --hard` | Desfaz todas as alterações que aconteceram em arquivos rastreados. |

## merge
| Comando | Descrição |
| ------ | ------ |
| `git merge <nome-da-branch>` | Mescla as mudanças presentes na <nome_da_branch> na branch corrente. |
| `git merge <nome-da-branch-remota> <nome-da-branch>` | Faz um merge de uma branch em outra branch. |

## cherry-pick
| Comando | Descrição |
| ------ | ------ |
| `git cherry-pick <hash-do-commit>` | Faz a copia de um commit de uma ramificação para outra. |

## clean
| Comando | Descrição |
| ------ | ------ |
| `git clean -n` | Mostra uma lista de arquivos que serão apagados. |
| `git clean -f` | Apaga todos os novos arquivos não rastreados na alteração. |
| `git clean -i` | Mostra uma lista de opções para apagar somente alguns arquivos. |

## fetch / rebase
| Comando | Descrição |
| ------ | ------ |
| `git fetch` | Faz o download das atualizações do repositório remoto e trás para o repositório local. |
| `git rebase <nome-da-branch>` | Aplica os commits da <branch> na branch corrente. |