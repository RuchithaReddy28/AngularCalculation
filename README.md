# AngularCalculation

# Web Page for Mathematical Calculations using Angular

## AIM:
To design a dynamic website to perform mathematical calculations using Angular Framwork

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS in component.html file

### Step 3:

Write typescript to perform the calculations.

### Step 4:

Validate the layout in various browsers.

### Step 5:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
Cone:
cone.component.html:
```html
<style>
    h2{
background-color: rgb(224, 241, 241);
color: rgb(31, 29, 30);
}
.container {
  display: block;
  background-color: white;
  min-height: 200px;
  margin-top: 100px;
}
.al{
    text-align: center;
    font-size: 25px;
}

</style>
<div class="container">
    <div class="al">
    <h2>VOLUME OF CONE</h2>
    Radius=<input type="text"[(ngModel)]='radius'>Meters<br/>
    Height=<input type="text"[(ngModel)]='height'>Meters<br/>
    <input type="button" (click)="onCalculate()" value="CalculateArea"><br/>
    Volume=<input type="text" [value]="volume"> Meters<sup>3</sup><br/>
    V=πr2h/3
</div>
</div>

```
cone.component.ts:
```html

import { Component } from "@angular/core";

@Component({
    selector:'Cone-Vol',
    templateUrl:'./cone.component.html'
})
export class ConeComponent{
    radius:number;
    height:number;
    volume:number;
    constructor(){
        this.radius=0;
        this.height=0;
        this.volume=0;
    }
    onCalculate(){
        this.volume = 22/7*this.radius**2*this.height/3
    }
}
```
cylinder:
cylinder.component.html:
```html
<style>
    h2{
background-color: rgb(224, 241, 241);
color: rgb(31, 29, 30) ;
}
.container {
  display: block;
  background-color: white;
  min-height: 200px;
  margin-top: 100px;
}
.al{
    text-align: center;
    font-size: 25px;
}

</style>
<div class="container">
<div class="al">
    <h2>VOLUME OF CYLINDER</h2>
    Radius=<input type="text"[(ngModel)]='radius'>Meters<br/>
    Height=<input type="text"[(ngModel)]='height'>Meters<br/>
    <input tAype="button" (click)="onCalculate()" value="CalculateArea"><br/>
    Volume=<input type="text" [value]="volume"> Meters<sup>3</sup><br/>
    volume=π*r^2*h

</div>
</div>
```
cylinder.componet.ts:
```html
import { Component } from "@angular/core";

@Component({
    selector:'Cylinder-Vol',
    templateUrl:'./cylinder.component.html'
})
export class CylinderComponent{
    radius:number;
    height:number;
    volume:number;
    constructor(){
        this.radius=0;
        this.height=0;
        this.volume=0;
    }
    onCalculate(){
        this.volume = 22/7*this.radius**2*this.height
    }
}
```
app.component.css:
```html
h2{
    text-align: center;
    color: rgb(17, 14, 39);
    margin-top: 10px;


}
.container {
    width: 800px;
    margin-left: auto;
    margin-right: auto;
  }
  .backgd{
    background-color: lightblue ;
}
  .footer{
      text-align: center;
      font-size: 20px;
      color:black;
      background-color: lightblue;
      margin-top: 10px;
  }

```
app.component.html:
```html
<div class="backgd">
  <h2>MATH CALCULATION</h2>
  <div class="container">
      

<Cylinder-Vol>

</Cylinder-Vol>

<Cone-Vol>

</Cone-Vol>
<div class="footer">Developed By: Jegathish siva</div>

  </div>

</div>
```
app.module.ts:
```html
import { NgModule } from '@angular/core';
import { FormsModule } from '@angular/forms';
import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component';
import { ConeComponent } from './cone/cone.component';
import { CylinderComponent } from './cylinder/cylinder.component';

@NgModule({
  declarations: [
    AppComponent,CylinderComponent,ConeComponent
  ],
  imports: [
    BrowserModule,FormsModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }

```


## OUTPUT:
###WITHOUT OUTPUT:
![output](https://github.com/RuchithaReddy28/AngularCalculation/blob/main/N1.JPG?raw=true)
### WITH OUTPUT:
![output](https://github.com/RuchithaReddy28/AngularCalculation/blob/main/N2.JPG?raw=true)

## Result:
To design a dynamic website to perform mathematical calculations using Angular Framwork is successfully created.
