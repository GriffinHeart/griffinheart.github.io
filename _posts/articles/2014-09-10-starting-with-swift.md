---
layout: post
title: Starting with swift 
excerpt: "From hating obj-c to starting with swift."
categories: articles
tags: [swift, iOS, Tokyo last train]
comments: true
share: true
---

I was never a fan of obj-c, I don't like looking at it, it looks alien, disorganized and unclean.

I guess the problem comes from having my first experience with obj-c after having started working with Ruby and Ruby on Rails. Frankly it doesn't make much sense, I've worked with C and C++, maybe it just the method calling syntax or the Xcode IDE.

This never looked pretty to me:

{% highlight objc %}
    UITableView *newTableView = [[UITableView alloc] initWithFrame:dropDownTableFrame
                                                         style:UITableViewStylePlain];
{% endhighlight %}

Naturally when Apple announced the release of Swift I said to my self "nothing can be worse than obj-c", so I wanted to give it a try.

Enter **Tokyo Last Train**, an Android application built by [Edern](https://www.behance.net/edern), [Iolanda](pt.linkedin.com/in/yolandacorreia) and me.

Small application, about 3 screens (splash, main, results) and 2 input boxes. Sounds simple enough. Now if I just had the time to focus on it.

Around this time I decided I wanted to meet more developers in Tokyo, so I joined a few meetups and doorkeeper events. One of those is the [Tokyo iOS Meetup](http://www.meetup.com/TokyoiOSMeetup/) which has a coding club every few weeks. Awesome, I'll meet other folks, port the app and learn more about iOS and swift. 

The first coding club I went was in August 4th, organized by [Ahart](http://www.meetup.com/TokyoiOSMeetup/members/75042762/) and [Jonathan](http://www.meetup.com/TokyoiOSMeetup/members/2013655/) at a space provided by [Luxstack](luxstack.com), big thanks to them.

###So here is what I learned

My objective for that coding club was to have an application that showed 2 input boxes and a button after you press the button you get some results. Here's how it looked:

<figure>
	<img src="/images/first-results.jpg" alt="First results from the coding club">
	<figcaption>Result after the coding club</figcaption>
</figure>

Not very impressive, but I went from 0 to something. I learned a few things about `Storyboards` and Swift `optionals`.

####Storyboard

Its very easy to click the `.storyboard` file and start putting boxes, labels and all kinds of stuff in your layout, but then what? I need to connect the layout with code.

Xcode looks like a proper IDE, something tells me I don't need to go and do it manually. A few google searches and I couldn't find any good results. Oh, I'm in a coding club, theres people around me, I should talk to them. Note to self: socialize more, people rarely bite.

See that button there, the one that looks like a tuxedo and bow tie button? Press that and you get a side by side code view and layout view. From then on you can drag from the `outlets` and `actions` to code and Xcode will insert the relevant stuff. Here's a gif:

<figure>
	<img src="/images/outlet.gif" alt="How to connect layout to code">
	<figcaption>Ctrl + drag and drop to code</figcaption>
</figure>

####Optionals and the bang !

Coming from Ruby the bang `!` is something that we're used to see. But in swift it takes another meaning.

Swift has the concept of optionals, from the docs: 

> Swift also introduces optional types, which handle the absence of a value. Optionals say either “there is a value, and it equals x” or “there isn’t a value at all”.[^1]

Optionals are pretty easy to understand, but if you noticed, on the gif, the outlet is created as: 

`@IBOutlet var toTextField: UITextField!`

The bang means this is a implicit unwrapped optional. The usefulness of this is for initialization purposes, you should use it only if something is `nil` at the start but after initialization it will always have a value. This stackoverflow answer is pretty good in explaining it: 

[Why create "Implicitly Unwrapped Optionals"?](http://stackoverflow.com/a/24026196)


All in all the coding club was a very nice experience, its fun to be with other people that are also working on their personal projects and talk with them. I've decided to port **Tokyo Last Train** using only the coding club meet ups.

Swift looks like a very huge improvement over obj-c in my opinion, learning the language is as hard as any other language. The big challenge here is in getting to know the APIs of iOS and OSX and being proficient in the editor.

Oh and by the way, did I tell you **Tokyo Last Train** is available in the [Google Store](https://play.google.com/store/apps/details?id=com.tokyolasttrain&hl=en)?

[^1]: <https://developer.apple.com/library/prerelease/mac/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html>
