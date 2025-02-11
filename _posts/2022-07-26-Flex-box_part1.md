---
layout: post
title: FLex Box part 1
subtitle: FLex Box
categories: CSS
tags: [FLex-Box CSS]
---


## Introduction to Flex box Part1


You know everything necessary to begin using it in your own projects.

* display: flex changes an element to a block-level container with flex items inside of it.
* display: inline-flex allows multiple flex containers to appear inline with each other.
* justify-content is used to space items along the main axis.
* align-items is used to space items along the cross axis.
* flex-grow is used to specify how much space (and in what proportions) flex items absorb along the main axis.
* flex-shrink is used to specify how much flex items shrink and in what proportions along the main axis.
* flex-basis is used to specify the initial size of an element styled with flex-grow and/or flex-shrink.
* flex is used to specify flex-grow, flex-shrink, and flex-basis in one declaration.
* flex-wrap specifies that elements should shift along the cross axis if the flex container is not large enough.
* align-content is used to space rows along the cross axis.
* flex-direction is used to specify the main and cross axes.
* flex-flow is used to specify flex-wrap and flex-direction in one declaration.
* Flex containers can be nested inside of each other by declaring display: flex or display: inline-flex for children of flex containers.


## Example:

important code:
```
.cards {
  background-color: #ffc200;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.col {
  display: inline-flex;
  flex-direction: column;
  justify-content: space-between;
}
```

The whole code:


HTML:
```
<!doctype html>
<html>
<head>
  <link href='https://fonts.googleapis.com/css?family=Libre+Baskerville:400,700,400italic' rel='stylesheet' type='text/css'>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="header">
    <div class="container">
      <h1>Headlines.</h1>
      <ul>
        <li><a href="3">About</a></li>
        <li><a href="#expertise">Our Services</a></li>
        <li><a href="3">Our Team</a></li>
        <li><a href="#footer">Contact Us</a></li>
      </ul>
    </div>
  </div>
  <div class="jumbotron">
    <div class="container">
      <h2>We <span>collect and curate</span>
articles, opinions, and images
from around the world.</h2>
    </div>
  </div>
  <div class="banner">
    <div class="container">
      <h2>The Bottom Line.</h2>
      <p>We deliver the news that is relevant to you.</p>
    </div>
  </div>
  <div class="container">
    <h2 id="expertise">Our Expertise.</h2>
    <div class="main">
      <div class="spacer">
        <div class="cards">
          <div class="col">
            <img src="https://content.codecademy.com/projects/headlines/p1.jpg">
            <img src="https://content.codecademy.com/projects/headlines/p6.jpg">
            <img src="https://content.codecademy.com/projects/headlines/p8.jpg">
          </div>
          <div class="col">
            <img src="https://content.codecademy.com/projects/headlines/p2.jpg">
            <img src="https://content.codecademy.com/projects/headlines/p5.jpg">
            <img src="https://content.codecademy.com/projects/headlines/p7.jpg">
          </div>
          <div class="col">
            <img src="https://content.codecademy.com/projects/headlines/p3.jpg">
            <img src="https://content.codecademy.com/projects/headlines/p4.jpg">
            <img src="https://content.codecademy.com/projects/headlines/p9.jpg">
            <img src="https://content.codecademy.com/projects/headlines/p10.jpg">
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="footer">
    <h3>Headlines.</h3>
    <p>1000 7th Avenue</p>
    <p>New York, NY</p>
    <p>(484) 192 - 8372</p>
  </div>
</body>
</html>

```

CSS:


```
html, body {
  margin: 0;
  padding: 0;
  font-family: 'Libre Baskerville', sans-serif;
}

img {
  margin: 10px auto;
  height: auto;
  width: auto;
}

ul {
  text-align: right;
}

h1 {
  font-size: 20px;
}

/*Sizing*/

.container {
  margin: 0 auto;
}

.spacer {
  max-width: 1200px;
  margin: auto;
}

.main {
    background-color: #ffc200;
}

/*Header Section*/

.header {
  padding: 30px 0px 40px;
  margin-left: 50px;
  margin-right: 50px;
}

.header li {
  list-style: none;
  display: inline-block;
}

.header li a {
  color: #333;
  margin:0;
  border:0px;
}

/*Jumbotron Section*/

.jumbotron {
  background-color: #fff;
  max-width: 1200px;
  margin-left: 50px;
}

.jumbotron h2 {
  font-size: 50px;
  margin-bottom: 70px;
}

.jumbotron h2 span {
  color:#ffc200;
}

.jumbotron p {
  text-shadow: 0 0;
  font-size: 16px;
  color: #666;
  margin-bottom: 0;
}

/*Banner Section*/
.banner {
  background-color: #333;
  color: #fff;
  padding: 20px;
  text-align: center;
}

/*Expertise Section*/
.cards {
  background-color: #ffc200;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.col {
  display: inline-flex;
  flex-direction: column;
  justify-content: space-between;
}

#expertise {
  padding: 20px;
  background-color: #ffc200;
  margin: 0;
  text-align: center;
}

/*Footer Section*/
.footer {
  padding: 60px 0px;
  background-color: #000;
  color: #fff;
}

.footer h3 {
  font-size: 20px;
  margin-left: 20px;
}

.footer p {
  font-size:12px;
  margin-bottom: 0;
  margin-left: 20px;
}

```

