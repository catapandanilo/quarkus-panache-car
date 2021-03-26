# Tutorial: Quarkus - Simplificando o Hibernate utilizando Panache, criando uma aplicação simples utilizando Quarkus Java + REST + CDI + Panache

[Link do artigo](https://www.linkedin.com/pulse/tutorial-quarkus-simplificando-o-hibernate-panache-da-silva-melo/)

<!-- ABOUT THE PROJECT -->

## Sobre o Projeto

Tutorial: Quarkus - Simplificando o Hibernate utilizando Panache, criando uma aplicação simples utilizando Quarkus Java + REST + CDI + Panache

### Feito Com

Tecnologias utilizadas no projeto

- [JAVA](https://www.java.com/pt_BR/download/) - Java é uma linguagem de programação e plataforma computacional lançada pela primeira vez pela Sun Microsystems em 1995. Existem muitas aplicações e sites que não funcionarão, a menos que você tenha o Java instalado, e mais desses são criados todos os dias;
- [Quarkus](https://quarkus.io/) - A Red Hat lançou o Quarkus, um framework Java nativo do Kubernetes feito sob medida para o GraalVM e OpenJDK HotSpot. O Quarkus visa tornar o java uma plataforma líder em ambientes serverless e Kubernetes, oferecendo aos desenvolvedores um modelo unificado de programação reativa e imperativa;
- [Panache](https://quarkus.io/guides/hibernate-orm-panache) - Simplificando a camada de persistência de dados.

### Estrutura de Arquivos

A estrutura de arquivos está da seguinte maneira:

```bash
quarkus-panache-car
├── README.md
├── docs
│   └── postman
│       └── Quarkus-Panache-Car.postman_collection.json
├── pom.xml
├── quarkus-panache-car.iml
└── src
    ├── docs
    ├── main
    │   ├── docker
    │   │   ├── Dockerfile.jvm
    │   │   └── Dockerfile.native
    │   ├── java
    │   │   └── br
    │   │       └── com
    │   │           └── car
    │   │               ├── model
    │   │               │   └── Car.java
    │   │               ├── repository
    │   │               │   └── CarRepository.java
    │   │               └── resource
    │   │                   ├── CarResource.java
    │   │                   └── CarV2Resource.java
    │   └── resources
    │       ├── META-INF
    │       │   └── resources
    │       │       └── index.html
    │       ├── application.properties
    │       └── import.sql
    └── test
        └── java
            └── br
                └── com
                    └── car
                        └── resource
                            ├── CarResourceTest.java
                            └── NativeCarResourceIT.java

22 directories, 15 files

```

#### Executando a Instância do Postgresql no Docker 

Para iniciar o Postgresql, basta rodar o comando abaixo (O Docker precisa estar instalado): 

```sh
$ docker run --name postgres-car -e "POSTGRES_PASSWORD=postgres" -p 5433:5432 -v ~/developer/PostgreSQL:/var/lib/postgresql/data -d postgres
```

### Executando o projeto em Quarkus

Para executar um projeto em Quarkus, basta executar o comando: 
```sh
mvn compile quarkus:dev
```