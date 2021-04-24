# MyCrudApp

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.2.10.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

# Angular-CRUD-Operation

Step 1: Create New App

    ng new my-crud-app --routing
   
Step 2: Install Bootstrap

    npm install bootstrap --save
    
Now, let's import css file as like bellow:

    src/styles.css

/* You can add global styles to this file, and also import other style files */

    @import "~bootstrap/dist/css/bootstrap.css";

Step 3: Create Post Module

    ng generate module post --routing
    
run successfully command, it will create files as like bellow path:

    src/app/post/post.module.ts
    src/app/post/post-routing.module.ts

Step 4: Create Component For Module

    ng generate component post/index
    ng generate component post/view
    ng generate component post/create
    ng generate component post/edit
    
run successfully command, it will create folder with files as like bellow path:

    src/app/post/index/*
    src/app/post/view/*
    src/app/post/create/*
    src/app/post/edit/*

Step 5: Create Route

In this step, we will simply create route for index, create, edit and view using generated new component. so we have to update our post-routing module file.

    src/app/post/post-routing.module.ts

Step 6: Create Interface

in this step, we will create interface using angular command for post module. we will use post interface with Observable.

    ng generate interface post/post

    src/app/post/post.ts
    
Step 7: Create Services

Here, we will create post service file and we will write and call all web services. we will create getAll(), create(), find(), update() and delete().
    
    ng generate service post/post
Update below file 
       
       src/app/post/post.service.ts
  
Step 8: Update Component Logic and Template

Now in this step, we will work on our created component for crud application. we create four component for our crud application. now we will go one by one for creating list page, create page, edit page and view page.  

1) List Page Template and Component

now, here we will work on post index component. we will call post service and display it with create, edit, delete and view button. so let's update it.

    src/app/post/index/index.component.ts
    src/app/post/index/index.component.html

2) Create Page Template and Component

now here, we will use reactive form store data into server using web services. so let's update it.

    src/app/post/create/create.component.ts
    src/app/post/create/create.component.html
    
3) Edit Page Template and Component

now here, we will use reactive form store data into server using web services for update post information. so let's update it.

    src/app/post/edit/edit.component.ts
    src/app/post/edit/edit.component.html
    
4) Detail Page Template and Component

now here, we will display data into server using web services for update post information. so let's update it.

    src/app/post/view/view.component.ts
    src/app/post/view/view.component.html

Now let's update app html view:

    src/app/app.component.html

Step 9: Import to Module File

Now in last step, we will import our post module and HttpClientModule to main file and also other to post module.

    src/app/app.module.ts
    src/app/post/post.module.ts
    
Now we are ready to run our example, you can run by following command:

    ng serve
    localhost:4200/post
