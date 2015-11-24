Title: Creating a wordcloud from Facebook posts
Date: 2015-11-22
Category: Python
Tags: python
Slug: facebook-wordcloud
Author: Patrick Boyle
Summary: Using python to create a wordcloud from facebook posts

# Creating a wordcloud from Facebook posts
Recently people on Facebook have been posting wordclouds of their posts using a FB app. I thought this was cool, but I didn't really want to give an unknown app access to all my Facebook data. I'm in the process of learning python, so I thought it would be a fun project to try to do this in python.

The full code is located [here](https://github.com/patboyle86/projects/blob/master/FBWallPosts.ipynb) for those who are interested, but I'll show the results below.

## All posts
Here is the wordcloud for all posts on my page.
![All Posts](/images/allposts.png)

Obviously there are a lot of happy birthday posts, my name, beer, etc. What about just my posts?

## My posts
![My Posts](/images/myposts.png)

This is kinda strange...why is "New" so frequent? After digging around the text for a bit I found that I wrote "New Haven" a lot. I decided to replace "New Haven" with "NewHaven" to get around this and made a new wordcloud.

![My Posts](/images/myposts2.png)

Ok hmm, I guess I use the work "now" a lot...

What about just other people's posts on my wall?

## Other posts
![Other Posts](/images/otherposts.png)

Well, well, well...looks like the main reason people post on my wall is to wish me happy birthday. I'll combine "Happy Birthday" and "Happy birthday" into "HappyBirthday" to see what that does.

![Other Posts](/images/otherposts2.png)

So that evens things out a bit. Still lots of birthday wishes. I bet this would show up in the post dates as well.

## Posts over time
Here are the number of posts per month for me and everyone else.
![My Posts per month](/images/mypostsvstime.png)![Other Posts per month](/images/otherpostsvstime.png)

Oh, will ya look at that...seems like October is a popular month ;-)

Now I want to see post frequency over time.
![Posts vs Time](/images/allpostsvstime.png)

Seems like I peaked in late 2011.

## Summary
This was a cool little project. There's other things I could do, like make a wordcloud for each year to see the change, filter just for swear words to see my favorites, but this is good for now. Hope you enjoyed it too!
