<div id="app">
  <div ui-view></div>
</div>
<div id="app"></div>

<div id="app"></div>

<div id="app"></div>


<div style="text-align:center">
  <h1>
    Welcome to {{ Analista TI }}!
  h1>
  <img width="300" alt="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSzK3Ny4_-marl_PbJmvR6NxdIfjeFkHEFXtQ&usqp=CAU" src="data: ">
div>

 <div style="text-align:center">
  <h1>
    Welcome to {{ Analista TI }}!
  h1>
  <button (click)="changeTitle()">Alterar títulobutton>
div>

 <div style="text-align:center">
  <h1>
    Welcome {{Matheus}} {{Matheus}}!
  h1>
  <button (click)="changeTitle()">Alterar títulobutton>
div>

XHTML
<h1 class="title" *ngFor="let artigo of appService.artigos">
 <a href="/artigo/{{artigo._id}}">
 {{ aritgo de TI }}
 </a>
</h1>
1
2
3
4
5
<h1 class="title" *ngFor="let artigo of appService.artigos">
 <a href="/artigo/{{artigo._id}}">
 {{ artigo desenvolvimento e programação}}
 </a>
</h1>
<nav class="navbar navbar-default">
    <div class="container-fluid">
    <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
            <a class="navbar-brand" href="#">Menu</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav">
                <li class="dropdown">
                    <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Cadastro <span class="caret"></span></a>
                    <ul class="dropdown-menu">
                        <li><a href="#">Setor</a></li>
                        <li><a href="#">classe</a></li>
                    </ul>
                </li>
            </ul>
        </div>
        <!-- /.navbar-collapse -->
    </div>
    <!-- /.container-fluid -->
</nav>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <div class="box-header">
                    <div class="box-tools">
                        <div class="input-group">
                            <button class="btn btn-sm btn-primary" (click)="addSetor()"><i class="glyphicon glyphicon-plus"></i>Adicionar</button>
                            <input type="text" name="table_search" class="form-control input-sm pull-right" style="width: 150px;" placeholder="Pesquisa Setor" [(ngModel)]="filtro" />
                            <div class="input-group-btn">
                                <button class="btn btn-sm btn-default"><i class="fa fa-search"></i></button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="box-body table-responsive no-padding">
                    <table class="table table-hover">
                        <tr>
                            <th>Código</th>
                            <th>Descrição</th>
                            <th>Ação</th>
                        </tr>
                        <tr *ngFor="let setor of obterSetores()">
                            <td></td>
                            <td></td>
                            <td>
                                <div class="buttons">
                                    <button class="btn btn-success btn-xs" (click)="editSetor(setor)">
                                                <span class="glyphicon glyphicon-edit" aria-hidden="true"></span>
                                                Editar
                                            </button>
                                    <button class="btn btn-danger btn-xs" (click)="delSetor(setor)">
                                                <span class="glyphicon glyphicon-trash" aria-hidden="true"></span>
                                                Exluir
                                            </button>
                                </div>
                            </td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <form name="form" (ngSubmit)="save()" #setor="ngForm">
                    <div class="box-header">
                        <div class="box-tools">
                            <div class="input-group">
                                <button type="submit" class="btn btn-sm btn-success" [disabled]="!setor.form.valid"><i name="save" id="save" class="glyphicon glyphicon-ok"></i>Salvar</button>
                                <button class="btn btn-sm btn-danger" (click)="cancel()"><i class="glyphicon glyphicon-remove"></i>Cancelar</button>
                            </div>
                        </div>
                    </div>
                    <div class="box box-primary">
                        <div class="box-header">
                            <h3 class="box-title">Informe os dados</h3>
                        </div>
                        <div class="form-group">
                            <input type="text" id="nameSetor" name="nameSetor" class="form-control" placeholder="Informe a descrição do setor" maxlength="100" [(ngModel)]="model.descricao" #nameSetor="ngModel" required/>
                            <span [hidden]="nameSetor.valid || nameSetor.pristine" class="alert alert-danger">descrição do setor</span>
                        </div>

                    </div>
                    <!-- /.box -->

                </form>
            </div>
        </div>
    </div>
</section>
<nav class="navbar navbar-default">
    <div class="container-fluid">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
            <a class="navbar-brand" href="#">Menu</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav">
                <li class="dropdown">
                    <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Cadastro <span class="caret"></span></a>
                    <ul class="dropdown-menu">
                        //Alterado href="#" para [TILink]
                        <li><a [routerLink]="['/app-setor']">Setor</a></li>
                        <li><a href="#">Pesquisa</a></li>
                    </ul>
                </li>
            </ul>
        </div>
        <!-- /.navbar-collapse -->
    </div>
    <!-- /.container-fluid -->
</nav>

//Incluí o router-outlet
<router-outlet></router-outlet>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <div class="box-header">
                    <div class="box-tools">
                        <div class="input-group">
                            <button class="btn btn-sm btn-primary" (click)="addProduto()"><i class="glyphicon glyphicon-plus"></i>Adicionar</button>
                            <input type="text" name="table_search" class="form-control input-sm pull-right" style="width: 150px;" placeholder="Pesquisa Produto" [(ngModel)]="filtro" />
                            <div class="input-group-btn">
                                <button class="btn btn-sm btn-default"><i class="fa fa-search"></i></button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="box-body table-responsive no-padding">
                    <table class="table table-hover">
                        <tr>
                            <th>Código</th>
                            <th>Descrição</th>
                            <th>Barra</th>
                            <th>Setor</th>
                            <th>Ação</th>
                        </tr>
                        <tr *ngFor="let produto of obterProdutos()">
                            <td></td>
                            <td></td>
                            <td></td>
                            <td></td>
                            <td>
                                <div class="buttons">
                                    <button class="btn btn-success btn-xs" (click)="editProduto(produto)">
                                                <span class="glyphicon glyphicon-edit" aria-hidden="true"></span>
                                                Editar
                                            </button>
                                    <button class="btn btn-danger btn-xs" (click)="delProduto(produto)">
                                                <span class="glyphicon glyphicon-trash" aria-hidden="true"></span>
                                                Exluir
                                            </button>
                                </div>
                            </td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <form (ngSubmit)="save()" #produtoForm="ngForm">
                    <div class="box-header">
                        <div class="box-tools">
                            <div class="input-group">
                                <button type="submit" class="btn btn-sm btn-success" [disabled]="!produtoForm.form.valid"><i name="save" id="save" class="glyphicon glyphicon-ok"></i>Salvar</button>
                                <button class="btn btn-sm btn-danger" (click)="cancel()"><i class="glyphicon glyphicon-remove"></i>Cancelar</button>
                            </div>
                        </div>
                    </div>
                    <div class="box box-primary">
                        <div class="box-header">
                            <h3 class="box-title">Informe os dados</h3>
                        </div>
                        <div class="form-group">
                            <input type="text" id="descricao" name="descricao" class="form-control" placeholder="Informe a descrição do produto" maxlength="100" [(ngModel)]="model.descricao" #descricao="ngModel" required/>
                            <div [hidden]="descricao.valid || descricao.pristine" class="alert alert-danger">Descrição de sua atividade</div>
                        </div>

                        <div class="form-group">
                            <input type="text" id="barra" name="barra" class="form-control" placeholder="Informe o código de barras" maxlength="14" [(ngModel)]="model.barra" #barra="ngModel" required/>
                            <div [hidden]="barra.valid || barra.pristine" class="alert alert-danger">Código de barras</div>
                        </div>

                        <div class="form-group">
                            <select class="form-control" id="setor" required [(ngModel)]="model.id_setor" name="setor" #setor="ngModel">
                                    <option *ngFor="let setor of setores" [value]="setor.id"></option>
                            </select>
                            <div [hidden]="setor.valid || setor.pristine" class="alert alert-danger">Setor</div>
                        </div>

                    </div>
                    <!-- /.box -->

                </form>
            </div>
        </div>
    </div>
</section>
<nav class="navbar navbar-default">
    <div class="container-fluid">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
            <a class="navbar-brand" href="#">Menu</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav">
                <li class="dropdown">
                    <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Cadastro <span class="caret"></span></a>
                    <ul class="dropdown-menu">
                        <li><a [routerLink]="['/app-setor']">Setor</a></li>
                        //Alterado href="#" para [TILink]
                        <li><a [routerLink]="['/app-produto']">artigos</a></li>
                        <li><a [routerLink]="['/app-produto']">Trabalhos</a></li>
                        <li><a [routerLink]="['/app-produto']">Projetos</a></li>


                    </ul>
                </li>
            </ul>
        </div>
        <!-- /.navbar-collapse -->
    </div>
    <!-- /.container-fluid -->
</nav>

<router-outlet></router-outlet>
<html ng-app="app">
<head>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.21/angular.min.js"></script>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.0rc1/angular-route.min.js"></script>
    <link href="~/Content/bootstrap.min.css" rel="stylesheet" />
    <script src="~/Scripts/jquery-2.1.1.min.js"></script>
    <script src="~/Scripts/bootstrap.js"></script>
    <script src="~/app/app.js"></script>
    <title>ExampleAngularJS</title>
    @RenderSection("JavascriptHeader", required: false)
</head>
<body>
    <div class="row">
        <div class="navbar navbar-default">
            <div class="navbar-header">
                <ul class="navbar navbar-nav">
                    <li>
                        <span class="navbar navbar-brand">Registration</span>
                    </li>
                </ul>
            </div>
            <div class="navbar-collapse colapse">
                <ul class="nav navbar-nav">
                    <li><a href="/Registration/Courses">Courses</a></li>
                    <li><a href="/Registration/Students">Students</a></li>
                </ul>
            </div>
        </div>
    </div>
    @RenderBody()
<html ng-app="myApp">
<head>
    <title>CRUD AngularJS</title>
    <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/angularjs/1.4.3/angular.min.js"></script>
</head>
<body ng-controller="MainCtrl">
    <form ng-submit="submit()">
        Nome<br>
            <input type="text" ng-model="nome"><br>
        Email<br>
            <input type="text" ng-model="email"><br>
        Senha<br>
            <input type="password" ng-model="senha"><br>
        <input type="submit" id="submit" value="Submit" />
    </form>
<html>
<head>
    <title>Angular2</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <meta http-equiv="x-ua-compatible" content="ie=edge">
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.min.css">
    <!--<link rel="stylesheet" href="../styles.css">-->
    <!-- Polyfill(s) for older browsers -->
    <script src="../node_modules/core-js/client/shim.min.js"></script>
    <script src="../node_modules/zone.js/dist/zone.js"></script>
    <script src="../node_modules/reflect-metadata/Reflect.js"></script>
    <script src="../node_modules/systemjs/dist/system.src.js"></script>
    <script src="../systemjs.config.js"></script>
    <script>
      System.import('app').catch(function(err){ console.error(err); });
    </script>
</head>
<body>
    <my-app>Carregando...</my-app>
    <div class="container">
   <div class="row">
      <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12 col-xl-12">
          <a href="#" class="btn btn-success">Novo</a>
          <table class="table table-striped table-hover">   
              <thead>
                  <tr>
                    <th>Nome</th>
                    <th>Email</th>
                    <th>Telefone</th>
                    <th>Deletar</th>
                  </tr>
              </thead>
              <tbody>  
                 <tr *ngFor = "let c of clientes">
             <td>{{c.nome}}</td>
             <td>{{c.email}}</td>
             <td>{{c.telefone}}</td>
                  <td><button class="btn btn-danger">Deletar</button></td>
                </tr>
              </tbody>
          </table>
      </div>
   </div>
</div>

<div id="app"></div>


<div style="text-align:center">
  <h1>
    Welcome to {{ Analista TI }}!
  h1>
  <img width="300" alt="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSzK3Ny4_-marl_PbJmvR6NxdIfjeFkHEFXtQ&usqp=CAU" src="data: ">
div>

 <div style="text-align:center">
  <h1>
    Welcome to {{ Analista TI }}!
  h1>
  <button (click)="changeTitle()">Alterar títulobutton>
div>

 <div style="text-align:center">
  <h1>
    Welcome {{Matheus}} {{Matheus}}!
  h1>
  <button (click)="changeTitle()">Alterar títulobutton>
div>

XHTML
<h1 class="title" *ngFor="let artigo of appService.artigos">
 <a href="/artigo/{{artigo._id}}">
 {{ aritgo de TI }}
 </a>
</h1>
1
2
3
4
5
<h1 class="title" *ngFor="let artigo of appService.artigos">
 <a href="/artigo/{{artigo._id}}">
 {{ artigo desenvolvimento e programação}}
 </a>
</h1>
<nav class="navbar navbar-default">
    <div class="container-fluid">
    <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
            <a class="navbar-brand" href="#">Menu</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav">
                <li class="dropdown">
                    <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Cadastro <span class="caret"></span></a>
                    <ul class="dropdown-menu">
                        <li><a href="#">Setor</a></li>
                        <li><a href="#">classe</a></li>
                    </ul>
                </li>
            </ul>
        </div>
        <!-- /.navbar-collapse -->
    </div>
    <!-- /.container-fluid -->
</nav>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <div class="box-header">
                    <div class="box-tools">
                        <div class="input-group">
                            <button class="btn btn-sm btn-primary" (click)="addSetor()"><i class="glyphicon glyphicon-plus"></i>Adicionar</button>
                            <input type="text" name="table_search" class="form-control input-sm pull-right" style="width: 150px;" placeholder="Pesquisa Setor" [(ngModel)]="filtro" />
                            <div class="input-group-btn">
                                <button class="btn btn-sm btn-default"><i class="fa fa-search"></i></button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="box-body table-responsive no-padding">
                    <table class="table table-hover">
                        <tr>
                            <th>Código</th>
                            <th>Descrição</th>
                            <th>Ação</th>
                        </tr>
                        <tr *ngFor="let setor of obterSetores()">
                            <td></td>
                            <td></td>
                            <td>
                                <div class="buttons">
                                    <button class="btn btn-success btn-xs" (click)="editSetor(setor)">
                                                <span class="glyphicon glyphicon-edit" aria-hidden="true"></span>
                                                Editar
                                            </button>
                                    <button class="btn btn-danger btn-xs" (click)="delSetor(setor)">
                                                <span class="glyphicon glyphicon-trash" aria-hidden="true"></span>
                                                Exluir
                                            </button>
                                </div>
                            </td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <form name="form" (ngSubmit)="save()" #setor="ngForm">
                    <div class="box-header">
                        <div class="box-tools">
                            <div class="input-group">
                                <button type="submit" class="btn btn-sm btn-success" [disabled]="!setor.form.valid"><i name="save" id="save" class="glyphicon glyphicon-ok"></i>Salvar</button>
                                <button class="btn btn-sm btn-danger" (click)="cancel()"><i class="glyphicon glyphicon-remove"></i>Cancelar</button>
                            </div>
                        </div>
                    </div>
                    <div class="box box-primary">
                        <div class="box-header">
                            <h3 class="box-title">Informe os dados</h3>
                        </div>
                        <div class="form-group">
                            <input type="text" id="nameSetor" name="nameSetor" class="form-control" placeholder="Informe a descrição do setor" maxlength="100" [(ngModel)]="model.descricao" #nameSetor="ngModel" required/>
                            <span [hidden]="nameSetor.valid || nameSetor.pristine" class="alert alert-danger">descrição do setor</span>
                        </div>

                    </div>
                    <!-- /.box -->

                </form>
            </div>
        </div>
    </div>
</section>
<nav class="navbar navbar-default">
    <div class="container-fluid">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
            <a class="navbar-brand" href="#">Menu</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav">
                <li class="dropdown">
                    <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Cadastro <span class="caret"></span></a>
                    <ul class="dropdown-menu">
                        //Alterado href="#" para [TILink]
                        <li><a [routerLink]="['/app-setor']">Setor</a></li>
                        <li><a href="#">Pesquisa</a></li>
                    </ul>
                </li>
            </ul>
        </div>
        <!-- /.navbar-collapse -->
    </div>
    <!-- /.container-fluid -->
</nav>

//Incluí o router-outlet
<router-outlet></router-outlet>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <div class="box-header">
                    <div class="box-tools">
                        <div class="input-group">
                            <button class="btn btn-sm btn-primary" (click)="addProduto()"><i class="glyphicon glyphicon-plus"></i>Adicionar</button>
                            <input type="text" name="table_search" class="form-control input-sm pull-right" style="width: 150px;" placeholder="Pesquisa Produto" [(ngModel)]="filtro" />
                            <div class="input-group-btn">
                                <button class="btn btn-sm btn-default"><i class="fa fa-search"></i></button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="box-body table-responsive no-padding">
                    <table class="table table-hover">
                        <tr>
                            <th>Código</th>
                            <th>Descrição</th>
                            <th>Barra</th>
                            <th>Setor</th>
                            <th>Ação</th>
                        </tr>
                        <tr *ngFor="let produto of obterProdutos()">
                            <td></td>
                            <td></td>
                            <td></td>
                            <td></td>
                            <td>
                                <div class="buttons">
                                    <button class="btn btn-success btn-xs" (click)="editProduto(produto)">
                                                <span class="glyphicon glyphicon-edit" aria-hidden="true"></span>
                                                Editar
                                            </button>
                                    <button class="btn btn-danger btn-xs" (click)="delProduto(produto)">
                                                <span class="glyphicon glyphicon-trash" aria-hidden="true"></span>
                                                Exluir
                                            </button>
                                </div>
                            </td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <form (ngSubmit)="save()" #produtoForm="ngForm">
                    <div class="box-header">
                        <div class="box-tools">
                            <div class="input-group">
                                <button type="submit" class="btn btn-sm btn-success" [disabled]="!produtoForm.form.valid"><i name="save" id="save" class="glyphicon glyphicon-ok"></i>Salvar</button>
                                <button class="btn btn-sm btn-danger" (click)="cancel()"><i class="glyphicon glyphicon-remove"></i>Cancelar</button>
                            </div>
                        </div>
                    </div>
                    <div class="box box-primary">
                        <div class="box-header">
                            <h3 class="box-title">Informe os dados</h3>
                        </div>
                        <div class="form-group">
                            <input type="text" id="descricao" name="descricao" class="form-control" placeholder="Informe a descrição do produto" maxlength="100" [(ngModel)]="model.descricao" #descricao="ngModel" required/>
                            <div [hidden]="descricao.valid || descricao.pristine" class="alert alert-danger">Descrição de sua atividade</div>
                        </div>

                        <div class="form-group">
                            <input type="text" id="barra" name="barra" class="form-control" placeholder="Informe o código de barras" maxlength="14" [(ngModel)]="model.barra" #barra="ngModel" required/>
                            <div [hidden]="barra.valid || barra.pristine" class="alert alert-danger">Código de barras</div>
                        </div>

                        <div class="form-group">
                            <select class="form-control" id="setor" required [(ngModel)]="model.id_setor" name="setor" #setor="ngModel">
                                    <option *ngFor="let setor of setores" [value]="setor.id"></option>
                            </select>
                            <div [hidden]="setor.valid || setor.pristine" class="alert alert-danger">Setor</div>
                        </div>

                    </div>
                    <!-- /.box -->

                </form>
            </div>
        </div>
    </div>
</section>
<nav class="navbar navbar-default">
    <div class="container-fluid">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
            <a class="navbar-brand" href="#">Menu</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav">
                <li class="dropdown">
                    <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Cadastro <span class="caret"></span></a>
                    <ul class="dropdown-menu">
                        <li><a [routerLink]="['/app-setor']">Setor</a></li>
                        //Alterado href="#" para [TILink]
                        <li><a [routerLink]="['/app-produto']">artigos</a></li>
                        <li><a [routerLink]="['/app-produto']">Trabalhos</a></li>
                        <li><a [routerLink]="['/app-produto']">Projetos</a></li>


                    </ul>
                </li>
            </ul>
        </div>
        <!-- /.navbar-collapse -->
    </div>
    <!-- /.container-fluid -->
</nav>

<router-outlet></router-outlet>
<html ng-app="app">
<head>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.21/angular.min.js"></script>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.0rc1/angular-route.min.js"></script>
    <link href="~/Content/bootstrap.min.css" rel="stylesheet" />
    <script src="~/Scripts/jquery-2.1.1.min.js"></script>
    <script src="~/Scripts/bootstrap.js"></script>
    <script src="~/app/app.js"></script>
    <title>ExampleAngularJS</title>
    @RenderSection("JavascriptHeader", required: false)
</head>
<body>
    <div class="row">
        <div class="navbar navbar-default">
            <div class="navbar-header">
                <ul class="navbar navbar-nav">
                    <li>
                        <span class="navbar navbar-brand">Registration</span>
                    </li>
                </ul>
            </div>
            <div class="navbar-collapse colapse">
                <ul class="nav navbar-nav">
                    <li><a href="/Registration/Courses">Courses</a></li>
                    <li><a href="/Registration/Students">Students</a></li>
                </ul>
            </div>
        </div>
    </div>
    @RenderBody()
<html ng-app="myApp">
<head>
    <title>CRUD AngularJS</title>
    <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/angularjs/1.4.3/angular.min.js"></script>
</head>
<body ng-controller="MainCtrl">
    <form ng-submit="submit()">
        Nome<br>
            <input type="text" ng-model="nome"><br>
        Email<br>
            <input type="text" ng-model="email"><br>
        Senha<br>
            <input type="password" ng-model="senha"><br>
        <input type="submit" id="submit" value="Submit" />
    </form>
<html>
<head>
    <title>Angular2</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <meta http-equiv="x-ua-compatible" content="ie=edge">
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.min.css">
    <!--<link rel="stylesheet" href="../styles.css">-->
    <!-- Polyfill(s) for older browsers -->
    <script src="../node_modules/core-js/client/shim.min.js"></script>
    <script src="../node_modules/zone.js/dist/zone.js"></script>
    <script src="../node_modules/reflect-metadata/Reflect.js"></script>
    <script src="../node_modules/systemjs/dist/system.src.js"></script>
    <script src="../systemjs.config.js"></script>
    <script>
      System.import('app').catch(function(err){ console.error(err); });
    </script>
</head>
<body>
    <my-app>Carregando...</my-app>
    <div class="container">
   <div class="row">
      <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12 col-xl-12">
          <a href="#" class="btn btn-success">Novo</a>
          <table class="table table-striped table-hover">   
              <thead>
                  <tr>
                    <th>Nome</th>
                    <th>Email</th>
                    <th>Telefone</th>
                    <th>Deletar</th>
                  </tr>
              </thead>
              <tbody>  
                 <tr *ngFor = "let c of clientes">
             <td>{{c.nome}}</td>
             <td>{{c.email}}</td>
             <td>{{c.telefone}}</td>
                  <td><button class="btn btn-danger">Deletar</button></td>
                </tr>
              </tbody>
          </table>
      </div>
   </div>
</div>

<div id="app"></div>


<div style="text-align:center">
  <h1>
    Welcome to {{ Analista TI }}!
  h1>
  <img width="300" alt="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSzK3Ny4_-marl_PbJmvR6NxdIfjeFkHEFXtQ&usqp=CAU" src="data: ">
div>

 <div style="text-align:center">
  <h1>
    Welcome to {{ Analista TI }}!
  h1>
  <button (click)="changeTitle()">Alterar títulobutton>
div>

 <div style="text-align:center">
  <h1>
    Welcome {{Matheus}} {{Matheus}}!
  h1>
  <button (click)="changeTitle()">Alterar títulobutton>
div>

XHTML
<h1 class="title" *ngFor="let artigo of appService.artigos">
 <a href="/artigo/{{artigo._id}}">
 {{ aritgo de TI }}
 </a>
</h1>
1
2
3
4
5
<h1 class="title" *ngFor="let artigo of appService.artigos">
 <a href="/artigo/{{artigo._id}}">
 {{ artigo desenvolvimento e programação}}
 </a>
</h1>
<nav class="navbar navbar-default">
    <div class="container-fluid">
    <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
            <a class="navbar-brand" href="#">Menu</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav">
                <li class="dropdown">
                    <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Cadastro <span class="caret"></span></a>
                    <ul class="dropdown-menu">
                        <li><a href="#">Setor</a></li>
                        <li><a href="#">classe</a></li>
                    </ul>
                </li>
            </ul>
        </div>
        <!-- /.navbar-collapse -->
    </div>
    <!-- /.container-fluid -->
</nav>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <div class="box-header">
                    <div class="box-tools">
                        <div class="input-group">
                            <button class="btn btn-sm btn-primary" (click)="addSetor()"><i class="glyphicon glyphicon-plus"></i>Adicionar</button>
                            <input type="text" name="table_search" class="form-control input-sm pull-right" style="width: 150px;" placeholder="Pesquisa Setor" [(ngModel)]="filtro" />
                            <div class="input-group-btn">
                                <button class="btn btn-sm btn-default"><i class="fa fa-search"></i></button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="box-body table-responsive no-padding">
                    <table class="table table-hover">
                        <tr>
                            <th>Código</th>
                            <th>Descrição</th>
                            <th>Ação</th>
                        </tr>
                        <tr *ngFor="let setor of obterSetores()">
                            <td></td>
                            <td></td>
                            <td>
                                <div class="buttons">
                                    <button class="btn btn-success btn-xs" (click)="editSetor(setor)">
                                                <span class="glyphicon glyphicon-edit" aria-hidden="true"></span>
                                                Editar
                                            </button>
                                    <button class="btn btn-danger btn-xs" (click)="delSetor(setor)">
                                                <span class="glyphicon glyphicon-trash" aria-hidden="true"></span>
                                                Exluir
                                            </button>
                                </div>
                            </td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <form name="form" (ngSubmit)="save()" #setor="ngForm">
                    <div class="box-header">
                        <div class="box-tools">
                            <div class="input-group">
                                <button type="submit" class="btn btn-sm btn-success" [disabled]="!setor.form.valid"><i name="save" id="save" class="glyphicon glyphicon-ok"></i>Salvar</button>
                                <button class="btn btn-sm btn-danger" (click)="cancel()"><i class="glyphicon glyphicon-remove"></i>Cancelar</button>
                            </div>
                        </div>
                    </div>
                    <div class="box box-primary">
                        <div class="box-header">
                            <h3 class="box-title">Informe os dados</h3>
                        </div>
                        <div class="form-group">
                            <input type="text" id="nameSetor" name="nameSetor" class="form-control" placeholder="Informe a descrição do setor" maxlength="100" [(ngModel)]="model.descricao" #nameSetor="ngModel" required/>
                            <span [hidden]="nameSetor.valid || nameSetor.pristine" class="alert alert-danger">descrição do setor</span>
                        </div>

                    </div>
                    <!-- /.box -->

                </form>
            </div>
        </div>
    </div>
</section>
<nav class="navbar navbar-default">
    <div class="container-fluid">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
            <a class="navbar-brand" href="#">Menu</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav">
                <li class="dropdown">
                    <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Cadastro <span class="caret"></span></a>
                    <ul class="dropdown-menu">
                        //Alterado href="#" para [TILink]
                        <li><a [routerLink]="['/app-setor']">Setor</a></li>
                        <li><a href="#">Pesquisa</a></li>
                    </ul>
                </li>
            </ul>
        </div>
        <!-- /.navbar-collapse -->
    </div>
    <!-- /.container-fluid -->
</nav>

//Incluí o router-outlet
<router-outlet></router-outlet>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <div class="box-header">
                    <div class="box-tools">
                        <div class="input-group">
                            <button class="btn btn-sm btn-primary" (click)="addProduto()"><i class="glyphicon glyphicon-plus"></i>Adicionar</button>
                            <input type="text" name="table_search" class="form-control input-sm pull-right" style="width: 150px;" placeholder="Pesquisa Produto" [(ngModel)]="filtro" />
                            <div class="input-group-btn">
                                <button class="btn btn-sm btn-default"><i class="fa fa-search"></i></button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="box-body table-responsive no-padding">
                    <table class="table table-hover">
                        <tr>
                            <th>Código</th>
                            <th>Descrição</th>
                            <th>Barra</th>
                            <th>Setor</th>
                            <th>Ação</th>
                        </tr>
                        <tr *ngFor="let produto of obterProdutos()">
                            <td></td>
                            <td></td>
                            <td></td>
                            <td></td>
                            <td>
                                <div class="buttons">
                                    <button class="btn btn-success btn-xs" (click)="editProduto(produto)">
                                                <span class="glyphicon glyphicon-edit" aria-hidden="true"></span>
                                                Editar
                                            </button>
                                    <button class="btn btn-danger btn-xs" (click)="delProduto(produto)">
                                                <span class="glyphicon glyphicon-trash" aria-hidden="true"></span>
                                                Exluir
                                            </button>
                                </div>
                            </td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="content">
    <div class="row">
        <div class="col-xs-12">
            <div class="box">
                <form (ngSubmit)="save()" #produtoForm="ngForm">
                    <div class="box-header">
                        <div class="box-tools">
                            <div class="input-group">
                                <button type="submit" class="btn btn-sm btn-success" [disabled]="!produtoForm.form.valid"><i name="save" id="save" class="glyphicon glyphicon-ok"></i>Salvar</button>
                                <button class="btn btn-sm btn-danger" (click)="cancel()"><i class="glyphicon glyphicon-remove"></i>Cancelar</button>
                            </div>
                        </div>
                    </div>
                    <div class="box box-primary">
                        <div class="box-header">
                            <h3 class="box-title">Informe os dados</h3>
                        </div>
                        <div class="form-group">
                            <input type="text" id="descricao" name="descricao" class="form-control" placeholder="Informe a descrição do produto" maxlength="100" [(ngModel)]="model.descricao" #descricao="ngModel" required/>
                            <div [hidden]="descricao.valid || descricao.pristine" class="alert alert-danger">Descrição de sua atividade</div>
                        </div>

                        <div class="form-group">
                            <input type="text" id="barra" name="barra" class="form-control" placeholder="Informe o código de barras" maxlength="14" [(ngModel)]="model.barra" #barra="ngModel" required/>
                            <div [hidden]="barra.valid || barra.pristine" class="alert alert-danger">Código de barras</div>
                        </div>

                        <div class="form-group">
                            <select class="form-control" id="setor" required [(ngModel)]="model.id_setor" name="setor" #setor="ngModel">
                                    <option *ngFor="let setor of setores" [value]="setor.id"></option>
                            </select>
                            <div [hidden]="setor.valid || setor.pristine" class="alert alert-danger">Setor</div>
                        </div>

                    </div>
                    <!-- /.box -->

                </form>
            </div>
        </div>
    </div>
</section>
<nav class="navbar navbar-default">
    <div class="container-fluid">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
            <a class="navbar-brand" href="#">Menu</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav">
                <li class="dropdown">
                    <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Cadastro <span class="caret"></span></a>
                    <ul class="dropdown-menu">
                        <li><a [routerLink]="['/app-setor']">Setor</a></li>
                        //Alterado href="#" para [TILink]
                        <li><a [routerLink]="['/app-produto']">artigos</a></li>
                        <li><a [routerLink]="['/app-produto']">Trabalhos</a></li>
                        <li><a [routerLink]="['/app-produto']">Projetos</a></li>


                    </ul>
                </li>
            </ul>
        </div>
        <!-- /.navbar-collapse -->
    </div>
    <!-- /.container-fluid -->
</nav>

<router-outlet></router-outlet>
<html ng-app="app">
<head>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.21/angular.min.js"></script>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.0rc1/angular-route.min.js"></script>
    <link href="~/Content/bootstrap.min.css" rel="stylesheet" />
    <script src="~/Scripts/jquery-2.1.1.min.js"></script>
    <script src="~/Scripts/bootstrap.js"></script>
    <script src="~/app/app.js"></script>
    <title>ExampleAngularJS</title>
    @RenderSection("JavascriptHeader", required: false)
</head>
<body>
    <div class="row">
        <div class="navbar navbar-default">
            <div class="navbar-header">
                <ul class="navbar navbar-nav">
                    <li>
                        <span class="navbar navbar-brand">Registration</span>
                    </li>
                </ul>
            </div>
            <div class="navbar-collapse colapse">
                <ul class="nav navbar-nav">
                    <li><a href="/Registration/Courses">Courses</a></li>
                    <li><a href="/Registration/Students">Students</a></li>
                </ul>
            </div>
        </div>
    </div>
    @RenderBody()
<html ng-app="myApp">
<head>
    <title>CRUD AngularJS</title>
    <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/angularjs/1.4.3/angular.min.js"></script>
</head>
<body ng-controller="MainCtrl">
    <form ng-submit="submit()">
        Nome<br>
            <input type="text" ng-model="nome"><br>
        Email<br>
            <input type="text" ng-model="email"><br>
        Senha<br>
            <input type="password" ng-model="senha"><br>
        <input type="submit" id="submit" value="Submit" />
    </form>
<html>
<head>
    <title>Angular2</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <meta http-equiv="x-ua-compatible" content="ie=edge">
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.min.css">
    <!--<link rel="stylesheet" href="../styles.css">-->
    <!-- Polyfill(s) for older browsers -->
    <script src="../node_modules/core-js/client/shim.min.js"></script>
    <script src="../node_modules/zone.js/dist/zone.js"></script>
    <script src="../node_modules/reflect-metadata/Reflect.js"></script>
    <script src="../node_modules/systemjs/dist/system.src.js"></script>
    <script src="../systemjs.config.js"></script>
    <script>
      System.import('app').catch(function(err){ console.error(err); });
    </script>
</head>
<body>
    <my-app>Carregando...</my-app>
    <div class="container">
   <div class="row">
      <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12 col-xl-12">
          <a href="#" class="btn btn-success">Novo</a>
          <table class="table table-striped table-hover">   
              <thead>
                  <tr>
                    <th>Nome</th>
                    <th>Email</th>
                    <th>Telefone</th>
                    <th>Deletar</th>
                  </tr>
              </thead>
              <tbody>  
                 <tr *ngFor = "let c of clientes">
             <td>{{c.nome}}</td>
             <td>{{c.email}}</td>
             <td>{{c.telefone}}</td>
                  <td><button class="btn btn-danger">Deletar</button></td>
                </tr>
              </tbody>
          </table>
      </div>
   </div>
</div>

<label for="example-input-1">Data</label>
					<input type="text" class="form-control date-mask" id="example-input-1" placeholder="Ex.: dd/mm/aaaa">
					<p class="help-block">Com a classe <code>.date-mask</code></p>
				</div>
				<div class="form-group col-lg-4">
					<label for="example-input-2">CPF</label>
					<input type="text" class="form-control cpf-mask" id="example-input-2" placeholder="Ex.: 000.000.000-00">
					<p class="help-block">Com a classe <code>.cpf-mask</code></p>
				</div>
				<div class="form-group col-lg-4">
					<label for="example-input-3">CEP</label>
					<input type="text" class="form-control cep-mask" id="example-input-3" placeholder="Ex.: 00000-000">
					<p class="help-block">Com a classe <code>.cep-mask</code></p>
				</div>
			</div>
			<div class="row">
				<div class="form-group col-lg-4">
					<label for="example-input-4">Horas</label>
					<input type="text" class="form-control time-mask" id="example-input-4" placeholder="Ex.: 00:00:00">
					<p class="help-block">Com a classe <code>.time-mask</code></p>
				</div>
				<div class="form-group col-lg-4">
					<label for="example-input-5">Data e hora</label>
					<input type="text" class="form-control date-time-mask" id="example-input-5" placeholder="Ex.: 00/00/0000 00:00:00">
					<p class="help-block">Com a classe <code>.date-time-mask</code></p>
				</div>
				<div class="form-group col-lg-4">
					<label for="example-input-6">Telefone</label>
					<input type="text" class="form-control phone-mask" id="example-input-6" placeholder="Ex.: 0000-0000">
					<p class="help-block">Com a classe <code>.phone-mask</code></p>
				</div>
			</div>
			<div class="row">
				<div class="form-group col-lg-4">
					<label for="example-input-7">Telefone com DDD</label>
					<input type="text" class="form-control phone-ddd-mask" id="example-input-7" placeholder="Ex.: (00) 0000-0000">
					<p class="help-block">Com a classe <code>.phone-ddd-mask</code></p>
				</div>
				<div class="form-group col-lg-4">
					<label for="example-input-8">Celulares de São Paulo</label>
					<input type="text" class="form-control cel-sp-mask" id="example-input-8" placeholder="Ex.: (00) 00000-0000">
					<p class="help-block">Com a classe <code>.cel-sp-mask</code></p>
				</div>
				<div class="form-group col-lg-4">
					<label for="example-input-9">Máscara Mista</label>
					<input type="text" class="form-control cep-mask" id="example-input-9" placeholder="Ex.: AAA 000-S0S">
					<p class="help-block">Com a classe <code>.mixed-mask</code></p>
				</div>
			</div>
		</fieldset>
	</form>
</div>
Apenas letras

<input type="text" required="required" name="text" pattern="[a-z\s]+$" />
Apenas números

<input type="text" required="required" name="numbers" pattern="[0-9]+$" />
Data

<input type="date" required="required" maxlength="10" name="date" pattern="[0-9]{2}\/[0-9]{2}\/[0-9]{4}$" min="2012-01-01" max="2014-02-18" />
Hora

<input type="time" required="required" maxlength="8" name="hour" pattern="[0-9]{2}:[0-9]{2} [0-9]{2}$" />
Campos genéricos de texto

<input type="text" required="required" name="name" />
Telefone

<input type="tel" required="required" maxlength="15" name="phone" pattern="\([0-9]{2}\) [0-9]{4,6}-[0-9]{3,4}$" />
Email

<input type="email" required="required" class="input-text" name="email" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,4}$" />
Moeda

<input type="tel" required="required" maxlength="15" name="valor" pattern="([0-9]{1,3}\.)?[0-9]{1,3},[0-9]{2}$" />
Utilizei o type=”tel”, pq em celulares renderiza melhor o teclado.

Input file

<input type="file" name="file" accept="image/*" required="required" />

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="description" content="Criptografia Moip">
    <meta name="author" content="Moip">
    <title>Validação de contas bancárias</title>

    <link href='//fonts.googleapis.com/css?family=Open+Sans:400,700' rel='stylesheet' type='text/css'>
    <link href="https://moip.com.br/docs/stylesheets/screen.css" rel="stylesheet" type="text/css" media="screen" />
    <link href="https://moip.com.br/docs/stylesheets/print.css" rel="stylesheet" type="text/css" media="print" />
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/css/bootstrap-theme.min.css">

    <script type="text/javascript" src="http://code.jquery.com/jquery-2.1.3.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/js/bootstrap.min.js"></script>

    <script type="text/javascript" src="build/bank-account-validator.min.js"></script>

  </head>

  <script type="text/javascript">

    $(document).ready(function() {
      $("#validate_bank_account").click(function() {
        Moip.BankAccount.validate({
          bankNumber         : $("#bank_number").val(),
          agencyNumber       : $("#agency_number").val(),
          agencyCheckNumber  : $("#agency_check_number").val(),
          accountNumber      : $("#account_number").val(),
          accountCheckNumber : $("#account_check_number").val(),
          valid: function() {
            $("#success_message").removeClass('hide').fadeIn('slow');
            $("#error_message").fadeOut();
          },
          invalid: function(data) {
            var errors = "Ocorreram os seguintes erros:<br/>";
            for(i in data.errors){
              errors += "- " + data.errors[i].description + "<br/>";
            }
            $("#error_message").removeClass('hide').fadeIn('slow');
            $("#error_message").html(errors);
            $("#success_message").fadeOut();
          }
        });
      });
    });
  </script>

  <body>

    <div class="row">
      <h2 class="form-signin-heading" align="center">Bank Account Validator</h2>
      <hr>

      <div class="col-md-4">&nbsp;</div>

      <div class="col-md-4">

        <div id="success_message" class="alert alert-success hide">Conta Bancária válida</div>
        <div id="error_message" class="alert alert-danger hide"></div>

        <form class="form-signin">

          <div class="row">
            <div class="col-md-12">

              <label>Banco</label>
              <select id="bank_number" class="form-control">
                <option value="">Selecione o banco</option>
                <optgroup label="Principais bancos">
                  <option value="001">BANCO DO BRASIL S.A.</option>
                  <option value="237">BANCO BRADESCO S.A.</option>
                  <option value="341">BANCO ITAÚ S.A.</option>
                  <option value="104">CAIXA ECONOMICA FEDERAL</option>
                  <option value="033">BANCO SANTANDER BANESPA S.A.</option>
                  <option value="399">HSBC BANK BRASIL S.A.</option>
                  <option value="745">BANCO CITIBANK S.A.</option>
                </optgroup>
              </select>
            </div>
          </div>

          <br/>

          <div class="row">
            <div class="col-md-5">
              <label>Agência</label>
              <input id="agency_number" placeholder="Exemplo: 0170" maxlength="5" type="text" class="form-control" />
            </div>
            <div class="col-md-4">
              <label>Dígito</label>
              <input id="agency_check_number" placeholder="Exemplo: 8" maxlength="2" type="text" class="form-control" />
            </div>
          </div>

          <br/>

          <div class="row">
            <div class="col-md-5">
              <label>Conta corrente</label>
              <input id="account_number" placeholder="Exemplo: 97845" maxlength="12" type="text" class="form-control" />
            </div>
            <div class="col-md-4">
              <label>Dígito</label>
              <input id="account_check_number" placeholder="Exemplo: 1" maxlength="2" type="text" class="form-control" />
            </div>
          </div>

          <br/>

          <input type="button" value="Validar conta bancária" id="validate_bank_account" class="btn btn-lg btn-primary btn-block"/>

        </form>

      </div>
    </div>
    <div class="col-md-4"></div>
    <footer class="footer">
      <div class="container">
        <div class="text-muted pull-right">Powered by <b><a href="http://www.moip.com.br">Moip</a></b></div>
      </div>
    </footer>
    <div class="col-md-4"></div>
  </body>
</html>
<form method="post" action="filtro.php">
   Filtrar por:
   <select name="opcao_filtro">
      <option value="idade">Idade</option>
      <option value="cidade">Cidade</option>
      <option value="formacao">Formação</option>
   </select>
   <input type="text" name="valor_filtro"/><br>
   <input type="submit" name="enviar"/>
</form>
<Classe Button = "btn btn- sucesso" ng clique com o botão = "edituser (" nova ")">
<Span class = "glyphicon glyphicon- usuário"> </ span> Criar Novo Usuário
</ Button>
<Hr>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Restaurante</title>
    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">

    <script>
        angular.module("appRestaurante",[]);

        angular.module("appRestaurante").controller("cozinhaCtrl",function($scope) {

        });

        angular.module("appRestaurante").controller("recepcaoCtrl",function($scope) {


            $scope.clientes = [{nome: "Jorge"},
                               {nome: "Mateus"}];
            //Main functions__________________________________________
            $scope.adicionarCliente = function(cliente) {
                $scope.clientes.push(cliente.nome);
                console.log("action",$scope.clientes);
//                delete $scope.$4;
            }
        });



            //Functions________________________________________________


    </script>
</head>
<body ng-app="appRestaurante">

<div class="jumbotron">
    <h1>Programação e Desenvolvimento</h1>
</div>

<div class="container">
    <h2>Matheus</h2>

    <table class="table"  ng-controller="recepcaoCtrl">
        <thead>
        <tr>
            <th>Nome</th>
        </tr>

        </thead>
        <tbody>
        <tr ng-repeat="cliente in clientes">
            <td>
                {{cliente.nome}}
            </td>

        </tr>
        </tbody>
    </table>

</div>


<div ng-include="'/home/pedro-ramalho/Documentos/AngularJS/RodrigoBranas/Meu/angularJS/html/tabelaServicos.html'"> </div>




<div class="container jumbotron">

    <h2>Adicionar</h2>

    <form ng-controller="cozinhaCtrl">
        <h3> TI</h3>
        <div class="form-group">
            <input class="form-control"  placeholder="Nome"  ng-model="nomeComida">
        </div>
        <button type="submit" class="btn btn-primary">Adicionar conteudos</button>
    </form>


    <form ng-controller="recepcaoCtrl">
        <h3>Analista de sistemas</h3>
        <div class="form-group">
            <input class="form-control"  placeholder="Nome" ng-model="cliente.nome">
        </div>
        <button type="submit" class="btn btn-primary" ng-click="adicionarCliente(cliente)">Adicionar</button>
        {{Matheus}}
    </form>




</div>



</body>
</html>

