
<p align="center">
  <a href="https://cobi.bike"><img width="90px" height="90px" src="https://cdn.cobi.bike/devkit/resources/images/devkit-logo.svg">
  </a>

  <h3 align="center">COBI UI Components</h3>

  <p align="center">
    Sleek, intuitive, and scalable UI Components for faster and easier COBI webApp development.
    <br> <br>
    <a href="www.cobi.bike"><strong>Explore COBI DevKit website &raquo;</strong></a>
    <br>
    <br>
  </p>
</p>

<br>

## Description

These UI Components will let you to create Sleek, Intuitive and Scalable WebApp's. Build complex settings page, description view's for your WebApp's. Just grab one example and use it in your project! Read the instructions below how to start and create your own WebApp and run it on COBI!

## What's included


```
cobi-style/
├── css/
│   ├── cobi-style.css
│   └── adjust.css
├──  js/
│    ├── cobi-style.js
│    └──
├── sass/
│   └── cobi-style.scss
│
```

## Getting Started

#### General rules:
1. Make sure all your bars are the first things in your `<body>`.
2. Entire content of your page should be wraped with `.content` class.
3. Wrap elements with `.content-padded` class to give the content space around the screen.

All you have to do is just include `cobi-style.css` and `cobi-style.js` files to your project!

#### CSS:
``` html
<link href="https://cdn.cobi.bike/devkit/css/cobi-style.css" rel="stylesheet">
```
#### JS:
``` html
 <script src="https://cdn.cobi.bike/devkit/js/cobi-style.js"></script>
```


### Html basic template

Pls always use this basic template to create all of your views.
``` html
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <title>COBI template page</title>

  <!-- Sets initial viewport load and disables zooming  -->
  <meta name="viewport" content="initial-scale=1, maximum-scale=1">

  <!-- Makes your prototype chrome-less once bookmarked to your phone's home screen -->
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black">

  <!-- Include the compiled COBI CSS -->
  <link href="https://cdn.cobi.bike/devkit/css/cobi-style.css" rel="stylesheet">

  <!-- Include the your styles when you want to adjust styles to your needs -->
  <link href="css/adjust.css" rel="stylesheet">

  <!-- Include the compiled COBI JS -->
  <script src="https://cdn.cobi.bike/devkit/js/cobi-style.js"></script>

</head>

<body>

    <div class="content">
      <!-- content of your page go here -->
    </div>

</body>

</html>

```

## UI Components

Series of examples that tell you how you can use COBI UI Components:


### Typography

Use headings and paragraphs to title and describe sections of your app.
``` html
<h1>COBI Style framework!</h1>
<h2>COBI Style framework!</h2>
<h3>COBI Style framework!</h3>
<h4>COBI Style framework!</h4>
<h5>COBI Style framework!</h5>
<h6>COBI Style framework!</h6>
```

Wrap elements with .content-padded class to give the content space around the screen.

``` html
<div class="content-padded">
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.</p>
</div>
```

When you want to center headline or paragraphs in your view just add `class="text-center"`


### Buttons

Buttons come in many flavors

Regular button style
``` html
<button class="btn">Button text</button>
```
Disabled state
``` html
<button class="btn disabled">Button text</button>
```
Button with icon. You can find full list of icons <a>here</a>
``` html
<button class="btn">Button text<span class="icon icon-right-nav"></span></button>
```
Button with COBI surf blue color
``` html
<button class="btn blue">Button text</button>
```
Button with COBI tarmac color
``` html
<button class="btn tarmac">Button text</button>
```

### Bars

Title bars are full width and docked to the top of the viewport. Make sure all your bars are the first things in your `<body>`


``` html
<header class="bar bar-nav">
  <a class="icon icon-left-nav pull-left"></a>
  <a class="icon icon-compose pull-right"></a>
  <h1 class="title">Title</h1>
</header>
```

### Forms

Form with input group and labels. Use it to build your settings page.

``` html
<form class="input-group">
  <div class="input-row">
    <label>Full name</label>
       <input type="date" placeholder="21.02.2017">
  </div>
  <div class="input-row">
    <label>Example</label>
    <input type="email" placeholder="cobistyle@gmail.com">
  </div>
  <div class="input-row">
    <label>Username</label>
    <input type="text" placeholder="cobistyle">
  </div>
</form>
```
Centered input with transparent background color.
``` html
<div class="input-transparent">
  <input type="url" placeholder="http://example.com">
</div>
```

### Table-views

Table views can be used for build settings page.

``` html
<ul class="table-view">
  <li class="table-view-cell">
    <a class="navigate-right" href="settings.html" data-transition="slide-in">Load new page with push</a>
  </li>
  <li class="table-view-cell table-view-cell">
    <a class="navigate-right">Item 2</a>
  </li>
  <li class="table-view-cell">COBI toggle<label class="toggle"><input type="checkbox"><div class="slider round"></div></label></li>
  <li class="table-view-cell">
    <a>Item 1</a>
  </li>
  <li class="table-view-cell table-view-cell">
    <a>Item 2</a>
  </li>
  <li class="table-view-cell">COBI toggle
    <label class="toggle">
    <input type="checkbox" checked>
      <div class="slider round"></div>
    </label>
  </li>
  <li class="table-view-divider">Divider</li>
  <li class="table-view-cell">
    <a class="navigate-right">Item 1</a>
  </li>
  <li class="table-view-divider">Divider</li>
</ul>
```
### Modals

Modals are designed to be fire only from links, use `<a href="#myModalexample" class="btn blue">Open modal</a>` to fire modal div with `id="myModalexample"`

``` html
<!-- Content of your page -->
<div class="content-padded">
  <a href="#myModalexample" class="btn blue">Open modal</a>
</div>

<!-- Modal Content -->
<div id="myModalexample" class="modal">
  <header class="bar bar-nav">
    <a class="icon icon-close pull-right" href="#myModalexample"></a>
    <h1 class="title">Modal</h1>
  </header>

  <div class="content">
    <p class="content-padded">The contents of my modal go here. Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut.</p>
  </div>
</div>
```

### Toggle

Toggles can be used by tapping the control.

``` html
<label class="toggle"><input type="checkbox"><div class="slider round"></div></label>
```

### Icons

When you want to use icon just grab one from here:

``` html
<div class="content-padded">
  <span class="icon icon-back"></span>
  <span class="icon icon-bars"></span>
  <span class="icon icon-caret"></span>
  <span class="icon icon-check"></span>
  <span class="icon icon-close"></span>
  <span class="icon icon-code"></span>
  <span class="icon icon-compose"></span>
  <span class="icon icon-download"></span>
  <span class="icon icon-edit"></span>
  <span class="icon icon-forward"></span>
  <span class="icon icon-gear"></span>
  <span class="icon icon-home"></span>
  <span class="icon icon-info"></span>
  <span class="icon icon-list"></span>
  <span class="icon icon-more-vertical"></span>
  <span class="icon icon-more"></span>
  <span class="icon icon-pages"></span>
  <span class="icon icon-pause"></span>
  <span class="icon icon-person"></span>
  <span class="icon icon-play"></span>
  <span class="icon icon-plus"></span>
  <span class="icon icon-refresh"></span>
  <span class="icon icon-search"></span>
  <span class="icon icon-share"></span>
  <span class="icon icon-sound"></span>
  <span class="icon icon-sound2"></span>
  <span class="icon icon-sound3"></span>
  <span class="icon icon-sound4"></span>
  <span class="icon icon-star-filled"></span>
  <span class="icon icon-star"></span>
  <span class="icon icon-stop"></span>
  <span class="icon icon-trash"></span>
  <span class="icon icon-up-nav"></span>
  <span class="icon icon-up"></span>
  <span class="icon icon-right-nav"></span>
  <span class="icon icon-right"></span>
  <span class="icon icon-down-nav"></span>
  <span class="icon icon-down"></span>
  <span class="icon icon-left-nav"></span>
  <span class="icon icon-left"></span>
</div>
```
