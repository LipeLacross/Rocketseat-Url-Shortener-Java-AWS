## 🌐 [Versão em Português do README](README.md)

# Java in Practice with AWS

This project was developed during the free course **Java in Practice with AWS**, taught by **Fernanda Kipper** and promoted by Rocketseat. The system implements a serverless URL shortener using **AWS Lambda** and **Amazon S3**, allowing the creation of short URLs with configurable expiration times and support for redirection.

## 🔨 Project Features

- **Short URL Creation**: Receives the original URL and expiration time, generates a unique code, and stores the data in Amazon S3.
- **URL Redirection**: Validates whether the URL is within the expiration time and redirects to the original URL or returns an error if expired.
- **API Gateway**: HTTP endpoint configuration to manage requests.

### 📊 Visual Example of the Project

![System visual example](https://metal-flea-041.notion.site/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F7e08ccba-1e15-4032-8025-5db6afff0a93%2Fb39e3ca4-fead-4100-a870-4fdd55322eec%2Fimage.drawio.png?table=block&id=11820141-41ff-80fe-971c-e69eccfdc5ec&spaceId=7e08ccba-1e15-4032-8025-5db6afff0a93&width=1420&userId=&cache=v2)

## ✔️ Tools and Technologies Used

- **Java**: Programming language used in the project.
- **AWS Lambda**: Serverless functions for URL creation and redirection.
- **Amazon S3**: Storage of short URL metadata.
- **API Gateway**: HTTP endpoint configuration.
- **Maven**: Dependency and build manager.
- **Lombok**: Reduces boilerplate code in Java.

## 📁 Project Structure

- **CreateUrlLambda/**
    - `pom.xml`: Maven configuration.
    - `src/main/java/com/rocketboom/createUrlShortener/Main.java`: Implementation of short URL creation.
    - `src/main/java/com/rocketboom/createUrlShortener/UrlData.java`: Class to store URL data.

- **HelloWorldJava/**
    - `pom.xml`: Maven configuration.
    - `src/main/java/example/Hello.java`: Simple "Hello World" example function.
    - `src/main/java/org/example/Main.java`: Main function of the project.

- **RedirectUrlShortener/**
    - `pom.xml`: Maven configuration.
    - `src/main/java/com/rocketboom/redirectUrlShortener/Main.java`: Implementation of URL redirection.
    - `src/main/java/com/rocketboom/redirectUrlShortener/UrlData.java`: Class to store URL data.

- **README.md**
- **README_PT.md**

## 🛠️ How to Open and Run the Project

To run the project locally, follow these steps:

1. Ensure that Java and Maven are installed:
    - Check the Java version:
      java -version
    - Check the Maven version:
      mvn -version

   If not installed, visit the official sites for [Java](https://www.java.com/) and [Maven](https://maven.apache.org/) to download and install.

2. Clone the Repository:  
   git clone <REPOSITORY_URL>

3. Navigate to the directory and compile the project:  
   cd <PROJECT_FOLDER>  
   mvn clean install

4. Configure and deploy the Lambda functions:  
   Use the [AWS CLI](https://aws.amazon.com/cli/) to configure and deploy the `CreateShortUrlLambda` and `RedirectShortUrlLambda` functions.

## 🌐 Deployment

To deploy the project:

1. Initial AWS setup:  
   aws configure  
   Ensure you have permissions to create S3 buckets and Lambda functions.

2. Deploy the Lambda functions:  
   Configure and deploy the `CreateShortUrlLambda` and `RedirectShortUrlLambda` functions.

3. Configure the API Gateway:  
   Create an API Gateway to manage the endpoints:
    - Endpoint for short URL creation.
    - Endpoint for URL redirection.

4. Test the system:  
   Send HTTP requests to the generated endpoints and check the logs in AWS CloudWatch.

## Notion

- [Free Java Course Guide](https://efficient-sloth-d85.notion.site/Guia-do-curso-gratuito-de-Java-d19bee9b1e3049038f6cf828334821a6)

- [Java - AWS Lambda Course](https://efficient-sloth-d85.notion.site/Curso-Java-AWS-Lambda-725cedf305da44c69c847db4e3bad657)

- [Java in Practice by AWS](https://metal-flea-041.notion.site/Java-na-Pr-tica-by-AWS-1172014141ff8022a3e4ee81c99c2e57)
