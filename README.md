## 🌐 [English Version of README](README_EN.md)

# Java na Prática com AWS

Projeto desenvolvido durante o curso gratuito **Java na Prática com AWS**, ministrado por **Fernanda Kipper** e promovido pela Rocketseat. O sistema implementa um encurtador de URLs serverless utilizando **AWS Lambda** e **Amazon S3**, permitindo a criação de URLs curtas com prazo de validade configurável e suporte a redirecionamento.

## 🔨 Funcionalidades do Projeto

- **Criação de URLs curtas**: Recebe a URL original e o tempo de expiração, gera um código único e armazena os dados no Amazon S3.
- **Redirecionamento de URLs**: Valida se a URL está dentro do prazo de expiração e redireciona para a URL original ou retorna erro caso esteja expirada.
- **API Gateway**: Configuração de endpoints HTTP para concentrar as requisições.

### 📊 Exemplo Visual do Projeto

![Exemplo visual do sistema](https://metal-flea-041.notion.site/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F7e08ccba-1e15-4032-8025-5db6afff0a93%2Fb39e3ca4-fead-4100-a870-4fdd55322eec%2Fimage.drawio.png?table=block&id=11820141-41ff-80fe-971c-e69eccfdc5ec&spaceId=7e08ccba-1e15-4032-8025-5db6afff0a93&width=1420&userId=&cache=v2)

## ✔️ Técnicas e Tecnologias Utilizadas

- **Java**: Linguagem de programação utilizada no projeto.
- **AWS Lambda**: Funções serverless para criação e redirecionamento de URLs.
- **Amazon S3**: Armazenamento de metadados das URLs curtas.
- **API Gateway**: Configuração de endpoints HTTP.
- **Maven**: Gerenciador de dependências e build.
- **Lombok**: Redução de boilerplate no código Java.
- **Git/GitHub**: Controle de versão e colaboração.

## 📁 Estrutura do Projeto

- **CreateUrlLambda/**
  - `pom.xml`: Configuração do Maven.
  - `src/main/java/com/rocketboom/createUrlShortener/Main.java`: Implementação da criação de URLs curtas.
  - `src/main/java/com/rocketboom/createUrlShortener/UrlData.java`: Classe para armazenar dados de URLs.

- **HelloWorldJava/**
  - `pom.xml`: Configuração do Maven.
  - `src/main/java/example/Hello.java`: Função simples de exemplo "Hello World".
  - `src/main/java/org/example/Main.java`: Função principal do projeto.

- **RedirectUrlShortener/**
  - `pom.xml`: Configuração do Maven.
  - `src/main/java/com/rocketboom/redirectUrlShortener/Main.java`: Implementação do redirecionamento de URLs.
  - `src/main/java/com/rocketboom/redirectUrlShortener/UrlData.java`: Classe para armazenar dados de URLs.

- **README.md**
- **README_EN.md**

## 🛠️ Abrir e rodar o projeto

Para iniciar o projeto localmente, siga os passos abaixo:

1. Certifique-se de que o Java e o Maven estão instalados:
  - Verifique a versão do Java:  
    java -version
  - Verifique a versão do Maven:  
    mvn -version

   Caso não estejam instalados, acesse os sites oficiais do [Java](https://www.java.com/) e [Maven](https://maven.apache.org/) para download e instalação.

2. Clone o Repositório:  
   git clone <URL_DO_REPOSITORIO>

3. Navegue até o diretório e compile o projeto:  
   cd <PASTA_DO_PROJETO>  
   mvn clean install

4. Configure e implante as funções Lambda:  
   Use a [AWS CLI](https://aws.amazon.com/cli/) para configurar e implantar as funções `CreateShortUrlLambda` e `RedirectShortUrlLambda`.

## 🌐 Deploy

Para realizar o deploy do projeto:

1. Configuração inicial na AWS:  
   aws configure  
   Certifique-se de que você tem permissões para criar buckets S3 e funções Lambda.

2. Deploy das funções Lambda:  
   Configure e implante as funções `CreateShortUrlLambda` e `RedirectShortUrlLambda`.

3. Configuração do API Gateway:  
   Crie um API Gateway para gerenciar os endpoints:
- Endpoint para criação de URLs curtas.
- Endpoint para redirecionamento de URLs.

4. Teste o sistema:  
   Envie requisições HTTP para os endpoints gerados e verifique os logs no AWS CloudWatch.

## Notion

- [Guia do curso gratuito de Java](https://efficient-sloth-d85.notion.site/Guia-do-curso-gratuito-de-Java-d19bee9b1e3049038f6cf828334821a6)

- [Curso Java - AWS Lambda](https://efficient-sloth-d85.notion.site/Curso-Java-AWS-Lambda-725cedf305da44c69c847db4e3bad657)

- [Java na Prática by AWS](https://metal-flea-041.notion.site/Java-na-Pr-tica-by-AWS-1172014141ff8022a3e4ee81c99c2e57)
