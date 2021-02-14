---
date: 2020-12-31
tags: "['coding', 'rxjs', 'learning']"
layout: layouts/post.njk
title: Flattening Out with RxJS
description: How I finally came to understand the RxJS flattening operators.

---
### The journey

The Pluralsight course "Play by Play: Angular and ngrx," \[VERIFY AND GET LINK\] Duncan Hunter mentions that the learning curve of [RxJS](https://rxjs-dev.firebaseapp.com/ "RxJS home page") can be visualized through a repeated pattern of small flat periods of understanding followed by sheer ascents of struggle. This post is about my latest journey through one of those ascents: struggling to understand the flattening operators of RxJS.

#### Operators of interest

This part of the RxJS journey specifically delves into the so-called flattening operators: concatMap, mergeMap, switchMap, and exhaustMap \[LINKS FOR THESE\].

### All over the place

I still consider myself _just_ beyond a beginner when using reactive programming and RxJS. After a couple years spent primarily as a front-end developer, I've gained enough experience to feel somewhat comfortable with it. More comfortable than knowing enough to be "dangerous," but maybe not enough to work myself out of every jam. But I enjoy coding with RxJS, especially since I'm more of an HTML and CSS, front-of-the-front-end kind of guy. And all of our applications at work use Angular, which heavily utilizes RxJS and reactive programming (which, not to mention, makes reactive UIs much more, well, reactive), so RxJS really provides some spice to the normal logic coding.

But among the successes were the aforementioned struggles, one them being particularly long-lasting, which is: How the heck does a `concatMap` operator differ from a `mergeMap`? Or a `switchMap`? `switchMap` seems to be used more often that the others, but why? And then there's even `exhuastMap`. More like `exhaustedMap`. 

When using these operators in simple observable streams, the results seemed exactly the same: an observable goes in, and a different observable goes out. OK. But just by definition -- literally, by the definitions in the official RxJS docs, as well as on the very-helpful LearnRxJS site -- I knew they couldn't be the same. To try and get through this upward slope, I read many articles and watched many videos purporting to explain the differences. The one comparing the operators to office jobs \[NEEDS LINK\], and the ever-helpful Deborah Kurata's ng-conf presentation helped me understand results, but not understanding. And until I achieved understanding, there was still potential for misuse.

But as with understanding a lot of things, you not only need to be given the correct information, but be given it in a way _that you understand_. Everyone's brain works differently, and there is no one-size-fits-all solutions to insight. And I was waiting for my own light-bulb moment.

### The light-bulb moment

Episode XXX of ng-conf's Angular Show had on guests \[NAME EPISODE AND SHOW\] to talk about some of these operators. I listened in as usual, a regular listener of the show, not expecting insight but more a boning-up of what I already knew, having apparently conceded to a fate of lack of understanding. 

I was shoveling snow in our driveway at the time, and when the insight came, I stopped shoveling. I rewound the podcast and listened again. That was it. _I got it._

For these flattening operators, the magic happens not for observables comes into the operator callback function. The important part for these operators is _which observables leave it_ \[EDIT FOR CLARITY\].

And that was what I'd been looking for. I mean, in hindsight, it seems obvious: operators take values and return different values. But that hadn't previously clicked for me. I just needed a change in perspective, and then it was like the last piece of the puzzle  -- a really big piece -- being slotted right into place.

#### Examples

\[Create code on CodePen and paste code examples with comments showing console output here\]

#### Conclusion

Of course, after coming to this understanding, I thought back of implementations that used RxJS and used one or more of these operators, and using one and shrugging and going on with my day, knowing in the back of my mind that I'd potentially added a bug down the line. You can't help these sort of things.

But I'd reached a new plateau of understanding. I took the moment to catch my breath after a lengthy climb, and I looked back down the mountain and saw how'd far I come. 