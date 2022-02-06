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
















