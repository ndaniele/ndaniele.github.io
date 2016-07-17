---
layout: post
title:  "Sinatra Project"
date:   2016-07-17 15:45:53 +0000
---


When I first started on the Sinatra section it felt like an easy race to the finish line. Sentra, by using Active Record and Rack made everything so much easier. ...At least at first. As I progressed through the labs they went from easy to very complicated without a lot of transition in between, and so I realized I needed to press pause on my progress and go back and review the Sinatra section again. ...So, over the course of about 5 days I reviewed every Sinatra lesson, looked over the code from each lab that I had completed, and made sure that I understood how each model was hooking into each view and how each view was being called by each controller action. 

I started to dream about the code. I saw it as some kind of abstract sound board (an image from when I once worked as a sound engineer) I saw each piece of code as a connection with ports leading into it and with cables coming off of it. My job was to connect them together in the correct way. 

So with that vision in my head I began on the final projects. As soon as I began the Fwitter app I was very glad that I had gone back to review the lesson. I was able to understand all of the code, and even streamline some code patches I found online to make them fit my app. I also had a lot of fun building the fwitter app, as my main motivation for working as a developer is to work on social apps, like twitter (or fwitter in this case). 

For my Sinatra assessment project I created a Fwitter Plus app. Building off of the structure of the Fwitter app and adding an optional category that a user could assign to a given tweet. ...Sort of like a low-tech hashtag. 

Building this Fwitter Plus app was going pretty smoothly in the stubbing out phase. I had a working app, more or less, by the end of my first day of coding, and I went to sleep feeling confident that I could be finished with the assignment early the next day. .... I WAS WRONG!!

The next day I ended up spending about 7 hours online chatting with Learn Experts (primarily @Jnoconner) who helped me debug my Fwitter Plus App. My main problem was that I had called my twitter categories "Type" and, as I soon found out, Rack doesn't allow you to call anything "Type". So I had to create a whole new database and a whole new set of migrations, then I had to track down every instance of the word "type" in all my controller actions and views and change it. (I chose to change it to "genre" which seemed safe since I’ve used that word in multiple previous labs). 

Through the many hours that I worked to debug my code, I was still very happy that I went back and reviewed this entire section. I was able to follow and even anticipate the advice that the Learn Experts were giving me. Because I fully understood the terms and structure of the Sinatra App, debugging became an ...enjoyable (if you can believe it) experience. It was fun to mount the site in shotgun, run it through until hitting an error, and then tracking that error through the levels of my code. I felt like I was beginning to see how actual developers work on real world projects. 

My final app isn't the prettiest, and I don't think it's about to offer Twitter (or even Fwitter) any serious competition on the app store. But I enjoyed building it. It was a confirmation that I have actually been learning something these past months. And it motivated me to learn more! I'm looking forward to seeing what Rails has in store!

