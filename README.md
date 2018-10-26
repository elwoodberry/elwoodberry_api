# ElwoodBerry API   
API driven portfolio, blog and ecommerce customer facing portal.  
[ElwoodBerry.com](http://elwoodberry.com)  

## Summary  
Drive the spa from a WP API.

## Development Stack  
1. Apache/Linux  
1. Wordpress (admin panel)    
1. Wordpress REST API  
1. Angular   
1. Ionic  
1. Materialize or Google Material  



## Wordpress   
### Plugins   
1. [JSON Basic Authentication](https://github.com/WP-API/Basic-Auth)   
## Angular   

**Create Project**  
```javascript     
$ ng new PROJECTNAME      
```   
**Serve Project**  
```javascript   
---   
$ ng serve -o   
---  
```   
**Build Project**  
```javascript   
---   
$ ng build --prod   
---  
```  

## Materialize   
You can download the materlize library [here](https://materializecss.com/).    
After ucompresseing the download, move the folder's CSS files and JS files to their respective locations inside the assets folder.   
```json      
{
	"e2e": {},
	"node_modules": {},
	"src": {
		"assets": {
			"css": {
				"f1": "materialize.css",
				"f2": "materialize.min.css"
			},
			"js": {
				"f1": "materialize.js",
				"f2": "materialize.min.js"
			}
		}
	}
}   
```    
**Import CSS** in app root style.css (or style.scss).      
```javascript  
@import "./assets/css/materialize.min.css";    
``` 
**Update** app.component.ts          
```javascript   
import { Component } from '@angular/core';
import * as M from '../assets/js/materialize.min.js'; // Import Materialize JS library.  

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})

export class AppComponent {
  title = 'Tour of Heroes';
}
```

## References    
### Wordpress  
1. [REST API Handbook](https://developer.wordpress.org/rest-api/)   

### Angular    
1. [ng build](https://github.com/angular/angular-cli/wiki/build)
1. [Running an angular 2 application..](https://stackoverflow.com/questions/39771458/running-an-angular-2-application-built-locally-on-chrome-using-angular-cli-witho)   
1. [Creating a web app in 5 minutes with Angular 5 and Materialize CSS](https://fullstackengine.net/create-wedding-page-angular-materialize/)     
1. [Materialize Carousel Mobile with Angular 6](https://youtu.be/AT5L3K-TGps)

### Ionic   
1. [PWA Basics](https://ionicframework.com/pwa)
1. [How to make PWAs with Ionic](https://blog.ionicframework.com/how-to-make-pwas-with-ionic/)


## Log    
* October 12th, 2018  
   - Drafting the outline of the project.  
* October 24th, 2018  
   - Create [ElwoodBerry API](http://elwoodberry.com/api/)  
   - Configured access to [http://elwoodberry.com/api/wp-json/wp/v2/](http://elwoodberry.com/api/wp-json/wp/v2/)  
   - Used the "Tour Of Heroes" Angular demo as the SPA placeholder uploaded to the root directory.
   
* October 25th, 2018   
   - **ERROR** Couldn't find Materialize object on window. It is created by the materialize-css library. Please import materialize-css before importing angular2-materialize.
