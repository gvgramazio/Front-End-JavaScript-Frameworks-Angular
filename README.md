# Front-End JavaScript Frameworks: Angular

About this course: This course concentrates mainly on Javascript based front-end frameworks, and in particular the Angular framework (Currently Ver. 4.x). This course will use Typescript for developing Angular application. Typescript features will be introduced in the context of Angular as part of the exercises. You will also get an introduction to the use of Angular Material and Angular Flex-Layout for responsive UI design. You will be introduced to various aspects of Angular including components, directives and services. You will learn about data binding, Angular router and its use for developing single-page applications. You will also learn about designing both template-driven forms and reactive forms. A quick introduction to Observables, reactive programming and RxJS in the context of Angular is included. You will then learn about Angular support for client-server communication and the use of REST API on the server side. You will use Restangular for communicating with a server supporting the REST API. A quick tour through Angular animation support and Angular testing rounds off the course. You must have either completed the previous course in the specialization on Bootstrap 4, or have a working knowledge of front end web-UI frameworks to be able to navigate this course. Also a good working knowledge of JavaScript, especially ES 5 is strongly recommended.

At the end of this course you will:

- Be familiar with client-side Javascript frameworks and the Angular framework
- Be able to implement single page applications in Angular
- Be able to use various Angular features including directives, components and services
- Be able to implement a functional front-end web application using Angular
- Be able to use Angular Material and Angular Flex-Layout for designing responsive Angular applications
- Be able to use Observables and RxJS in the context of Angular applications

Who is this class for: This course is aimed at students with sufficient knowledge of Web technologies like HTML, CSS and JavaScript. A good working knowledge of JavaScript, especially ES 5 is strongly recommended.

---

https://www.coursera.org/learn/angular

## Week 1

### Basics of Node.js and NPM

#### Objectives and Outcomes

In this exercise you will learn the basics of Node and NPM. At the end of this exercise, you will be able to:

- Set up package.json file in the project folder for configuring your Node and NPM for this project
- Install a NPM module and make use of it within your project

#### Initializing package.json

#### At the command prompt in your **git-test** folder, type

```
npm init
```

- Follow along the prompts and answer the questions as follows: accept the default values for most of the entries, except set the entry point to index.html
- This should create a *package.json* file in your **git-test** folder.

#### Installing an NPM Module

- Install an NPM module, lite-server, that allows you to run a Node.js based development web server and serve up your project files. To do this, type the following at the prompt:

```
npm install lite-server --save-dev
```

- You can check out more documentation on lite-server [here](https://github.com/johnpapa/lite-server).
- Next, open package.json in your editor and modify it as shown below. Note the addition of two lines, line 7 and line 9.

```
{
  "name": "git-test",
  "version": "1.0.0",
  "description": "This is the Git and Node basic learning project",
  "main": "index.html",
  "scripts": {
    "start": "npm run lite",
    "test": "echo \"Error: no test specified\" && exit 1",
    "lite": "lite-server"
  },
  "repository": {
    "type": "git",
    "url": "git+https://jogesh_k_muppala@bitbucket.org/jogesh_k_muppala/git-test.git"
  },
  "author": "",
  "license": "ISC",
  "homepage": "https://bitbucket.org/jogesh_k_muppala/git-test#readme",
  "devDependencies": {
    "lite-server": "^2.2.2"
  }
}

```

- Next, start the development server by typing the following at the prompt:

```
npm start
```

- This should open your *index.html* page in your default browser.
- If you now open the *index.html* page in an editor and make changes and save, the browser should immediately refresh to reflect the changes.

#### Setting up .gitignore

- Next, create a file in your project directory named *.gitignore* (**Note**: the name starts with a period)Then, add the following to the .gitignore file

```
node_modules
```

- The do a git commit and push the changes to the online repository. You will note that the node_modules folder will not be added to the commit, and will not be uploaded to the repository.

#### Conclusions

In this exercise you learnt to set up package.json, install a npm package and start a development server.
