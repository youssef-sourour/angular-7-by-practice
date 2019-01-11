# AppDemo

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.2.1.

## Objectifs
Create a component and understand its behavior.
## Steps
* Create the Navigation component class
   * src/app/navigation/navigation.component.ts
    ```
    import { Component } from '@angular/core';
    @Component({
        selector : 'app-nav',
        templateUrl : './navigation.component.html'
    })
    export class NavigationComponent {
        menu: string[] = ['Home', 'Blog', 'About', 'Contact'];
    }

    ```
   * src/app/navigation/navigation.component.html
    ```
    <nav>
        <ul>
            <li *ngFor="let element of menu">
                <a>{{element}}</a>
            </li>
        </ul>
    </nav>
    ```    
    * src/app/app.component.html
    ```
    <app-nav></app-nav>
    ```
    * src/app.module.ts
    ```
    import { NavigationComponent } from './navigation/navigation.component';
    ...
    @NgModule({
        declarations: [
            AppComponent,
            NavigationComponent
        ],
        ...
    ```

## Alternative way through ng cli 
* Create component using ng cli command line:
    ```
    ng generate component navigation --spec false --selector app-nav --module app 
    ```
* src/app/navigation/navigation.component.ts
    ```
    menu: string[] = ['Home', 'Blog', 'About', 'Contact'];
    ``` 
* src/app/navigation/navigation.component.html
    ```
    <nav>
        <ul>
            <li *ngFor="let element of menu">
                <a>{{element}}</a>
            </li>
        </ul>
    </nav>
    ```
* src/app/app.component.html
    ```
    <app-nav></app-nav>
    ```

### Angular CLI component manual
* ng g c help :
    ```
    ng generate component --help
    ```
## Launch app-demo

Run `ng serve --open` for a dev server. 

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.
https://github.com/angular/angular-cli/wiki
