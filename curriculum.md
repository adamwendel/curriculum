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

### Possible Projects
1) Compare and contrast two different things like a venn diagram (e.g. iPhone vs. Android)
   * Leftmost Div is for thing 1 (iPhone)
   * Center Div is for what is common between thing 1 and thing 2
   * Right Div is for thing 2 (Android)
   
*Challenge can be done by having them use view width to give each div exactly 1/3 of the screen. Example file for both can be found in lessonOne > projectOne.html*


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

Lesson 3
-------------------------------
### Objectives
 1) introduce the idea of a front-end web framework
 
 2) explain the pros / cons of using a framework
 
 3) Use Skill Struck Website as an example
 
 3) Add link to bootstrap CSS and introduce container
 
### Introduce Front-End Framework
Websites have matured to the point where a consistent look and feel is necessary and becomes part of the websites' brand image

Bootstrap was created by software developers at twitter to help them create that consistent look and feel across the website with easy to remember css classes

Frameworks have a bunch of pre-created CSS classes that can be used by pointing to the CSS file and referencing the class names in the html file

Great Documentation exists so that it can be better understood how to use the classes

### Pros / Cons of using a framework
Pros:
 * Pre-created classes that quickly add a bunch of styling to a website
 * Ground work has been created to do some of the basic styling
 * Created to be "responsive", meaning that websites can more easily be created to respond to different screen sizes (phone vs tablet vs computer)
 * You don't have to understand exactly how everything is coded to be able to use the features

Cons:
 * Coded by someone else, so what may be intuitive to them may not be intuitive to you
 * If something breaks or doesn't work the way you want it to, it can take lots of trial and error to see what in their code breaks everything
 * Can be a "shortcut" in learning, as what is happening "under the hood" may not be understood, creating a great deal of frustration in troubleshooting
 
### Demonstrate with Skill Struck Website how frameworks help
 * Show that there are different "rows" of content
 * Show the different "columns" of content
 * Navbar at the top and the fixed nature
 
 *Note: The SkillStruck website does use a couple of different frameworks to create the exact look and feel, but the concepts are the same of columns, rows, easily creatable navs and footers, etc*
 
### Link to boostrap

```Html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css" integrity="sha384-GJzZqFGwb1QTTN6wy59ffF1BuGJpLSa9DkKMp0DgiMDm4iYMj70gZWKYbI706tWS" crossorigin="anonymous">

```
Explain that this link works just like linking to a local css file or like linking to an image from the internet. Downloading and adding the file locally will be shown later.

Create a container
```Html
<div class="container">
    <p>stuff goes here</p>
</div>
```
Demonstrate a before/after with the container and what happens by adding that one line of code (the content is centered, no matter the window size)

Everything that should go in the main body area should go into a container. Most of the time a Nav Bar is not included inside the container but stretches the width of the window


### Projects ----- TO BE ADDED AT A LATER DATE


Lesson Four
--------------------

