## Box Line Graph By SVG in html 

### Introduction
This code is part of course project [CS6280](http://www.comp.nus.edu.sg/~sites/cs6280/week1.html), school of computing, NUS.

This code not parse the '.trace' file, you need to parse the trace file yourself and output the events in a file.
Then this program will convert your output file into a picture in the web browser.


### Idea
[Draw Box Line Graph Using JavaScript+SVG --- Hand by Hand](https://docs.google.com/document/d/1thR_uHmaZhuNjbCk6WJZ1E-DNqS60jVItxtxHZfSe5w/edit?usp=sharing)


### Platform
Runing on 
* Chrome 53
Didn't test on other web brower.

Write on
* Any text editor you like.

### How to run 
1. Directly drag the boxLine.html file into a brower.
2. Press the "Choose File" button, and choose 'trace153809.txt' under the same program directory, or your own input file.
3. Press the "Begin Draw" button, after a while, the graph will shows on your screen.

Tips1: You can zoom-in and zoom-out by the browser. (Ctrl +/-)
Tips2: If you are using Chrome, use this one to capture a full picture of the graph: [Full Page Capture Extension](https://chrome.google.com/webstore/detail/full-page-screen-capture/fdpohaocaechififmbbbbbknoalclacl?utm_source=chrome-app-launcher-info-dialog)

### Program Input 
This program input from a file that stores events as below formats:

<cpu>, <eventStartTime>, <eventEndTime>, <color1>, <color2>, <type>

Each represents the cpu number, the event start time in 0.1 us, the event
 end time in 0.1 us, the two colors you wants to use for this event, and the
`<type> is in  {user, trap, syscall, irq, idle}`.

For example, the First 10 lines of the Trace 153809 should be:

```
2 14766898778511278 14766898778511283 (10,48,80) (100,128,200) syscall
2 14766898778523730 14766898778523735 (10,48,80) (100,128,200) syscall
2 14766898778523547 14766898778523867 (28,150,125) (55,92,241) user
2 14766898778523841 14766898778523846 (10,48,80) (100,128,200) syscall
2 14766898778523904 14766898778523909 (10,48,80) (100,128,200) syscall
2 14766898778523995 14766898778524051 (10,48,80) (100,128,200) syscall
2 14766898778524142 14766898778524264 (10,48,80) (100,128,200) syscall
2 14766898778524280 14766898778524323 (10,48,80) (100,128,200) syscall
2 14766898778523867 14766898778524385 (249,27,234) (166,217,218) user
2 14766898778524367 14766898778524372 (10,48,80) (100,128,200) syscall
 ...
```
Use `Choose File` button to choose a file like above, then browser will give 
you the graph.
    
### Parameter Settings
Now we have a few parameters to set the graph. They are at the beginning of the code.
* The width of idle line, default only 2 px: *lineWidth = 2*; 
* The width of white lines at each time tag points, default 1 px: *seperatorWidth = 1*;  
* The distance between two time tags, defualt 70px: *seperatorDistance = 70*;
* The vertical length of the event Box: *bigBoxWidth = 30*, *smallBoxWidth = 20*;
* The ratio of inner color area over total area of an event box: *innerBoxWidthRatio = 0.4*; // Two color not implemented yet. 
* The blank spaces between two cpu lines, defualt 50px: *cpuLineMargin = 50*; 
* The maximum length of a CPU line, now set to 2000px: *maxLength = 2000*;


### Future Works 
1. Add time tag text. Done.
2. Add CPU numbers text. Done.
3. Implement the 'two color' box. Done.
4. Add a layer to convert real CPU events data to our *element* in the input array.
This includes:
* Add control to event color. Done.
* Convert microseconds float number to our *startTime* and *endTime* in the *element*.  Done.
5. Design zoom-in and zoom-out. (Remember we are in a web brower.)

### Team Member
* Liu Zhendong - Tony
* Gao Xiang 

### Reference
1. [SVG tutorial - rectangle](http://www.w3schools.com/graphics/svg_rect.asp)
2. [JavaScript tutorial - output](http://www.w3schools.com/js/js_output.asp)

