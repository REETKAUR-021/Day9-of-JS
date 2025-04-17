<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOM PART 2</title>
</head>
<body>
    <div id="box" name="DIV">
        this is a div
        <ul>
            list
            <li>item1</li>
            <li>item2</li>
        </ul>
    </div>
    <p class="paragraph">this is a paragraph</p>
<script>
    let div = document.querySelector("div");
console.log(div);

//to get the attribute value

let id = div.getAttribute("id");
console.log(id);

let name = div.getAttribute("name");
console.log(name);

let paragraph = document.querySelector("p");
console.log(paragraph.getAttribute("class"));

//to set the attribute value

let para = document.querySelector("p");
console.log(para.setAttribute("class" , "newClass"));

//Style
let div1 = document.querySelector("div");
console.log(div.style);

div.style.backgroundColor="green";

div.style.fontSize="20px";

div.innerText="HELLO!";

//insert elements

let newEl = document.createElement("box");
console.log(newEl);

let newBtn = document.createElement("button");
newBtn.innerText="click me!";
console.log(newBtn);

//append
let div = document.querySelector("div");

div.append(newBtn); //adds at the end of node(inside)

div.prepend(newBtn); //adds at the start of node(inside)

div.before(newBtn); //adds before the node(outside)

div.after(newBtn); //adds after the node(outside)

let p = document.querySelector("p");
p.after(newBtn);

let newHeading = document.createElement("h1");
newHeading.innerHtml = "<i>hi , I m new!</i>";
document.querySelector("body").prepend(newHeading);

//Delete elements
let para1 = document.querySelector("p");
para1.remove(); //remove the node

newHeading.remove();

</script>
</body>
</html>
