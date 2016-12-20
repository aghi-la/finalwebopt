## Website Performance Optimization portfolio project


####Part 1: Optimize PageSpeed Insights score for index.html.

The PageSpeed Insights score is made to 90 above in both Mobile and Desktop by minifying CSS and adding async to JS.The script is brought down to bottom part of body in index.html.The minified CSS is included in the index.html inside style format.Also all the images are compressed.

####Part 2: Optimize Frames per Second in pizza.html

The views/pizza.html is optimized to obtain a frames per second rate of 60 fps or higher by modifying views/js/main.js and views/pizza.html.

The main changes made in main.js are :

1. 'determineDx' function is removed and made important changes to 'changePizzaSizes(size)' function.
2. 'document.querySelectorAll' is replaced with 'document.getElementByClassName('randomPizzaContainer')'.
3. var pizzasDiv = document.getElementById("randomPizzas"); is moved out of 'for' loop to improve the performance.
4. Important changes made to 'updatePosition' function.
  document.querySelectorAll('.mover') is replaced with document.getElementsByClassName('mover') to improve efficiency.
  document.body.scrollTop is assigned to a new variable 'top' [since,performing a.b.c is more expensive than a.b which is more expensive than simply doing a].
  Changes done on Iteration loops.
  instead of left, used transform which only triggers compositing.(CSS hardware acceleration)
5. requestAnimationFrameToScroll() function is included
  A new 'scrolling' variable is used to ensure requestAnimationFrame only runs when scroll event is fired
6. document.getElementById("movingPizzas1") is used instead of document.querySelector("#movingPizzas1")
7. 'translateZ(0)' , 'translate3d(0,0,0)'' are included to reduce the paint.

The main changes made in pizza.html are :

1. Minified CSS and included in style of pizza.html.
2. will-change : transform property is added to mover class.
3. Images are compressed.


