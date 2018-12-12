Unit 2
==============================

This Unit assumes that during Unit 1 divs have been taught to the student. Topics covered in this unit are as follows: 
* Grouping objects in Divs

* Margin
* Padding
* View Width
* View Height



Lesson 1 - Manipulating Divs
------------------------------
1. Review Divs
2. Answer Questions
3. Introduce Padding and Margins
4. Give Assignment (recommendations given below)


_Hint: To make sure that they can easily see what is going on, it would be best to have a background color on the div._

### First Div - Padding

the first div example below is to introduce padding to the student.
```CSS
.first-div{
    background-color: gray;
    padding-top: 10px;
    padding-left: 10px;
    padding-bottom: 10px;
    padding-right: 10px;
}
```

```HTML
<div class="first-div">
    <h1>This is a header</h1>
    <p>We are learning about how to move objects around on the screen</p>
    <a href="#">Link to other stuff</a>
</div>
```

### Second Div - Margin


```CSS
.second-div{
    background-color: tan;
    margin-left: 100px;
    margin-top: 50px;
}
```

```Html
<div class="second-div">
    <h1>The second div</h1>
    <p>This second div is going to show off how to push objects from the right side of the screen</p>
</div>
```
Start off by showing them that they can push content from the left so everything is not left aligned.
Other things to teach:
* Why margin-top pushes content up
* combining all margin values into one
 * margin: (Top, Left, Bottom, Right) _Follows clock hands_
 * margin: ValueForAll _setting one value for all directions_


### Third Div - Combine the two with Border
```CSS
.third-div{
    background-color: aqua;
    padding: 5px;
    margin-top:50px;
    margin-left: 75px;
    border: 5px solid blue;
}
```

```Html
<div class="third-div">
    <h1>The Third Div</h1>
    <p>This third div combines all three concepts into one div: margin, padding, and border.</p>
</div>
```

#### Bonus Section
Introduce the concept of View Width (vw) and view height (vh)

explain that they are based off of percentage of space inside the browser window. can be used to set:
* Height (of a div or background picture)
* Width (of a div or background picture)
* Margin
* Padding

```CSS
.fourth-div{
    background-color: bisque;
    padding-left: 20vw;
    margin-left: 10vw;
    height: 20vw;
    width: 30vw;
}
```

```HTML
<div class="fourth-div">
    <h1>Another div to show off concepts</h1>
    <p>This last div will show using View Width and View Height instead of fixed pixels.</p>
</div>
```

Setting the width of a div can definitely be helpful in centering content on the page if the kids are bright about how they do it. For example:

have a Div that is 60% wide leaves 40% to divide between the two sides. therefore:
```CSS
.centered-div{
    margin-left: 20vw;
    width: 60vw;
    background-color:cadetblue;
}
```

```HTML
<div class="centered-div">
    <h1>We can center content on the screen!</h1>
    <p>this is done setting the width of a div and then taking half of the remainder as the margin-left</p>
</div>
```


Lesson 2 - Using Chrome Inspector and Advanced File Structure
----------------------------------------------

### Chrome Inspector
On Pc, right click and hit "inspect" (usually the last option of the menu). Alternatively, keyboard shortcuts are:
* Ctrl + Shift + i
* F12

Concepts to go over:
* Let them see the code for last week's website in the inspector
* Use the pointer to highlight an element and see the code
* Show off looking at the Styles that are applied to an element
* Show off the box model
 * Height and width of element (blue)
 * Padding around element (green)
 * Border on element (yellow)
 * margin on element (orange)
* Show them that you can change code temporarily either in the HTML or CSS
* Demonstrate that you can Change code on other websites temporarily!

![](newGoogle.png)

### Advanced File Structure
Up to this point, everything has been placed in the same folder.
Teach the following:
* Websites generally have index file in root directory (explain root)
 * Other pages in Html folder
 * Images in Images Folder
 * Styles in css folder
 * Scripts in Scripts folder
Thus far, if we have been linking to a file in the same directory, it has been an **absolute** reference

Relative file paths: use ../ to go back a directory or to another folder.

Go up a directory: ../
Go down a directory: /

Examples:
* ../index.html
 * used when you are linking from a page in the html folder to go back to the index.
* css/styles.css
 * used to go into the images folder or the 
 styles folder
 
 lessonTwo.html
 ```Html
<head>
    <link href="css/lessonTwo.css" rel=stylesheet type="text/css">
</head>
<body>
    <a href="html/about.html">About</a>
    <img src="../newGoogle.PNG">
</body>
```

html/about.html

This block of code includes in the header a complex going back to the previous folder and then into another folder in order to get to the styles
```HTML
<head>
    <link href="../css/lessonTwo.css" rel=stylesheet type="text/css">
</head>

<body>
    <a href="../lessonTwo.html">Home Page</a>
    <br>
    <p>this page just exists to show how to go back a directory to link to another page.</p>
</body>
```


