
<p align="center">
  <a href="https://cobi.bike"><img width="90px" height="90px" src="https://cdn.cobi.bike/devkit/v1.0.0/resources/images/devkit-logo.svg">
  </a>

  <h3 align="center">COBI.Bike DevKit UI Components</h3>

  <p align="center">
    Sleek & intuitive UI components for faster and easier development of COBI.Bike modules :rocket:
    <br>
    <a href="https://github.com/cobi-bike/devkit"><strong>This project is part of the COBI.Bike DevKit</strong></a>
    <br>
    <br>
  </p>
</p>

<br>

# Table of contents

- [Quick start](#quick-start)
- [General rules](#general-rules)
- [Html basic template](#html-basic-template)
- [Demo examples](#demo-examples)
- [UI Components](#ui-components)
  - [Content](#content)
  - [Typography](#typography)
  - [Buttons](#buttons)
  - [Title Bars](#title-bars)
  - [Forms](#forms)
  - [Table Views](#table-views)
  - [Modals](#modals)
  - [Toggle](#toggle)
  - [Icons](#icons)
- [Credits](#credits)


# Quick start
The COBI.Bike DevKit-UI library is a collection of the most common web [UI components](#ui-components), mainly supposed to be used for building [DevKit settings and manual pages](https://github.com/cobi-bike/DevKit#-settings-for-your-module). All elements are touch enabled, animated and responsive to provide a nice native (mobile) experience. The lib also comes with a shared CSS style according to the COBI.Bike CI, so it blends perfectly in with the native COBI.Bike app when used for your own [DevKit](https://github.com/cobi-bike/DevKit) module. In addition more complex components are provided to build for module settings or manual page. See [Demo examples](#demo-examples).

It's dead simple to integrate into your project. All you have to do is just include `cobi-style.css` and `cobi-style.js` files to your project!

### CSS:
``` html
<link href="https://cdn.cobi.bike/devkit/v1.0.0/css/cobi-style.css" rel="stylesheet">
```
### JS:
``` html
<script src="https://cdn.cobi.bike/devkit/v1.0.0/js/cobi-style.min.js"></script>
```

# General rules
Please follow these few rules for a proper and easy integration:

1. Make sure to put a title bar always as  the first element in your `<body>`.
2. The entire content of your page should be wraped with `.content` class.
3. Wrap elements with `.content-padded` class to give the content space around the screen.


# HTML basic template

Always use this basic template to create all of your views.
``` html
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <title>COBI.Bike template page</title>

  <!-- Sets initial viewport load and disables zooming  -->
  <meta name="viewport" content="initial-scale=1, maximum-scale=1">

  <!-- Makes your prototype chrome-less once bookmarked to your phone's home screen -->
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black">

  <!-- Include the compiled COBI.Bike CSS -->
  <link href="https://cdn.cobi.bike/devkit/v1.0.0/css/cobi-style.css" rel="stylesheet">

  <!-- Include the compiled COBI.Bike JS -->
  <script src="https://cdn.cobi.bike/devkit/v1.0.0/js/cobi-style.min.js"></script>

</head>

<body>

    <div class="content">
      <!-- content of your page go here -->
    </div>

</body>

</html>
```
# Demo examples

## 1. App settings/description template

Use this template to describe your app and build your settings page.

<h6>(Remember to always test your project in <a href="https://developers.google.com/web/tools/chrome-devtools/device-mode/">Chrome Mobile Devices Simulator</a>)</h6>

[See demo](https://cdn.cobi.bike/devkit/v1.0.0/examples/app-music.html)

``` html
<!-- Settings view header -->
  <header class="bar gray">
    <a class="icon icon-info pull-right" href="#appDescription" data-transition="slide-out"></a>


    <!-- Info view start -->
    <div id="appDescription" class="modal">

      <header class="bar light">
        <a class="icon icon-close pull-right" href="#appDescription" data-transition="slide-out"></a>
      </header>

      <div class="content">
        <img class="content-bg" src="https://cdn.cobi.bike/devkit/v1.0.0/resources/images/hex-shape-bg.svg" alt="">

        <div class="app-info-header">
          <!--  Your App icon shuld be square with size 230px x 230px -->
          <img class="app-icon" src="https://cdn.cobi.bike/devkit/v1.0.0/resources/images/app_icon.jpg">
        </div>

        <div class="content-padded">
          <h3 class="text-center">Spotify app</h3>
          <p class="text-center">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</p>
        </div>
        <div class="img-slider" id="mySlider">
          <div class="slide-group">
            <div class="slide">
              <img src="https://cdn.cobi.bike/devkit/v1.0.0/resources/images/slide1.jpg">
            </div>
            <div class="slide">
              <img src="https://cdn.cobi.bike/devkit/v1.0.0/resources/images/slide2.jpg">
            </div>
            <div class="slide">
              <img src="https://cdn.cobi.bike/devkit/v1.0.0/resources/images/slide3.jpg">
            </div>
          </div>

          <div class="indicators-group">
            <ul class="indicators">
              <li class="dot-style active"></li>
              <li class="dot-style"></li>
              <li class="dot-style"></li>
            </ul>
          </div>

        </div>
      </div>
    </div>
    <!-- Info view end -->
  </header>

  <!-- Settings view content -->
  <div class="content gray">
    <div class="content-padded">
      <p class="content-padded text-center">If you want to use Spotify app, you have log in first, then you will have acces to Spotify app and other stuff.</p>
    </div>

    <form class="input-group">
      <form class="input-group">
        <div id="input" class="input-icon">
          <span class="icon icon-person"></span>
          <input class="login-icon" type="text" placeholder="Your login">
        </div>
        <div class="input-icon">
          <span class="icon icon-more"></span>
          <input type="password" placeholder="Password">
        </div>
      </form>
      <button class="btn btn-block blue">Log In</button>
  </div>

```


## 2. Modal template

Use this template to describe your app and build your settings page.

<h6>(Remember to always test your project in <a href="https://developers.google.com/web/tools/chrome-devtools/device-mode/">Chrome Mobile Devices Simulator</a>)</h6>

[See demo](https://cdn.cobi.bike/devkit/v1.0.0/examples/modal.html)

``` html
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

## 3. Settings template with nested view

Use this template to build content of your settings page.

<h6>(Remember to always test your project in <a href="https://developers.google.com/web/tools/chrome-devtools/device-mode/">Chrome Mobile Devices Simulator</a>)</h6>

[See demo](https://cdn.cobi.bike/devkit/v1.0.0/examples/settings-view.html)

``` html
<div class="content gray">
  <!-- content of your page go here -->
    <p class="content-padded text-center">This is the example page with settings view. Feel free to use it in your project.</p>
    <ul class="table-view">
      <li class="table-view-cell"><a class="navigate-right" href="push.html" data-transition="slide-in">Load new page with push</a></li>
      <li class="table-view-cell">COBI.Bike toggle
        <label class="toggle">
          <input type="checkbox">
          <div class="slider-circle round"></div>
        </label>
      </li>
      <li class="table-view-cell">COBI.Bike toggle active
        <label class="toggle">
          <input type="checkbox" checked>
          <div class="slider-circle round"></div>s
        </label>
      </li>
      <li class="table-view-divider">Profile</li>
    </ul>
    <form class="input-group">
      <div class="input-row">
        <label>Birth date</label>
        <input type="date" placeholder="21.02.2017">
      </div>
      <div class="input-row">
        <label>Email</label>
        <input type="email" placeholder="email@cobi.bike">
      </div>
      <div class="input-row">
        <label>Username</label>
        <input type="text" placeholder="user">
      </div>
    </form>
</div>
```

# UI Components

Here's a series of examples/templates to show how to use COBI.Bike UI Components.

## Content

Three styles of content are available:

White:
``` html
<div class="content">
  <!-- content of your page go here -->
</div>
```

Gray:
``` html
<div class="content gray">
  <!-- content of your page go here -->
</div>
```

COBI.Bike Surf Blue:
``` html
<div class="content blue">
  <!-- content of your page go here -->
</div>
```


## Typography

Use headings and paragraphs to title and describe sections of your app.

 ``` html
<h1>COBI.Bike Style framework!</h1>
<h2>COBI.Bike Style framework!</h2>
<h3>COBI.Bike Style framework!</h3>
<h4>COBI.Bike Style framework!</h4>
<h5>COBI.Bike Style framework!</h5>
<h6>COBI.Bike Style framework!</h6>
 ```

Wrap elements with `.content-padded` class to give the content space around the screen.

``` html
<div class="content-padded">
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.</p>
</div>
```

To center a headline or paragraphs in your view just add `class="text-center"`


## Buttons

Buttons come in many flavors and support all kind of states:

Regular button style
``` html
<button class="btn">Button text</button>
```
Disabled state
``` html
<button class="btn disabled">Button text</button>
```
Button with icon. You can find the full list of icons [here](#icons).

``` html
<button class="btn">Button text<span class="icon icon-right-nav"></span></button>
```
Button with COBI.Bike surf blue color
``` html
<button class="btn blue">Button text</button>
```
Button with COBI.Bike tarmac color
``` html
<button class="btn tarmac">Button text</button>
```

## Title Bars

Title bars are full width and docked to the top of the viewport. Make sure your title bar is the first element in your `<body>`.

Title bar with blue background (default)
``` html
<header class="bar bar-nav">
  <a class="icon icon-left-nav pull-left"></a>
  <a class="icon icon-compose pull-right"></a>
  <h1 class="title">Title</h1>
</header>
```

Title bar with white background
``` html
<header class="bar light">
</header>
```

Title bar with gray background
``` html
<header class="bar gray">
</header>
```

## Forms

Form with input group and labels. Useful to build your module's [settings page](https://github.com/cobi-bike/DevKit#-settings-for-your-module).

``` html
<form class="input-group">
  <div class="input-row">
    <label>Date</label>
       <input type="date" placeholder="21.02.2017">
  </div>
  <div class="input-row">
    <label>Example</label>
    <input type="email" placeholder="mail@cobi.bike">
  </div>
  <div class="input-row">
    <label>Example</label>
    <input type="text" placeholder="">
  </div>
</form>
```
Centered input with transparent background color.
``` html
<div class="input-transparent">
  <input type="url" placeholder="http://example.com">
</div>
```

Centered input with transparent background color and icon on left side.
``` html
<form class="input-group">
  <div id="input" class="input-icon">
    <span class="icon icon-person"></span>
    <input class="login-icon" type="text" placeholder="Your login">
  </div>
  <div class="input-icon">
    <span class="icon icon-more"></span>
    <input type="password" placeholder="Password">
  </div>
</form>
```

## Table-views

Table views are perfect to build a list of settings with a set of toggle buttons or input fields.

``` html
<ul class="table-view">
  <li class="table-view-cell">
    <a class="navigate-right" href="source.html" data-transition="slide-in">Load new page with push</a>
  </li>
  <li class="table-view-cell table-view-cell">
    <a class="navigate-right">Item 2</a>
  </li>
  <li class="table-view-cell">COBI.Bike toggle<label class="toggle"><input type="checkbox"><div class="slider-circle round"></div></label></li>
  <li class="table-view-cell">
    <a>Item 1</a>
  </li>
  <li class="table-view-cell table-view-cell">
    <a>Item 2</a>
  </li>
  <li class="table-view-cell">COBI.Bike toggle
    <label class="toggle">
    <input type="checkbox" checked>
      <div class="slider-circle round"></div>
    </label>
  </li>
  <li class="table-view-divider">Divider</li>
  <li class="table-view-cell">
    <a class="navigate-right">Item 1</a>
  </li>
</ul>
```

To open a sub view related to a settings entry just use this and as `href` value. You the can use a separate html for your sub view. Do not forget to include `cobi-style.min.js` file to your project.
``` html
<ul class="table-view">
  <li class="table-view-cell">
    <a class="navigate-right" href="source.html" data-transition="slide-in">Load new page with push</a>
  </li>
</ul>
```

## Modals

Modals are designed to be triggered only by links, use `<a href="#myModalexample" class="btn blue">Open modal</a>` to trigger and open a modal div with `id="myModalexample"`. Do not forget to include `cobi-style.min.js` file to your project.

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

## Toggle

Toggles are swiched by tapping the control.

``` html
<label class="toggle"><input type="checkbox"><div class="slider-circle round"></div></label>
```

## Icons

Here's a list of useful icons to be used in your project if needed:

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

# Credits

This application uses Open Source components. You can find the source code of their open source projects along with license information below. We acknowledge and are grateful to these developers for their contributions to open source.

Project: Ratchet https://github.com/twbs/ratchet

Copyright connors and other contributors. All right reserved.

License (MIT) https://github.com/twbs/ratchet/blob/master/LICENSE
