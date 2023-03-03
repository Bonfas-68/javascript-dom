# javascript-dom
<body onload="alert('hello internal js!!');">
    <h1>Hello inline Javascript</h1>
</body>

<body>
    <h2>JS before end tag of the body</h2>

    
    <script type="text/javascript">
        alert("Hello!!");
    </script>
</body>

<body>
    <h1>External Source</h1>
    <script src="index.js"></script>
</body>

Browser loads elements from top to bottom so take care of how you arrange the css, js in the document e.g the css link should always be ontop of the javacript in the head tag, and javascript recommended position be before the end body tag.

The DOM Document Object Model gives the structure of your document to help in manipulation of it's elements. Using the dot notation to tap into the properties and methods

#####
document.getElementById("title");
<h1 id=​"title">​Hello​</h1>​
document.querySelector("#title");
<h1 id=​"title">​Hello​</h1>​
document.querySelector("#list");
<ul id=​"list">​…​</ul>​
document.querySelector(".item a");
<a href=​"https:​/​/​www.google.com">​Google​</a>​
document.querySelector("li.item");
<li class=​"item">​…​</li>​
document.querySelectorAll(".item");
NodeList(3) [li.item, li.item, li.item]


<!-- Manipulating text using Javascript -->
innerHTML = displays or changes everything within the selected element
textContent = displays or changes the original content 

###Manipulating attributes
document.querySelector("a").attributes;
NamedNodeMap {0: href, href: href, length: 1}
document.querySelector("a").setAttribute("href", "https://www.bing.com");
undefined
document.querySelector("a").getAttribute("href"(;
VM3027:1 Uncaught SyntaxError: Unexpected token ';'
document.querySelector("a").getAttribute("href");
'https://www.bing.com'
