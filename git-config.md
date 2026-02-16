# Configurando o Git 

## Gerando uma chave SSH

No console:

```
ssh-keygen -t ed25519 -C "idfelipemalatesta@gmail.com"
```

Certifique se o arquivo foi criado

```
cat ~/.ssh/id_ed25519.pub
```

Na conta do GitHub: Settings -> SSH and GPG keys -> New SSH key

Cole o conteúdo do arquivo .pub

Após adicionar a chave na sua conta, teste a conexão do ssh com o Github

Verifique se há fingerprint corresponde: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/githubs-ssh-key-fingerprints

```
ssh -T git@github.com
```

Autorizado, será gerado o 2 arquivos known_host, copie as chaves do arquivo

```
cat ~/.ssh/known_hosts
```

Confirme se todas as fingerptins do arquivo correspondem às do site (devem ser 3): https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/githubs-ssh-key-fingerprints

Se tudo estiver correto, pode remover o arquivo known_hosts.old

## Configurando usuário e email

Execute o seguinte comando para especificar quem assinará seus commits com um nome de usuário e e-mail:

```
git config --global user.name "Felipe Malatesta"
git config --global user.email idfelipemalatesta@gmail.com
git config --global init.defaultBranch main
```

O arquivo ~/.gitconfig deve ter sido criado

```
cat ~/.gitconfig
```

Feito! Já é possível clonar um repositório via SSH.
