---
layout: post
title:  "Abstraction for Legibility and Adaptation"
date:   2017-07-07 17:52:18 +0000
---


An important concept around variables and methods is the idea of using abstraction when writing code. Abstraction in writing code allows for creating a legible interface when reading and modifying code. It's like condensing code to its purest form, minimizing repetitions by using class readers. The Advanced Class Methods lesson explains that the lowest level of abstraction is simply calling a variable in order to expose data. A more refined way to do so its to call on a class itself using #self. The example given was using #self.all to read the contents of an array as opposed to calling the class variable @@all directly. By using the former instead of the latter, if the name of the class variable needs to change, you only need to go to one place to do so. 

Another example of abstraction, which works from the previous example, is encapsulating a class method. The lesson gives a final example of the visual differences between abstraction versus literal implementation with this comparison: 


Person.all.detect{|p| p.name == "Ada Lovelace"}
 
Person.find_by_name("Ada Lovelace")


In some ways, encapsulating a class method is a way for you to get to the core of what you're trying to achieve when writing a piece of code. It leaves out extraneous information that might clog up your code, which can be prevented when you lay out a plan of what's needed and what's expectedin your code. In the very first words, you can understand that you will be using the name class variable with a find method (or detect in this case). 






