# Instalando o Github-CLI

Link do projeto para instalação no Linux

https://github.com/cli/cli/blob/trunk/docs/install_linux.md#rpm

**Instalação para RPM packages:**

- Amazon Linux 2
- CentOS
- Fedora
- Red Hat Enterprise Linux
- openSUSE
- SUSE

```bash
sudo dnf install dnf5-plugins
sudo dnf config-manager addrepo --from-repofile=https://cli.github.com/packages/rpm/gh-cli.repo
sudo dnf install gh --repo gh-cli
```

**1. Autentique com o GitHub CLI**

```bash
gh auth login
```
Siga o fluxo interativo: escolha GitHub.com → SSH → Login with a web browser.

**2. Inicialize o repositório Git na pasta do projeto**

```bash
cd caminho/para/seu/projeto
git init
```

**3. Adicione os arquivos ao Git**

```bash
git add 
```

**4. Faça o commit**

```bash
git commit -m "upload ..."
```

**5. Defina a branch como `main`**

```bash
git branch -M main
```

**6. Crie o repositório no GitHub e faça o push**

```bash
gh repo create nome-do-repositorio --public --source=. --remote=origin --push
```

Pronto! Rode `gh repo view --web` para abrir o repositório no navegador.

