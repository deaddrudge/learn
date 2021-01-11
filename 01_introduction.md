Please note, all things in caps are keywords that should be understood in time. Wikipedia does a good job at this; do your research, but don't kill your brain with it too fast, lots of things to cover.

# Before you can begin, make sure you have these tools

### A Computer
ideally with a real keyboard
### Visual Studio Code 
(weapon of choice for writing code)
https://code.visualstudio.com/Download
### Node.js 
installed to computer
https://nodejs.org/en/download/
### Chrome browser...
currently the best browser for development


```
Make sure you install all of these as the first priority
```



## Preamble
In today's world, the barrier to learn coding skills is actually quite small. The internet which has evolved for decades has created the most widely available platform on the planet, and the underlying languages and protocols of that platform are freely available and well documented. Compare that to 30 or more years ago and you can see how far things have progressed.

The underlying foundation of every website are the following components. These components can be argued and nuanced, but assuming your knowledge and time is limited, as mine was at the time I learned, here is a good paradigm to see it.

### Basic Parts
* Network
* The Server
* And the HTML it outputs

## The network
In brief, there is a network protocol (TCP/IP) which connects computers together when they either plug into a wired connection (LAN), use wifi, or even use wireless connection. This protocol has many parts, but to boil it down to what is critical in understanding, there are IP addresses (numbers like 123.22.11.11) Ports (:3000 or :80 which is default) and names. When you type a name like foogle.com into the address bar, the browser appends something like http:// to the beginning, making it http://foogle.com/. Also of note, it's using the default port, so an http address will be set to :80, while https will be :443. This http is just one protocol available on browsers, there are many others.

## The Server

Breaking these down further, the server can be thought of as a program running on a computer. That computer is on a network, and by the magic of DNS (Domain Name Server) a domain name is translated into an IP (Internet Protocol) address that corresponds to that computer. That computer then has that request, and must then route that 'request' to the right program.

That HTTP server program is running constantly, typically as a background program that only fires when someone activates it with a request. 

Once the HTTP server program has the request, it will try to respond. It does this by splitting the url into chunks and trying to match those chunks to a route. If no match is found it will return an error, but if a match is found it will return a response.

Typically the HTTP server will try to return an html page, but alternatively it will return data in the form of JSON text. 

Complex websites will break up responsibilities to different servers. For example, you can have one website that returns HTML, and another that returns JSON. In this way you can separate the complexity into distinct components. This is known as separation of concern. Often teams will be split into different groups that focus on their own areas of concern to speed up development.

## HTML

Now for what I consider the fun part and my area of specialty. The HTML is really what you will see on the browser. It covers the styling (CSS), the MARKUP (HTML), and any javaScript.  is itself broken into areas of concern. Separation of concern is a common thread throughout the whole process to manage the complexity of the whole. 

HTML is a collection of protocols, but it's primary purpose is to convey information in an organized way. In the evolution of the web, javascript has come to play a critical role in building modern websites. Along with CSS the basic building block of almost any web based application can be achieved.

Important parts of HTML
* Markup (html)
* Scripts (javascript)
* stylesheets (css)

## Markup

The actual markup language of html is fairly simple once you get used to it. Information flows from top to bottom, and things are grouped by HTML TAGS.

list of tags here: https://www.w3schools.com/TAGs/

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Grassland Project</title>
  <link rel="stylesheet" type="text/css" href="style.css" />
</head>
<body>
  <header>
    <h1>Hello world</h1>
  </header>
  <main>
  This is the world... hello then
  </main>
</body>
</html>
<script type="module" src="main.js"></script>
```

Contained in this markup are all of the elements needed to render a page or perform some kind of action.

## JavaScript

JavaScript is arguablly the most important software language in the world right now. If you know this simple and powerful language, you will have job security for the rest of your life. Not only that, but you can build powerful applications and pretty much anything. The web browser has become the new paradigm in that every computer has one, and if the code works on one browser, it probably works on every browser. In this way the browser has become a way to write something one time, and let it proliferate across every possible platform. Learn this!

```javascript
const dog = {
  hello : true
  , there : false
  , maybe : true
  , you : "want"
  , to : "learn" 
}

console.log(dog)
// { ...hello : true, ...}
console.log(dog.hello)
// true
console.log(dog.there)
// false
console.log(dog.maybe)
// true
console.log(dog.you)
// "want"
console.log(dog.to)
// "learn"

// this is how you create functions that do stuff
function alertSomething (thing) {
  alert(thing)
}

// this is how you create timers that do something in time
setTimeout(function() {
  alertSomething( "That did something" )
}, 4000) // 4000 is roughly 4 seconds
```

## CSS

Though it has not evolved quite as much as javascript, css still offers a powerful arsenal to craft the look and feel of an application.
```css

/* 
  Set the default of the body, which is the main tag for everything
*/
body {
  color : blue;
  font-size:16px;
}

/* 
  for some reason you want to make all A tags 
  that are direct decendents of the BODY tag red 
*/
body > a {
  color : red;
}

```

That's probably way more than enough to digest, please write me with questions.

## Action Items
* Get Computer (real computer with keyboard)
* Install Visual Studio Code
* Install Node.js
* Install Chrome if not already installed