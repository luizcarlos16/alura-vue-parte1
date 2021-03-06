# Curso de Vue.js parte 1: construindo Single Page Applications
![](http://www.alura.com.br/assets/api/share/curso-vue-parte1.png)
## Pré-requisitos
> [NodeJS](https://nodejs.org/)
```
Vue CLI
```
### Aula 01 - Bem começado metade feito
Instalar o CLI do Vue Globalmente
```
npm install -g vue-cli@2.7.0
```
Obs: requer privilégios de Administrador

Verificar a versão do Vue
```
 vue --version
```
Novo projeto a partir de um template
```
vue init webpack-simple alurapic
```

Iniciar o projeto
```
   cd alurapic
   npm install              //baixar as dependências
   npm run dev              //subir o servidor
```
- Interpolação
- Live-reloading

`` Revisão ``
```
instalar e utilizar o Vue CLI
criar do zero um novo projeto
estrutura fundamental do projeto
arquivos de template .vue
estrutura de um template
relação entre index.html, main.js e App.vue
como a renderização de um template é feita
data binding unidirecional através de interpolação
o mecanismo de live reloading
```


### Aula 02 - Adequando o template gerado

```
data binding unidirecional em atributos através da diretiva v-bind
atalho para v-bind
a diretiva v-for
```

### Aula 03 - Integração com API de terceiros
[API Fotos](https://s3.amazonaws.com/caelum-online-public/vue/api.zip)

Revisão
```
a subir uma API para ser consumida pela nossa aplicação
a entender a separação entre cliente e API
a baixar e registrar o módulo VueResource
o suporte à lifecycle hooks que todo componente possui
que recursos no global view object ficam disponíveis para todas as outras view
consumir uma API através de $http
o conceito de promise
enxergar ainda melhor o poder do data binding
```

### Alura 04 - Criando componentes e encapsulamento de view

```
a estilizar um componente
boa prática na organização do projeto
a criar um componente reutilizável
como passar parâmetro para um componente (comunicação)
o conceito de slot e preservação de conteúdo
importação de um componente em outro
a definir e delimitar o escopo de estilos ao componente no qual foram declarados
```

### Aula 05 - Melhorando a UX com animações
```
a diretiva v-on e como lidar com eventos do JavaScript
atalho para diretiva v-on
diferença de v-on para v-bind
a filtrar uma lista
compreender o uso de computed property
que podemos acessar qualquer propriedade de data através de this
a diretiva v-show
detalhe entre v-show e slots
como realizar transições com auxílio do componente transition
a criar mais um componente
```

### Aula 06 - Single Page Application e criação de rotas

```
a criar um novo componente/página
o conceito de Single Page Application
extrair de App.vue um componente de página, separando responsabilidades
a baixar e registrar o módulo VueRouter
criar rotas da aplicação
o componente router-view
o modo history vs hash
a criar um menu baseado em nossas configurações de rota
a tornar o menu um componente
executar efeito de transição na troca de páginas
a validar propriedades em um componente
```

### Aula 07 - Um pouco mais sobre componentes
```
a criar um novo componente reutilizável
a criar nossos próprios eventos
a aplicar classes condicionalmente
a diferença do valor passado para a propriedade de um componente sem bind e com bind
a validar propriedades de componentes
```

