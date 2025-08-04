Subject:

jQuery: most popular JavaScript tool of all time

jQuery is a fast, lightweight JavaScript library that simplifies DOM manipulation, 
event handling, animations, and AJAX requests


inside the script tag add
Example Code:
```
    <script>
  $(document).ready(function() {

  });
</script>
```
if its before your html code

the code you put inside this function will run as soon as your browser has loaded your page.

This is important because without your document ready function, your code may run before your HTML is rendered, which would cause bugs.


All jQuery functions start with a $


jQuery often selects an HTML element with a selector, then does something to that element.


make all of your button elements bounce. Just add this code inside your document ready function:
Example Code:
```
  $("button").addClass("animated bounce");
```
you are using jQuery to apply the Animate.css bounce class to your button elements.


jQuery's **.addClass()** function, allows you to add classes to elements.


make all the elements with the class text-primary shake by adding the following to your document ready function:
Example Code:
```
  $(".text-primary").addClass("animated shake");
```


make the button element with the id target6 fade out:
Example Code:
```
  $("#target6").addClass("animated fadeOut");
```


They are three ways of targeting elements: 
by type: $("button"), by class: $(".btn"), and by id $("#target1").


you can remove a class with jQuery's **removeClass()** function.
Example Code:
```
  $("#target2").removeClass("btn-default");
```


jQuery has a function called **.css()** that allows you to change the CSS of an element.
Here's how we would change its color to blue:
Example Code:
```
  $("#target1").css("color", "blue");
```
This is slightly different from a normal CSS declaration, because the CSS property and its value are in quotes, and separated with a comma instead of a colon.


You can also change the non-CSS properties of HTML elements with jQuery. 
For example, you can disable buttons.

jQuery has a function called **.prop()** that allows you to adjust the properties of elements.

Here's how you would disable all buttons:
Example Code:
```
  $("button").prop("disabled", true);
```


you can change the text between the start and end tags of an element. 
You can even change HTML markup.

jQuery has a function called **.html()** that lets you add HTML tags and text within an element. 
Any content previously within the element will be completely replaced with the content you provide using this function.
Example Code:
```
  $("h3").html("<em>jQuery Playground</em>");
```


also has a similar function called **.text()** that only alters text without adding tags. 
In other words, this function will not evaluate any HTML tags passed to it, but will instead treat it as the text you want to replace the existing content with.


jQuery has a function called **.remove()** that will remove an HTML element entirely.
Example Code:
```
  $("#target4").remove();
```


jQuery has a function called **appendTo()** that allows you to select HTML elements and append them to another element.

For example, if we wanted to move target4 from our right well to our left well, we would use:
Example Code:
```
  $("#target4").appendTo("#left-well");
```


jQuery has a function called **clone()** that makes a copy of an element.

For example, if we wanted to copy target2 from our left-well to our right-well, we would use:
Example Code:
```
$("#target2").clone().appendTo("#right-well");
```
Did you notice this involves sticking two jQuery functions together? 
This is called **function chaining** and it's a convenient way to get things done with jQuery.


Every HTML element has a parent element from which it inherits properties.

jQuery has a function called **parent()** that allows you to access the parent of whichever element you've selected.

an examplel, if you want to give the parent element of the left-well element a background color of blue:
Example Code:
```
  $("#left-well").parent().css("background-color", "blue")
```


jQuery has a function called **children()** that allows you to access the children of whichever element you've selected.

an example to give the children of your left-well element the color blue:
Example Code:
```
$("#left-well").children().css("color", "blue")
```


jQuery uses CSS Selectors to target elements. 
The **target:nth-child(n)** CSS selector allows you to select all the nth elements with the target class or element type.

Here's how you would give the third element in each well the bounce class:
Example Code:
```
  $(".target:nth-child(3)").addClass("animated bounce");
```


You can also target elements based on their positions using **:odd** or **:even** selectors.

Note that jQuery is zero-indexed which means the first element in a selection has a position of 0. 
This can be a little confusing as, counter-intuitively, :odd selects the second element (position 1), fourth element (position 3), and so on.

Here's how you would target all the odd elements with class target and give them classes:
Example Code:
```
  $(".target:odd").addClass("animated shake");
```



Example Code:
```
  $("body").addClass("animated hinge");
```


