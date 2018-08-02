Hands-On Full-Stack Web Development with Angular 6 and Laravel 5 (ISBN 139781788833912)
---

**What You Will Learn**

* Explore the core features of Angular 6 to create sophisticated user interfaces
* Use Laravel 5 to its full extent to create a versatile backend layer based on RESTful APIs.
* Configure a web application in order to accept user-defined data and persist it into the database using server-side APIs.
* Build an off-line-first application using service-worker and manifest file.
* Deal with token based authentication on single page application (SPA).
* Deploy using Docker images.


**Table of Contents** (ISBN 139781788833912)

- [Chapter 1, *Understanding the core concepts of Laravel 5*](#chapter-1-understanding-the-core-concepts-of-laravel-5)
- [Chapter 2, *The Benifits of TypeScript*](#chapter-2-the-benifits-of-typescript)
- [Chapter 3, *Understanding the core concepts of Angular 6*](#chapter-3-understanding-the-core-concepts-of-angular-6)
- [Chapter 4, *Building the baseline backend application*](#chapter-4-building-the-baseline-backend-application)
- [Chapter 5, *Creating a Restful API using Laravel Framework (Part I)*](#chapter-5-creating-a-restful-api-using-laravel-framework-part-i)
- [Chapter 6, *Creating a Restful API using Laravel Framework (Part II)*](#chapter-6-creating-a-restful-api-using-laravel-framework-part-ii)
- [Chapter 7, *Progressive web application with Angular-cli*](#chapter-7-progressive-web-application-with-angular-cli)
- [Chapter 8, *Dealing with Angular Router and Components*](#chapter-8-dealing-with-angular-router-and-components)
- [Chapter 9, *Creating Services and User authentication*](#chapter-9-creating-services-and-user-authentication)
- [Chapter 10, *Building the front-end views with NgBootstrap*](#chapter-10-building-the-front-end-views-with-ngbootstrap)
- [Chapter 11, *Angular tests, build and Deploy*](#chapter-11-angular-tests-build-and-deploy)

## Development environment
**All chapters and examples are based on Docker and Docker-compose**.

- Docker:
  * Go to https://docs.docker.com/install/.
  * Choose your platform and follow the installation steps.
  * Start Docker.
- VS Code:
  * Go to the https://code.visualstudio.com/Download
  * Choose your platform and follow the installation steps.
  * Follow the installation steps for your platform.
- MySQL Workbench:
  * Go to https://dev.mysql.com/downloads/workbench/
  * Choose your platform and follow the installation steps.
- Node.js:
  * Go to https://nodejs.org/en/
  * Choose your platform and follow the installation steps.

## Using the sample code

After download the individual chapters from repository, we need to take a few steps before running our application.

Here is the steps (Remember you must have all the softwares installed on your machine mentioned on Software list).

Installation process for chapters: 01, 04, 05, 06, 10, 11.

1. Edit `.env.example` to: `.env` if you can't see the `.env`.
**Important Note: on some operating systems `.dot` files are hidden by default**,
so you need a code editor to see and edit this kind of file, we strong recommend the use of VS.code. Open your terminal inside the chapter folder and type the following command on your Terminal: `cp .env.example .env`.
2. Change the `.env` database configuration using the `docker-compose.yml` MySql configuration as follow:
    ```
      DB_CONNECTION=mysql
      DB_HOST=mysql
      DB_PORT=3306
      DB_DATABASE=chapter-04 # Note here you need to use the right chapter number
      DB_USERNAME=chapter-04
      DB_PASSWORD=123456
      ```
3. Open your Terminal window inside the project folder and type the following command: `docker-compose up -d` to start all **Docker containers**, this should take some minutes do download and build the images.
4. Type the following command: `docker-compose exec php-fpm bash` to access container **bash**.
5. Inside the container bash, type the following command: `composer install`, this command may take a few minutes to download all the project dependencies, depending on your internet connection.
6. Run `php artisan key:generate`
7. Run `php artisan migrate`
8. Run `php artisan db:seed`

**Congratulations** now we have everything we need to see the application running.

Open your default browser and go to http://localhost:8081. and we can see the Laravel welcome screen.

---
**Important note: On some chapters the url must be different. We advise you to use the individual instructions in each chapter to have access to the correct urls.**
**if you are on windows, use the IP address generated by Docker-tools-cmd**

---

### Special instructions for some chapters

**chapter 02**:
Open your terminal inside the chapter folder and type the folloing command: `npm install`.

**chapter 03**:
1. Open your terminal inside the chapter folder and type the folloing command: `npm install`.
2. Type on your terminal: `npm start`.
3. Go to http://localhost:4200/

**chapter 07**:

In this chapter you must conbine instruction for back-end chapters (01, 04, 05, 06, 10, 11) with front-end chapters (01, 03). So here is the step by step;

1. Edit `.env.example` to: `.env` if you can't see the `.env`.
**Important Note: on some operating systems `.dot` files are hidden by default**,
so you need a code editor to see and edit this kind of file, we strong recommend the use of VS.code. Open your terminal inside the chapter folder and type the following command on your Terminal: `cp .env.example .env`.
2. Change the `.env` database configuration using the `docker-compose.yml` MySql configuration as follow:
    ```
      DB_CONNECTION=mysql
      DB_HOST=mysql
      DB_PORT=3306
      DB_DATABASE=chapter-04 # Note here you need to use the right chapter number
      DB_USERNAME=chapter-04
      DB_PASSWORD=123456
      ```
3. Open your Terminal window inside the project folder and type the following command: `docker-compose up -d` to start all **Docker containers**, this should take some minutes do download and build the images.
4. Type the following command: `docker-compose exec php-fpm bash` to access container **bash**.
5. Inside the container bash, type the following command: `composer install`, this command may take a few minutes to download all the project dependencies, depending on your internet connection.
6. Run `php artisan key:generate`
7. Run `php artisan migrate`
8. Run `php artisan db:seed`

Open your terminal inside `chapter/Client` folder and type the following commands:

9. Open your terminal inside the chapter folder and type the folloing command: `npm install`.
10. Type on your terminal: `npm start`.

---

# Chapter 1, *Understanding the core concepts of Laravel 5*

The Laravel framework is a powerful tool for the development of web applications, using the paradigm *convention over configuration*. Out of the box, Laravel has all of the features that we need to build modern web applications, token based authentication, routes, resources and many more. Also, the Laravel framework is one of the most popular PHP frameworks for developing web applications today. In this chapter we will learn how to setup the environment, Laravel application Lifecycle and how to use the Artisan Cli.

# Chapter 2, *The Benifits of TypeScript*

TypeScript enables you to write consistent JavaScript code. It includes static typing and other features that are very common in object-oriented languages also we can use the new features of the latest version of ECMAScript. Not only that, but TypeScript helps us to write clean and well-organized code. In this chapter we will see the benefits of TypeScript over traditional JavaScript, how to use static typing and understand how to use Interfaces, Classes, Generics, Import and Export classes.

# Chapter 3, *Understanding the core concepts of Angular 6*

Angular is one of the most popular and is used framework around the world for the development of front-end web applications. In addition to being very versatile and complete, also include the Angular/Cli tool to generate modules, components, services and many more utilities. In this chapter we will learn how to use the new version of Angular/Cli, the core concepts of Angular and understand component life cycle.

# Chapter 4, *Building the baseline backend application*

At this moment we will start building the sample application. In this chapter we are going to create a Laravel application using the Restful architecture, we will take a closer look at some points that we mentioned briefly in Chapter 1, such as using Docker containers to configure our environment and also how to keep our database always populated even using the MySQL Docker container, how to use Migrations and database seed and also how to create a consistent documentation with Swagger UI.

# Chapter 5, *Creating a Restful API using Laravel Framework (Part I)*

In this chapter we will make a brief introduction about RESTful and API's.
You will learn how to build a RESTful API using the core elements of Laravel framework as: controllers, routes, and Eloquent Object Relational Mapping (ORM).
In this chapter we show some basic wireframes about an application we are building.
In addition we will look more closely at some relationships like: One-to-one, One-to-many, Many-to-many and others.

# Chapter 6, *Creating a Restful API using Laravel Framework (Part II)*

In this chapter we will continue to build our example API, we still have a long way to go in Laravel.
We will learn how to use some features very common in every web application, such as token based authentication how to dealing with request validation, custom error message and how to use Laravel Resources. Also we will see how to use the Swagger documentation to test our API.

# Chapter 7, *Progressive web application with Angular-cli*

In this chapter we will see some changes that occurred in the angular-cli.json file from previous Angular version (before version 6), which now provides an improved support for multiple applications.
We will see how to use *ng add* command to create a PWA (Progressive web application) and how we can organize our project structure to leave a single basis for a scalable project. Also we will see how use the Angular/Cli to create service-work and manifest files.

# Chapter 8, *Dealing with Angular Router and Components*

At this point we come to one of the most important parts for single page application (SPA) which is the use of routes and the Angular framework provides a powerful tool for dealing with application routing is the *@angular/router* dependency. In this chapter we will learn how to use some of these features like router-outlet, child-views and how to create master detail pages. Also we will start to create the front-end views.

# Chapter 9, *Creating Services and User authentication*

In this chapter we have a lot of work ahead and we will create many new things and make some refactoring to memorize import details. This is a great way to learn new things in a regular and progressive way. Also we will go deeply into the operation and use of the *HTTP module* of the Angular framework, now known as *httpClient*.
In addition we will see how to use Interceptors, handling errors, use Authorization Headers and how to protect application routes using *Route Guards*.

# Chapter 10, *Building the front-end views with NgBootstrap*

At this moment we will see how to include Bootstrap CSS framework and NgBootstrap components inside a running Angular application using the new *ng add* command from Angular/Cli.
Also we will see how to connect our Angular services with components and how to using the backend API to put all together.
We will learn how to configure CORS on our backend API and how to use it with our Angular Client side application. Also we will see how to dealing with Angular Pipe, Template-driven Forms, Model-driven Forms and form validations.

# Chapter 11, *Angular tests, build and Deploy*

In this chapter we learned how to install, customize and extend Bootstrap CSS framework, how to use NgBootstrap components and how to connect Angular services with components and UI interfaces. Also we will learn how to write Angular unit tests, how to configure application linters (For SCSS and Tslint) to keep code consistency, how to create NPM scripts and also how to create a Docker image and deploy the application.