# O framework CSS Bootstrap

- 20 minutos

## Definição

- kit css pra deixar sua aplicação minimamente bonita
- não substitui um webdesigner dedicado ao serviço, mas enrola muito bem!

## Aplicação

- acelerar seu trabalho de fazer um aplicativo de ponta a ponta e... ficar bonito no final
- você *ainda* tem que aprender algum CSS, mas alguns problemas bem feios já estão resolvidos

## Exemplo

- antes de começar, prepare um projeto. pode inclusive usar o projeto iniciado aula passada
- na parte front-end, use o bower ou o próprio npm pra instalar, caso seu front-end seja com npm também

```bash
bower install bootstrap --save
```

- seja via npm ou [bowie](https://www.youtube.com/watch?v=tRcPA7Fzebw), isso também instalará a versão apropriada do jquery
- o index.html ficaria mais ou menos assim:

```html
<!DOCTYPE html>
<!-- index.html -->
<html>
  <head>
    <!-- bibliotecas do bootstrap -->
    <script type="text/javascript" src="bower_components/jquery/dist/jquery.js"></script>
    <script type="text/javascript" src="bower_components/bootstrap/dist/js/bootstrap.js"></script>
    <link rel="stylesheet" href="bower_components/bootstrap/dist/css/bootstrap.css"/>
    <link rel="stylesheet" href="bower_components/bootstrap/dist/css/bootstrap-theme.css"/>

    <title>Hello Bootstrap!</title>
  </head>
  <body>
    <h1>Usando bootstrap pra bonitificar a aplicação</h1>
    <div class="container well">
      <div class="row">
        <div class="col-xs-4 col-xs-offset-4">
          <div class="alert alert-success" role="alert">
            Olá, eu sou um painel de alerta de sucesso!
          </div>
        </div>
      </div>
    </div>
  </body>
</html>
```

- veja no browser como o seu index.html ficou
- sobre as tags e marcações novas:
  - o ```<link rel="stylesheet" href="..." />``` é como a tag de script, só que para folhas de estilo
  - uma [folha de estilo](https://en.wikipedia.org/wiki/Cascading_Style_Sheets) *(Cascading Style Sheet)* serve para orientar a aperência das tags no corpo do documento html
  - o atributo **class** pode indicar uma ou mais classes. você pode definir as suas, mas por enquanto vamos usar as do bootstrap
  - estas classes e o que cada uma delas faz [encontra-se](http://getbootstrap.com/getting-started/) [documentado](http://getbootstrap.com/css/#grid) [bem](http://getbootstrap.com/javascript/) [aqui](http://getbootstrap.com/components/), mas vamos resumir o básico durante esta aula.

### Grade e container

- a recomendação do bootstrap é colocar todas as coias que você quer mostrar dentro de um [container](http://getbootstrap.com/css/#overview-container)
- containers, por sua vez, podem conter [linhas](http://getbootstrap.com/css/#grid-intro) (rows)
- as linhas, seguindo o raciocínio, podem conter [colunas](http://getbootstrap.com/css/#grid-options) (col-*)
  - a diversão começa com as colunas, pois:
    - colunas variam de acordo com o tamanho do "display". Do menor para o maior: **xs, sm, md, lg**
    - colinas varia de acordo com a grade virtual de 12 colunas, onde 1 é a menor possível e a 12 é a linha inteira
    - isso resulta em nomes de coluna memoráveis: **col-sm-3 col-xs-6 col-md-2**
  - e você pode aplicar várias classes de tamanho distintas! **col-sm-4** e **col-xs-6** podem estar na mesma div
  - várias classes distintas de tamanho ajudam em uma coisa chamada **responsividade** ou **layout adaptativo**
    - um jeito de dizer que seu aplicativo ficará bonito em qualquer tela
- no final, entender o bootstrap é a porta para [frameworks](https://angular-ui.github.io/) mais [pesados](https://material.angularjs.org/latest/)

### Componentes

- [componentes](http://getbootstrap.com/components/#glyphicons-glyphs) ajudam ainda mais a dar melhor aparência ao negócio
- assim como forçamos um pouco a amizade ao dizer que uma div é uma row só por causa da classe css, vamos forçar aqui também.
- cada componente do bootstrap tem suas beneces oferecidas por uma lista de classes especiais e Às vezes por atributos customizados
- um ícone, por exemplo, pode ser incluído assim:

```html
<span class="glyphicon glyphicon-glass"></span>
```

- uma lista de elementos:

```html
<ul class="list-group">
  <li class="list-group-item">
    <span class="badge">14</span>
    Cras justo odio
  </li>
</ul>
```

- um [formulário](http://getbootstrap.com/components/#input-groups-basic):

```html
<form ng-submit="ctl.save()">
  <div class="input-group">
    <span class="input-group-addon" id="basic-addon1">
      <span class="glyphicon glyphicon-user"></span>
    </span>
    <input type="text" class="form-control" ng-model="ctl.user.name"
      placeholder="Username" aria-describedby="basic-addon1">
  </div>
  <div class="input-group">
    <span class="input-group-addon" id="basic-addon2">
      <span class="glyphicon glyphicon-asterisk"></span>
    </span>
    <input type="password" class="form-control" ng-model="ctl.user.password"
      placeholder="Password" aria-describedby="basic-addon2">
  </div>
  <button type="submit" class="btn btn-default">Submit</button>
</form>
```

- [e](http://getbootstrap.com/components/#panels-alternatives) [por](http://getbootstrap.com/components/#nav-tabs) [aí](http://getbootstrap.com/components/#dropdowns) [vai](http://getbootstrap.com/components/#badges)

## Exercício

- use os conceitos de css para deixar a aplicação de reserva de espaços bonita
- a vida é correr atrás de componentes e css que funcionem
- o que foi mostrado aqui é pra lhe dar a direção
- agora, de volta ao aplicativo de fim de curso!

[Voltar](../README.md)
