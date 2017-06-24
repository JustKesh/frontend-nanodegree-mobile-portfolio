# How to run the application
* Click the following [link] () to run the application.
* Or open the index.html in any browser of your preference

## Optimizations in Index.html 
* Added "media=print" to the css print stylesheet
* Added async attribute to the google analytics script
* Added ( media="none" onload="if(media!='all')media='all'") to the font to keep it from loading until the page finished loading
* Inline style.css
* Minified perfmatters.js
* Compressed img/profilepic.jpg
* Optimized pizzeria.jpg image

PageSpeed for Mobile: 95
PageSpeed for Desktop: 96

## Optmzations in views/js/main.js for pizza.html
* In function changePizzaSizes(size), 
** moved the document selector outside of the for loop, 
** removed the determineDX function and 
** added switch(size) to  set the different sizes of pizzas to their width percentages instead of pixel conversion
* In updatePositions(), 
** moved repetitive code outside of the for loop to handle scrollTop/1250, 
** declared the variable 'position' to handle the sin calculation,
** Used getElementsByClassName for faster DOM access
** reversed the loop to optimize performance and only calculate the object length once
** changed style.left to style.transform
* In document.addEventListener('DOMContentLoaded', function()
** Since we are using transform in updatePositions() instead of basicLeft, a custom property, means basicLeft has to change to style.left with px
** Used getElementById for faster DOM access

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>