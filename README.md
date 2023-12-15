# How to Angular(v17)
# Guia para Configuração de Projeto Angular

Este guia oferece um passo a passo detalhado para configurar um ambiente de desenvolvimento Angular em sua máquina local, utilizando a ferramenta Angular CLI. Abrange desde os pré-requisitos até a execução da sua primeira aplicação Angular.

## Pré-requisitos

Antes de começar, é importante estar familiarizado com:

- JavaScript
- HTML
- CSS

Conhecimento em TypeScript é útil, mas não obrigatório.

Você também precisará:
- **Baixe e Instale o NodeJS LTS**: Para mais informações, veja [nodejs.org](https://nodejs.org/).
- **Node.js**: Angular requer uma versão LTS ativa ou LTS de manutenção do Node.js. Verifique a versão do Node.js em seu sistema com:
```
node -v
```
- **npm package manager**: Angular e Angular CLI dependem de pacotes npm. Para instalar pacotes npm, você precisa de um gerenciador de pacotes npm. O npm é instalado com Node.js por padrão. Verifique com:
```
npm -v
```
## Instalação do Angular CLI

O Angular CLI ajuda a criar projetos, gerar código para aplicativos e bibliotecas, e realizar várias tarefas de desenvolvimento, como testes, empacotamento e implantação.

Para instalar o Angular CLI:

1. Abra um terminal e execute:
```
npm install -g @angular/cli
```
2. No Windows, para executar scripts do PowerShell (necessário para binários globais do npm), configure a seguinte política de execução:

```
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```
## Criando um Espaço de Trabalho e Aplicação Inicial

Para desenvolver aplicativos, você precisa criar um espaço de trabalho Angular.

Para criar um novo espaço de trabalho e um aplicativo inicial:

1. Execute no terminal:
```
ng new my-app
```
   Siga as instruções, aceitando os padrões pressionando Enter.
2. Este comando instala os pacotes npm necessários e pode levar alguns minutos.

3. Após a instalação, um novo espaço de trabalho e um aplicativo de boas-vindas serão criados.

## Executando a Aplicação

Para construir e servir seu aplicativo localmente, o Angular CLI inclui um servidor.

1. Navegue até a pasta do espaço de trabalho (`my-app`).

2. Inicie o aplicativo com:
```
cd my-app
ng serve --open
```
   Este comando inicia o servidor e abre seu navegador em `http://localhost:4200/`.

Se tudo estiver correto, você verá a página inicial do seu aplicativo Angular.

### Criando Componentes no Angular

Para criar um componente:

1. No terminal, digite:
```
   ng g c nome-do-componente
```
2. Para criar dentro de uma pasta específica:
```
   ng g c pasta/nome-do-componente
```

### Criando Serviços

Para criar um serviço:

1. No terminal, digite:
```
   ng g s nome-do-servico
```

### Gerenciamento de Módulos

Para criar um módulo:

1. Use o comando:
```
   ng g m nome-do-modulo
```

### Rotas e Navegação

1. Configure rotas em `app-routing.module.ts`.
2. Use `<router-outlet></router-outlet>` no template.

### Construindo e Deploy

Para construir sua aplicação para produção:

1. Execute:
```
   ng build --prod
```

# Guia de Implantação no Netlify

### Pré-requisitos

- Uma aplicação Angular construída.
- Uma conta no Netlify.

### Passos para Implantação

1. Construa sua aplicação Angular para produção:
```
   ng build --prod
```
2. No Netlify, clique em “New site from Git”.
3. Configure as opções de build:
- **Publish directory**: `dist/nome-do-seu-projeto`

### Configurações Adicionais

- **Custom Domain**: Adicione um domínio personalizado nas configurações do site.
- **Redirects**: Crie um arquivo `_redirects` com:
```
  /* /index.html 200
```

### Atualizações Futuras

- Faça push das alterações para o repositório Git para atualizar o site no Netlify
