# Git / Github
## Configurando acesso ao github com chave ssh
- Gerando chave ssh 
  $ ssh-keygen -t ed25519 -C EMAIL_NO_GITHUB@SEUEMAIL.COM
- No git bash dentro da pasta .ssh
  $ eval $(ssh-agent -s)
- Ainda no git bash dentro de .ssh entregar a chave privada
  $ ssh-add id_ed25519
- Copiar a chave pública
  $ cat id_ed25519.pub
- Acessar github | https://github.com/settings/keys
  Clicar em NEW SSH KEY 
  Colar a chave pública e salvar