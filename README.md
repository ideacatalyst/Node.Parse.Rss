node-parse-rss
==============

A quick node.js RSS feed parser.

Original **quest**ion:
http://stackoverflow.com/questions/20177259/requesting-rss-feeds-from-two-web-sites-in-node-js
Saw this question on Stack Overflow and decided it merited a quick answer.

The author also posted it on LinkedIn:
http://www.linkedin.com/groups/Parse-RSS-feeds-using-Nodejs-2906459.S.5811745652475990020

## Try it yourself

Clone/copy this repo to your local machine:
```sh
git clone https://github.com/nelsonic/node-parse-rss.git
```
Install the modules:
```sh
npm install
```


## Initial Overview

From the original code on StackOverflow Maksim is using the following 
*non-core* node modules: 

1. **async**: https://github.com/caolan/async
2. **request**: https://github.com/mikeal/request
3. **feed-read**: https://github.com/sentientwaffle/feed-read

The firts two (async and request) are *uber* popular node modules that
have been tested by thousands of people and used in many high-profile projects.

feed-read on the other hand ...

![feed-read module page](http://i.imgur.com/Y3oqs0x.png "feed-read module")

only **5 watchers** at the time of writing (*not v. popular*)
and it was *last updated* **2 years ago** ... (might not be compatible with 
the latest version of node.js or its dependencies!)
but it *does* have **unit tests** which is a *good sign* so lets *try* it!

## Read the Readme & Unit Tests in feed-read Module 

Often developers neglect to document their work adequately in the README.md 
If this is the case, the best way of learning how to use a new module is to
read through the unit tests in the ./**test** folder in the case of feed-read

https://github.com/sentientwaffle/feed-read/blob/master/test/index.test.js

The tests are very clear. And the module is well written.

> I sent a clarifying question on LinkedIn:

- - -
Hi Maksim! 
Great question! (useful for other people learning node.js asynchronous callbacks) 

Just to clarify, when you say you "can't understand how to display the parsed result" do you want to combine the results of multiple RSS feed requests into a single http response to your clients? Or just want help styling the output into html? 

Also, are you deliberately trying to keep it simple by only using http module? 
(e.g. are you open to using framework like connect to take care of error handling and html template rendering?)
- - -

