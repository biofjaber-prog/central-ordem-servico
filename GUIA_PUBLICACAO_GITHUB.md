# Guia rápido para publicar no GitHub Pages

## 1. Crie o repositório
No GitHub, crie um repositório chamado, por exemplo:

`central-ordem-servico`

Deixe como **Public** se estiver usando GitHub Free e quiser publicar com GitHub Pages.

## 2. Envie os arquivos
Extraia o ZIP e envie **os arquivos de dentro da pasta**, não o ZIP fechado.

A estrutura precisa ficar assim na raiz do repositório:

```text
index.html
indicadores.html
README.md
.nojekyll
.gitignore
.github/workflows/pages.yml
```

## 3. Ative o GitHub Pages
No repositório:

1. Vá em **Settings**.
2. Clique em **Pages**.
3. Em **Build and deployment**, escolha **GitHub Actions**.
4. Salve, se necessário.

## 4. Aguarde o deploy
Depois do push na branch `main`, vá na aba **Actions** e aguarde o workflow finalizar.

A URL normalmente fica neste formato:

`https://SEU_USUARIO.github.io/NOME_DO_REPOSITORIO/`

Exemplo:

`https://biofjaber-prog.github.io/central-ordem-servico/`

## Atenção de segurança
Este projeto é estático. Tudo que estiver dentro de HTML, CSS e JavaScript poderá ser visualizado por quem acessar o código publicado.

O login atual é apenas uma barreira visual no navegador, não uma autenticação segura de sistema. Para uso real com dados sensíveis, use backend, banco de dados e autenticação protegida.


## Atualização dos indicadores pelo sistema

Esta versão usa a API real do GitHub para gravar o arquivo `data/store.json`. O token precisa ser fine-grained, restrito ao repositório `central-ordem-servico`, com permissão `Contents: Read and write`.

