## Box Line Graph By SVG in html 

### Introduction
This code is part of course project [CS6280](http://www.comp.nus.edu.sg/~sites/cs6280/week1.html), school of computing, NUS.
This simple script is a prototype of our final box line graph which shows the traced events on different CPU.
Now it only has basic features of the graph, but more features later can be implemented using the same idea here. And the idea is simple enough.

### Idea
[Draw Box Line Graph Using JavaScript+SVG --- Hand by Hand](https://docs.google.com/document/d/1thR_uHmaZhuNjbCk6WJZ1E-DNqS60jVItxtxHZfSe5w/edit?usp=sharing)


### Platform
Runing on 
* Chrome 53
Didn't test on other web brower.

Write on
* Any text editor you like.

### How to run 
Directly drag the boxLine.html file into a brower.

or

In the terminal opened at the directory of our file: 
```
google-chrome boxLine.html
```

### Program Input 
For now, the program input are defined as follows:  

*4* JavaScript arrays directly writen in code, and each array contains a number of elements. Each element contains 2 intagers and 1 string: *startTime*, *endTime* and *type*.
These elements each represents an event running on CPU. The *startTime* and *endTime* stands for the event start and end time, while the string *type*,
for now(remember this is just a prototype), just has three values "line", "smallBox" and "bigBox". 

For example, an array can be [[0,100,"line"],[100,150,"bigBox"],[150,180,"line"]]

    
### Parameter Settings
Now we have a few parameters to set the graph. They are at the beginning of the code.
* The width of idle line, default only 2 px: *lineWidth = 2*; 
* The width of white lines at each time tag points, default 1 px: *seperatorWidth = 1*;  
* The distance between two time tags, defualt 70px: *seperatorDistance = 70*;
* The vertical length of the event Box: *bigBoxWidth = 30*, *smallBoxWidth = 20*;
* The ratio of inner color area over total area of an event box: *innerBoxWidthRatio = 0.4*; // Two color not implemented yet. 
* The blank spaces between two cpu lines, defualt 50px: *cpuLineMargin = 50*; 
* The maximum length of a CPU line, now set to 2000px: *maxLength = 2000*;


### Futher Works 
1. Add time tag text.
2. Add CPU numbers text.
3. Implement the 'two color' box.
4. Add a layer to convert real CPU events data to our *element* in the input array.
This includes:
* Add control to event color.
* Convert microseconds float number to our *startTime* and *endTime* in the *element*. 
5. Design zoom-in and zoom-out. (Remember we are in a web brower.)

### Team Member
* Liu Zhendong - Tony
* Gao Xiang 

### Reference
1. [SVG tutorial - rectangle](http://www.w3schools.com/graphics/svg_rect.asp)
2. [JavaScript tutorial - output](http://www.w3schools.com/js/js_output.asp)

