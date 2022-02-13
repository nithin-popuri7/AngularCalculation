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
```
<body>
    <div class="container">
        <h1>Math Calculations</h1>
        <div class="subcontainer">
            
            <Rectangle-Area></Rectangle-Area>
        </div>
        <div class="subcontainer">
            <Cylinder-Area></Cylinder-Area>
        </div>
        <div class="footer">
            Developed by: Popuri Siva Naga Nithin
        </div>
    </div>
</body>
```
```
<div>
    <h2>Area of a Rectangle</h2>
    Length = <input  type="text" [(ngModel)]="length"> Meters<br>
    Breadth = <input [(ngModel)]="breadth"type ="text">Meters<br>
    <input type="button" (click)="onCalculate()" value="calculate"><br>
    Area=<input [value]="area" type="text" >Meter<sup>2</sup>
</div>
```
```
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'mathcalculations';
}
```
```import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'mathcalculations';
}
```
```import { Component } from "@angular/core";

@Component({
    selector:'Rectangle-Area',
    templateUrl:'./rectangle.component.html'

})
export class RectangleComponent{
    length:number
    breadth:number
    area:number
    constructor(){
        this.length = 0
        this.breadth = 0
        this.area = this.length*this.breadth;


    }
    onCalculate(){
        this.area = this.length*this.breadth;
    }
}
```
```
import { Component } from "@angular/core";
import { RadioControlValueAccessor } from "@angular/forms";

@Component({
    selector:'Cylinder-Area',
    templateUrl:'./cylinder.component.html'

})
export class CylinderComponent{
    radius:number
    height:number
    area:number
    
    constructor(){
        this.radius = 0
        this.height = 0
        this.area = 2*22/7*this.radius*(this.radius+this.height)

    }
    onCycCalculate(){
        this.area = this.area = 3.14*this.radius*this.radius*this.height
    }
}
```
```
.container{
    background-color: green;
    text-align: center;
    height: 720pxx;
}
.subcontainer{
    background-color: blue;
    width: 600px;
    height: 300px;
    text-align: center;
    margin-left: 400px;
    margin-bottom: 50px;
}
h1{
    text-decoration: underline;
}
```
```
import { NgModule } from '@angular/core';
import { FormsModule } from '@angular/forms';
import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component';
import { CylinderComponent } from './cylinder/cylinder.component';
import { RectangleComponent } from './rectangle/rectangle.component';

@NgModule({
  declarations: [
    AppComponent,
    RectangleComponent,
    CylinderComponent
  ],
  imports: [
    BrowserModule,
    FormsModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

## OUTPUT:
![githublogo](angu.jpeg)


## Result:
This is code is executed successfully to create a webpage to make mathematical calculations using angular.
