# Browser Rendering

Here, we are going to discuss how the browser renders HTML, CSS, JavaScript to DOM. 

![This is an image](https://blog.logrocket.com/wp-content/uploads/2021/06/how-browser-rendering-works.png)

Everyday we use browsers for myriad purposes, but very few of us aware of the processes that happen to get the interactive and wow kind of webpages. Understanding the whole scenario is bit complicated but looks fun to have a look at.


Let's get started.

# A brief explaination the way the browser renders

Without wasting much time let's deep dive into the discussion.


Whenever we search something, the browser gets the data from the servers and interprets and represents the info in the form of web pages. Behind the scene there are so many processes that undergo like,<br>

##### 1. Requesting Servers to provide information by browser engines.<br>
##### 2. Browser engine sends the information to the rendering engine.<br>
##### 3. Rendering engine renders the data.<br>
##### 4. JavaScript interpreter helps browsers to use JavaScript to make web pages interactive. <br>

## Here we focus on Rendering of the data.

### Creating DOM

Rendering engine gets the data in the form of ***HTML***, ***CSS***, ***PNG***, ***JPG***. Brower engine renders the HTML document and creates the DOM-Document Object Model tree, this is like a layout or skeleton of the web page, as shown in the fig. <br>
![This is an image](https://miro.medium.com/max/664/1*PSWV-BqV-2M3TR1qF-UAcw.jpeg) <br>

### Creating CSS

Then the case is with CSS, where the browser cretaes CSSOM-Cascading Style Sheet Object Model just like HTML DOM.<br>
![This is an image](https://api.programmingsoup.com/images/CSSOM.png)

### Creating Render Tree by Javascript

Eventually after this, Javascript combines the both DOM and CSSOM to construct Render Tree.<br>
![This is an image](https://i.stack.imgur.com/6rUqB.jpg)

### Layout and Painting

Render engine creates the layout according to the size issued through the css. The layout consists of size of each node where it will be printed on screen, and according to the render tree it paints the each pixel.

<br>
<br>
<br>


# Mechanism behind Browser Rendering

![This is an image](https://weareadaptive.com/wp-content/uploads/2020/04/critical-rendering-path.jpg)

The basic rendering flow has four steps namely,

- **Parsing** <br>
- **Render Tree** <br>
- **Layout** <br>
- **Paint**

## 1. Parsing

We can define parsing as translating a document into a structure that code can use. In simpler words splitting the complex task into individuals and focussing on each one. Parsing consists of grammar such as Vocabulary and Synatx rules and the other steps involved are as follows,

#### Lexical Analysis <br>
#### Syntax Analysis
#### Lexer (Tokenizer) - Create Tokens
#### Parser - Apply the syntax rules

Parsing is of two types Unconventional Parsing and Conventional Parsing.

### Conventional parsing :

Firstly the information that Render engine gets will be onverted into tokens by the 'Lexer'. 'Parser' constantly requests tokens from the 'Lexer', eventually lexer send the data in the form of tokens. Parser always try to use the tokens based on the syntax rules but if its not possible it stores the tokens and tries to find if the token can be matched to something.

The readily available parsers are :<br>
- Flex
- Lex
- Yacc
- Bison

Webkit uses Flex(Lexer) and Bison(Parser)

This kind of parsing is used for parsing CSS and Javascript.

### Unconventional Parsing :
using this we can parse HTML. We can't use conventional parsing for HTML because of the following reasons,
- HTML is not contex free grammar
- HTML Document Type Definition(DTD) w3c

To put it straight the browser recovers from the errors in the code if it encounters any. As like in the conventional model here too the process happens and render tree will be constructed. 

## 2. Render Tree

- Render tree is generated while DOM tree is being constructed.
- Render tree is a visual elements in the order which they need to get displayed.
- Elements in the render tree are called renderers or renderer objects.
- Render object is a rectangle.

Based on the definiton of DOM element it can be displayed as :
- Render none
- Render inline
- Render block
- Render inline-block
- Renderlist-item

## 3. Layout :
From the render tree the amount of space and geometry is calculated and assigned to their respective positions if the form of rectangles. Most of the time layout happens in one go

## 4. Paint :
The blocks of rectangles which has been constructed from the render tree is being colored by the paint() method and displays content on the page. 
The order of painting is :
- Background Color
- Background Image
- Border 
- children
- Outline


This is how the browser renders HTML, CSS, JS and displays the web pages.











