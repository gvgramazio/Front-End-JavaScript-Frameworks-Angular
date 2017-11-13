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

```JSON
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

### Getting Started with Angular

#### Objectives and Outcomes

In this first Angular exercise, you will first install *angular-cli*, the command line tool for scaffolding Angular applications. You will then use the tool to scaffold out a basic Angular application. We will thereafter develop this application into a full-fledged Angular application in the process of doing the exercises in this course. At the end of this exercise you will be able to:

- Install *angular-cli*
- Scaffold out a basic Angular application

#### Installing *Angular-CLI*

From the Angular-CLI documentation we learn that the Angular-CLI makes it easy to create an application that already works, right out of the box. It already follows the best practices suggested by the Angular community!

- To install *angular-cli* globally, type the following at the prompt:

```
npm install -g @angular/cli
```

**Note**:Use *sudo* on a Mac and Linux

- This will make the command line tool for creating Angular applications. To learn more about the various commands that this CLI provides, type at the prompt:

```
ng help
```

#### Generating and Serving an Angular Project using Angular-CLI

- At a convenient location on your computer, create a folder named *Angular* and move into that folder.
- Then type the following at the prompt to create a new Angular application named *conFusion*:

```
ng new conFusion -dir=<The path of your Angular folder>/conFusion --style=scss
```

- This should create a new folder named *conFusion* within your *Angular* folder and create the Angular application in that folder.
- Move to the conFusion folder and type the following at the prompt:

```
npm install
ng serve --open
```

- This will compile the project and then open a tab in your default browser at the address http://localhost:4200.
- You can initialize your project to be a Git repository by typing the following commands at the prompt:

```
git init
git add .
git commit -m "Initial Setup"
```

**Note**: Some of you may find that Angular CLI automatically does the first commit on your computer and initializes the Git repository. Please do a "git status" in the project folder just to check if an automatic commit has been done. This doesn't happen on my computer. Hence the above instructions.

- Thereafter you can set up an online Git repository and synchronize your project to the online repository. Make sure that the online Git repository is a private repository.

#### Conclusions

In this exercise you installed the Angular CLI tool and created a basic Angular project and served up the compiled project to your browser.

### Configuring your Angular Application

#### Objectives and Outcomes

In this exercise we will set up our project to use Angular Material and Angular Flex Layout. We will then introduce our first Angular Material component into our application. At the end of this exercise you will be able to:

- Configure your Angular project to use Angular Material and Flex Layout.
- Start using Material components in your application.

#### Configure your Angular Project to use Angular Material

**Note**: This course is designed with Angular Material Beta.3. Before you proceed forward, you may wish to read the detailed information posted in https://www.coursera.org/learn/angular/discussions/all/threads/4yxVk7DXEee0mQrUfDuicA where I have clearly explained about dealing with the newer Beta versions of Angular Material (up to Beta.12). I would strongly suggest that to proceed ahead with the course with minimal disruption, please install the Beta.8 version of Angular Material. With this installation, the course instructions will still work as given.

To configure your project to use Angular material, type the following at the prompt to install Angular Material, Angular Animations and HammerJS:

```
npm install @angular/material@2.0.0-beta.8 --save
npm install @angular/cdk@2.0.0-beta.8 --save
npm install --save @angular/animations 
npm install --save hammerjs 
```

#### Configure to use Material Design Icons

Next, include the following into the <head> of index.html to make use of Material Design icons:

```
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet"> 
```

#### Configure your Angular Project to use Flex Layout

Next, install Angular Flex Layout as follows:

```
npm install --save @angular/flex-layout@latest 
```

#### Updating AppModule

Then, you need to import the Angular Animations Module, Angular Material Module, Flex Layout Module and hammerjs into your root module (src/app/app.module.ts) as follows:

```
. . . 

import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
import { MaterialModule } from '@angular/material'; 
import { FlexLayoutModule } from '@angular/flex-layout';

. . . 

import 'hammerjs';

@NgModule({
  
  . . . 
  
  imports: [ 
    
    . . .,
    
    BrowserAnimationsModule,
    MaterialModule,
    FlexLayoutModule
    
  ], 
    
    . . . 
  
  
}) 

. . . 
```

#### Adding a Material Toolbar

Open app.component.html and replace its contents with the following code:

```
<md-toolbar color="primary"> <span>Ristorante Con Fusion</span> </md-toolbar>
```

#### Adding Styles

Add the following styles to styles.scss file:

```
@import '~@angular/material/prebuilt-themes/deeppurple-amber.css';

// some basic resets 

body { 
  padding: 0; 
  margin: 0; 
  font-family: Roboto, sans-serif; 
  
}
```

This will add a built-in Material theme to our application.
Do a Git commit with the message "Configuring Angular"

#### Conclusions

In this exercise we learnt to use Angular Material and Flex Layout NgModules in our Angular application.
