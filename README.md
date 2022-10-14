# Subindo uma aplicação React para o GitHub Pages

Crie um repositório e suba a sua aplicação react para ele, seguindo os passos tradicionais.

``` git init ```

```git add README.md```

``git commit -m "first commit"``

````git branch -M main````

`git remote add origin https://github.com/{UserName}/{repoName}.git
`

```git push -u origin main```

## Depois de subir o seu repositório

Digite no terminal. (~estando na pasta do projeto~)

``$ npm install gh-pages --save-dev``

## Abra o arquivo package.json

E cole a linha abaixo nas primeiras linhas (~depois da chave "version" e antes da chave "dependencies"~)

``"homepage": "https://{username}.github.io/{nome-do-repositorio}",``

substitua '{username}' pelo seu usuário do github e '{nome-do-repositorio}' pelo nome do repositório.

```
Exemplo:

 "homepage": "https://Megas-MDN.github.io/project-react",

```

## Ainda no package.json

Vá até a chave "scripts" e dentro dela acrescente as chaves:

    "predeploy": "npm run build",
    "deploy": "gh-pages -d build",

```
Exemplo: 
  "scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build",
    ...

},
```

## Depois das alterações faça a atualização do repositório

```
git add .
git commit -m "Realizando as modificações para gh-pages"
git push
```

## Faça o deploy

Por fim rode no terminal o seguinte comando:

``$ npm run deploy``

### Entre no github pages e verifique sua aplicação

```shell
https://{userName}.github.io/{repoName}/
```

Exemplo: 

    https://megas-mdn.github.io/project-react/


## Referências

1. [ Repositório Original (em inglês) ](https://github.com/gitname/react-gh-pages)
2. [ `create-react-app` guia oficial de Deploy](https://create-react-app.dev/docs/deployment/#github-pages)


