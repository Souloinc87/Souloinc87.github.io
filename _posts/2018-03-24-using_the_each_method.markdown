---
layout: post
title:      "Using the .each method "
date:       2018-03-24 01:10:56 -0400
permalink:  using_the_each_method
---


This past week I've been focusing on mastering my loops and how to iterate over arrays in Ruby. One thing that really helped me understand how Iteration and abstraction works was learning the *.each* method. When you have a list of elements within an array, you want to be able to change and update those elments in an easy and understandable way. 

One of my hang ups on arrays was the return value. The easiest way to understand a method is to understand what it returns. In this case the *.each* method always returns the original array that you give to it. So right off the bat we know that we would have to create an empty array and use the "shovel" method ( << ) in order to transfer the elments from the orinigal array into our new array. 

For instance, If I have an array that contains:

        array = [1, 2, 3, 4, 5] 

Lets say that I wanted to return an array with all of those numbers squared. Our code could look something like this using *.each*:

        array.each do |num|
     
		   num * num 
	
	    end
	 
However, if we were to enter this into our IRB we would get:

     => [1, 2, 3, 4, 5]

This is because the *.each* method will only return the original array. What we would have to do is create an empty array to save our updates in and then return that new array. No matter what we want to iterate over using *.each*, it will always return the original array if we don't create another array to save our changes to. 

If we want to return our array of numbers squared, we would first need to create the empty array. 

For example:

         new_array = [ ]
 

Now that we have somewhere for our updated elements to be saved, we incorporate it into our code like this:

        array = [ 1, 2, 3, 4, 5]
     
         
	    new_array = [ ]

          
		array.each do |num|
   
	       new_array << num * num
  
	     end 
  
	       new_array

        end

     
       new_array   #returns => [1, 4, 9, 16, 25]

Basically we've shovelled ( << ) our altered elements inside of our empty array in order to get the results of what our code changed. Of course, once you learn this concept using *.map* or *.collect*, it elimates the need to create an empty array altogether.   


