# dev-utils

Ferramentas para customização e melhoria de produtividade no seu ambiente de desenvolvimento

## Extensões do navegador

Obs: Normalmente os navegadores baseados no Chrome oferecem alguma opção para instalar extensões diretamente da loja do Chrome

### JSON Viewer

Formatar conteúdo JSON no navegador

Repositório: https://github.com/tulios/json-viewer

Chrome Webstore: https://chrome.google.com/webstore/detail/json-viewer/gbmdgpbipfallnflgajpaliibnhdgobh

### ColorZilla

Mostra o código hexadecimal ou RGB das cores utilizadas na janela atual

Chrome Webstore: https://chrome.google.com/webstore/detail/colorzilla/bhlhnicpbhignbdhedgjhgdocnmhomnp

### Wappalyzer

Exibe todas as tecnologias utilizadas no site

Chrome Webstore: https://chrome.google.com/webstore/detail/wappalyzer/gppongmhjkpfnbhagpmjfkannfbllamg

### Github Dark Theme

Tema escuro para o site do Github

Chrome Webstore: https://chrome.google.com/webstore/detail/github-dark-theme/odkdlljoangmamjilkamahebpkgpeacp

### Dracula Chrome Theme - Dark and Minimal

Tema Dracula para o Chrome

Chrome Webstore: https://chrome.google.com/webstore/detail/dracula-chrome-theme-dark/gfapcejdoghpoidkfodoiiffaaibpaem

---

## Extensões do Visual Studio Code

### Import Cost

Exibe o tamanho do pacote a ser importado

### Docker

Exibe suas imagens locais e os containers instalados, além de ser uma forma fácil de gerenciá-las

### GitLens

Exibe o nome da última pessoa a editar a linha atual, bem como a data da alteração

### Todo Tree

Basta adicionar um comentário no seguinte formato: `// TODO: Uma breve descrição da tarefa aqui`

Todas as tarefas criadas desta forma serão exibidas na barra lateral clicando no ícone da extensão

### Live share

Compartilhamento de código em tempo real, basta fazer login e compartilhar o link da sessão

### Color Highlight

Extensão que mostra um preview das cores no seu código

Repositório: https://github.com/egonyans/vscode-ext-color-highlight

---

## Customização do Visual Studio Code

### Material Icon Theme

Adiciona icones do tema material aos arquivos

### Dracula Official

Tema dracula para Visual Studio Code

### Fira Code

Instalar a fonte Fira Code e habilitar a propriedade `fontLigatures` dará uma estilização diferenciada aos operadores

---

## Customização do terminal

Mostrar branch atual no terminal do linux ou WSL

basta adicionar esse trecho de código no arquivo `~/.bashrc`

```shell
# Show git branch name
force_color_prompt=yes
color_prompt=yes
parse_git_branch() {
git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}
if [ "$color_prompt" = yes ]; then
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[01;31m\]$(parse_git_branch)\[\033[00m\]\$ '
else
PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w$(parse_git_branch)\$ '
fi
unset color_prompt force_color_prompt
```

Depois você vai precisar reiniciar o computador, encerrar sua sessão ou recarregar o arquivo de configurações do terminal
source ~/.bashrc
