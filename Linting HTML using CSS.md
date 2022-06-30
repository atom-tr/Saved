# Linting HTML using CSS
* Source: [Linting HTML using CSS - bitsofcode](https://bitsofco.de/linting-html-using-css)

## Inline Styles
```CSS
*[style] { 
    border: 5px solid red; /* Style to make the elements noticeable */
}
```
## Faulty or Missing Link Targets
```CSS
a:not([href]),
a[href="#"],
a[href=""],
a[href*="javascript:void(0)"] { … }
```
## Unaccessible Images
```CSS
img:not([alt]) { ... }
```
>
```CSS
img[alt=""] { ... }
```
## Missing Document Language
```CSS
html:not([lang]),
html[lang=""] { ... }
```
## Incorrect Character Set
```CSS
meta[charset]:not([charset="UTF-8"]) { ... }
```
>
```CSS
meta[charset="UTF-8"]:not(:first-child) { ... }
```
## Unaccessible Viewport Attributes
```CSS
meta[name="viewport"][content*="user-scalable=no"],
meta[name="viewport"][content*="maximum-scale"],
meta[name="viewport"][content*="minimum-scale"] { ... }
```
## Unlabelled Form Elements
```CSS
input:not([id]),
select:not([id]),
textarea:not([id]) { ... }

label:not([for]) { ... }
```
>
```CSS
input:not([name]),
select:not([name]),
textarea:not([name]) { ... }
```
>
```CSS
form:not([name]):not([id]) { ... }
```
## Empty Interactive Elements
```CSS
button:empty, 
a:empty { ... }
```
## Unnecessary or Deprecated Attributes
```CSS
script[type="text/javascript"],
link[rel="stylesheet"][type="text/css"] { ... }
```
