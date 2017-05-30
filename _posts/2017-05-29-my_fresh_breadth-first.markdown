---
layout: post
title:  FRESH BREADTH-FIRST
date:   2017-05-29 18:16:45 -0400
---



I recently attended a coding meetup where a group of programmers got together to work on projects and compare notes from the field. 
 
I was struggling with writing a sort algorithm in JavaScript which I was preparing for an upcoming interview, when one of the senior programmers in the group suggested that we all take some time to work on an “*Algo Problem ...you know…just for fun!”*
 
Algorithms …for fun? 
 
The whole reason I came to this meetup was to get some help on the algorithm I had been working on at home, alone, and had not been having very much fun with at all. 
 
I watched while my new friends closed their laptops and got out pens and paper. They spent 30 minutes scribbling ideas and looking alternately brilliant and totally puzzled. By the end of the allotted time, no one had a solution, not even the senior developer who had suggested the exercise, but it did seem like everybody working on the problem was having fun. 
 
I walked away from that meet-up determined to meet my next *“Algo”* challenge with an eye towards fun. Recently I had my chance. 

**A CHALLENGE, SHOULD YOU CHOOSE TO ACCEPT IT**
 
I’ve been working through the JavaScript curriculum in Learn.co from the Flatiron School (the Bootcamp I graduated from) Their curriculum is great and always updating, so it’s a good way to keep my coding skills sharp. 
 
I came across a challenge at the end of one of the lessons, that read: 

![](http://i.imgur.com/mLXpPYk.png)

With my experience at the code meet up fresh in my mind, I decided to complete this challenge, on my own, without extensive googling, and I committed to myself that, come hell or high water,  I would have fun while I picked it apart. 
 
I started by pulling up a JavaScript Repl, and working with the skeleton code that the Learn.co Readme had provided. It was simple code for iterating through an array of nested arrays and calling a function on each iteration.

![](http://i.imgur.com/8Kv7ZcF.png)

It seemed pretty straight forward, could I copy it’s logic patterns and simply swap out nested arrays for nested objects? (notice lines 14 through 18)

![](http://i.imgur.com/T1ONG5L.png)

But when I ran that code on my test array, I got this: 

![](http://i.imgur.com/d5TxECY.png)

Nope! that wasn’t gonna work. 
 
First, I had to realize that you can’t typecheck a JavaScript Object the same way you do an Array. 
 
**TYPEOF() TO THE RESCUE**

![](http://i.imgur.com/X0j9JkC.png)

I reworked my code with **typeof()**, but was still having problems. I stopped getting that TypeError message, but now my function completely skipped over the values in my nested objects. ...why was this happening? 
 
Then I remembered... you can’t iterate through an Object with a **For Loop!**
what will happen to all the **key: value** pairs? 
 
So....
 
**FOR IN LOOP TO THE RESCUE**

![](http://i.imgur.com/XsBCRcW.png)

After reworking my code with a **For In** loop I got the behavior I wanted for an array of nested arrays and objects. 
 
This is where I should have stopped to test my code with a new array, one containing nested objects which themselves contained nested objects, or nested arrays that contained within them nested arrays, or some combination of the two, but I didn’t. 
 
**KNOW WHEN TO QUIT**

In my arrogance, I thought:
 
“I get this, I see what’s going on here, I’ll make this challenge even more complex. I’ll make a function that can search through an array of nested objects, which themselves contain nested objects and arrays! ...let me just add a few extra lines of code to deal with objects nested inside of objects.”
 
so I went about adding multiple repetitious lines to my code:

![](http://i.imgur.com/MpXB0zq.png)

The solution was ugly,  but  when I tested my function on an array with nested objects inside of nested objects the function call worked the way I wanted it to. 
 
Tested with: 

![](http://i.imgur.com/fOkE29i.png)

//Returns: 44
 
So I felt that I had succeeded and decided to call it a night. 

**THE MORNING AFTER**
 
The next morning I was looking over the code I wrote and trying to think how I could refactor all that extra logic to make it less ugly. So I deleted a line...

...and then another line...

Then I read my code again from top to bottom and realized that the lines I had been so quick to include the night before were already accounted for within the logic of the While loop!!
 
So, while I was manually looping and re-looping for each possible condition, the while loop was also doing this same logic for me. (Which explains some of the oddly long *console.log(current)* statements I kept getting). 
 
I realized, that the power of this breadth first search algorithm is in its ability to deal with multiple scenarios (array of nested arrays, array of nested objects, array of objects containing nested arrays, array of arrays containing nested objects containing arrays…. etc) 
 
I also fully understood the mechanism that the algorithm uses to be so efficient. it searches **BREADTH FIRST**. looking across the given array, before going down into it’s nested children. 
 
This abstracts away all the issues with nesting that I was trying to account for with my extra (and very non-DRY and ugly) code. By popping each element or value into a *Next* array, Breadth-First reduces all nested values into a flat array, and then simply checks to see if the criteria function returns true for any of those arguments! 
 
This was my Eureka moment. 

It felt great, and, most importantly, I had a lot of fun working through this algorithm! 
 
That is the first time I think I have ever said that! It will not be the last.
 
Thanks Breadth-First! 
 
 
**MY FINAL CODE:**

![](http://i.imgur.com/ajL4206.png)











