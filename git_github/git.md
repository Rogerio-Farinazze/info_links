[Inicio](../README.md)
# Git / Github 
## Configurando acesso ao github com chave ssh
- $ ssh-keygen -t ed25519 -C EMAIL_NO_GITHUB@SEUEMAIL.COM | Gerando chave ssh
- $ eval $(ssh-agent -s) | No git bash dentro da pasta .ssh
- Ainda no git bash dentro de .ssh entregar a chave privada | $ ssh-add id_ed25519
- Copiar a chave pública | $ cat id_ed25519.pub
- Acessar github | https://github.com/settings/keys
  - Clicar em NEW SSH KEY 
  - Colar a chave pública e salvar

## Principais Comandos
- $ git init | Cria um repositório Git vazio ou reinicializa um já existente
- $ git add . | Adicione todo o conteúdo do arquivo ao índice 
- $ git commit -m "MENSAGEM DO COMMIT" | Grava as alterações feitas no repositório
- $ git remote add origin URL_DIRETORIO_GITHUB | Adiciona um ramo remoto chamado origin para o repositório na URL_DIRETORIO_GITHUB
- $ git status | Exibe a condição da árvore de trabalho
- $ git push origin main | Atualiza as refs remotas junto com os objetos associados a ela
- $ git pull origin main | Busque e integre-se a outro repositório ou em um ramo local

## Solução de problemas
- O erro fatal: refusing to merge unrelated histories
  - $ git pull origin master --allow-unrelated-histories
- O erro fatal: Your local changes to the following files would be overwritten by merge:
  - $ git reset --hard
  - $ git pull origin main 

## Referências
- [https://dio.me/courses/introducao-ao-git-e-ao-github](https://www.dio.me/courses/introducao-ao-git-e-ao-github)
- [https://git-scm.com/docs](https://git-scm.com/docs)

