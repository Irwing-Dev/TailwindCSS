# Instalando o TailwindCSS

## Como instalar o tailwind (v3.3.3)?
Passo 1 - Inicie um novo projeto npm com "npm init";

Passo 2 - Digite no terminal o comando: "npm install -D tailwindcss";

Passo 3 - Crie o arquivo tailwind.config.js com o comando: "npx tailwindcss init";

### Configurando o tailwind.config.js:

Para configurar este arquivo basta apenas colocar o código: 
```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    './src/**/*.html',
    './src/**/*.js'
],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

## ATENÇÃO!!! Crie uma pasta chamada src e ponha os arquivos: input.css e index.html

Isso porque na configuração acima, definimos que a pasta onde vai ser carregado os arquivos .html ou .js caso tenha, será na pasta src. Olhe o comando:

```
content: [
    './src/**/*.html',
    './src/**/*.js'
]
```

### Configurando o input.css

Passo 1 - Crie o arquivo input.css na psata src

Passo 2 - Importe o Tailwind CSS adicionando a seguinte linha no topo do arquivo:

```
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
```

Obs.: Não se importe com os errinhos que vai dar, eles não vão prejudicar em nada

## Iniciando a compilação com a CLI o tailwind: 

Digite no terminal o seguinte comando: "npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch"

Após isso pode dar um ctrl + c que já vai estar funcionando certinho.

## Configurando o arquivo index.html:

Coloque no head a seguinte linha: ```<link href="../dist/output.css" rel="stylesheet">```

E pronto, o projeto já está rodando