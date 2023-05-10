# node_tsx
Node Base TypeScript Project

Abra um terminal e crie uma nova pasta para sua aplicação.

Dentro da pasta, execute o seguinte comando para iniciar um projeto Node.js vazio:
```
npm init -y
```
Instale as dependências necessárias para o projeto:
```
npm install --save-dev typescript ts-node @types/node
```
typescript é o pacote que nos permite usar TypeScript no Node.js
ts-node é uma ferramenta que nos permite executar código TypeScript diretamente no Node.js, sem a necessidade de compilar primeiro.
@types/node fornece tipos para o Node.js.
Crie um arquivo tsconfig.json na raiz do projeto com o seguinte conteúdo:
```
{
  "compilerOptions": {
    "target": "ES2019",
    "module": "commonjs",
    "strict": true,
    "esModuleInterop": true,
    "outDir": "./dist",
    "sourceMap": true
  },
  "exclude": [
    "node_modules"
  ]
}
```
Este arquivo define as opções do compilador TypeScript. A opção outDir define o diretório onde os arquivos compilados serão salvos, enquanto sourceMap gera arquivos de mapeamento para depuração.

Crie um arquivo src/index.ts com o seguinte conteúdo:
```
console.log('Hello, TypeScript!');
```
Adicione um script ao arquivo package.json para executar o arquivo TypeScript:
```
{
  "scripts": {
    "start": "ts-node src/index.ts"
  }
}
```
Execute a aplicação com o seguinte comando:
```
npm start
```
O console exibirá a mensagem "Hello, TypeScript!".

O arquivo package.json pode ser algo como:
```
{
  "name": "minha-aplicacao",
  "version": "1.0.0",
  "description": "Uma breve descrição da minha aplicação",
  "main": "dist/index.js",
  "scripts": {
    "start": "ts-node src/index.ts",
    "build": "tsc"
  },
  "keywords": [
    "node",
    "typescript"
  ],
  "author": "Seu Nome",
  "license": "MIT",
  "dependencies": {},
  "devDependencies": {
    "@types/node": "^16.3.1",
    "ts-node": "^10.2.1",
    "typescript": "^4.3.5"
  }
}
```
