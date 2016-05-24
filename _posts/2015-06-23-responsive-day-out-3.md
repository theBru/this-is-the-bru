---
layout: post
title: Responsive Day Out 3
excerpt: A write-up of the third and final Responsive Day Out
---
Last Friday I attended the third (and my second) [Responsive Day Out](http://responsiveconf.com), organised by [Jeremy Keith](http://adactio.com) and the folks at [Clearleft](http://clearleft.com). Like the first one I attended two years ago, the talks were highly informative, engaging, and inspiring. For a relatively low-budget event, it has delivered the goods in abundance.  

Without further ado, here's a write-up of (and some of my thoughts on) each of the talks from Responsive Day Out 3.  

## Alice Bartlett (Government Digital Service)
Alice Bartlett's talk was around looking for the business case for accessibility (a common theme in this year's conference). She went through some stats about [GOV.uk](http:gov.uk) (19m visits a week; 330 department and organisation websites) and talked about the evolution of the site from its non-accessible Alpha version to its current fully accessible one. To make sure GOV.uk was accessible, it was tested with people with a broad spectrum of disabilities (both permanent and temporary).  

Alice defines accessibility a little differently from the dry and clinical [WCAG definition](http://www.w3.org/TR/WCAG20/), in that accessibile sites are built for inclusion. She quoted Anne Gibson’s A List Apart article, [Reframing Accessibility for the Web](http://alistapart.com/article/reframing-accessibility-for-the-web): “We can reframe accessibility in terms of what we provide, not what other people lack”.  

She was quick to point out, though, that there is no tangible evidence for a business case to justify the time and money spent on making a website / app accessible, with the exception of avoiding litigation. This is especially an issue with higher profile sites. However, this doesn’t mean that smaller sites with less chance to be sued shouldn’t pay any attention to accessibility.  

She concluded her talk by saying that accessibility should be baked in to how we’re making websites, that it shouldn’t be an add-on to the process, but rather the process itself. Because, after all, making sites accessible is the right thing to do.  

## Rachel Shillcock
Continuing the theme of accessibility, [Rachel Shillcock](https://www.rachilli.com/) talked about the close relationship between accessibility and responsive design. The gist of her talk was that accessible design is responsive design is accessible design.  

The theme of inclusion for all was also reflected here where she stated that websites and apps should be open and accessible to all regardless of disability (or lack thereof). Yes, there are too many things to concentrate on when building accessible websites, such as responsiveness, colour contrast, size of elements, spacing and whitespace, HTML structure, content structure, font style and weights, link styles, hover / active / focus states, subtitles or captions for media, no-JavaScript scenarios, page weight and performance … but if accessibility is integrated into the workflow, it becomes less of a burden on the designer / developer to create accessible experiences.  

Some tools and resources she’s suggested were:  

* Lea Verou's [Contrast Ratio](https://leaverou.github.io/contrast-ratio/)  
* [HTML CodeSniffer](https://squizlabs.github.io/HTML_CodeSniffer/)  
* Aaron Gustafson's book [Adaptive Web Design](http://adaptivewebdesign.info/)  
* Colour blindness check in PhotoShop  
* Paciello Group's [Colour Contrast Analyser](http://www.paciellogroup.com/resources/contrastanalyser/)  
* [Color Oracle](http://colororacle.org/)  
* [tota11y](https://khan.github.io/tota11y/)  
* Web Developer Toolbar for Firefox and Chrome / Opera  
* [The Accessibility Project](http://a11yproject.com/)  

## Alla Kolmatova (FutureLearn)
[Alla Kolmatova](http://www.craftui.com/)‘s talk was around modular design process. One of the highlights of the event, she defined modular design by likening the process to building something with Lego. Each element (or group of elements) are replaceable and reducible bits that make up a whole. Not too dissimilar to Brad Frost’s [Atomic Design](http://bradfrost.com/blog/post/atomic-web-design/) system.  

She gave some practical examples of the radical changes it requires to your workflow to implement modular design and the initial struggles that comes with the territory. However, the rewards far outweigh the pains. One of the key things in modular design is the lack of shared language – what do you call each element / piece / widget?  

Going in the territory of Patrick Rothfuss’s [The Kingkiller Chronicle](https://en.wikipedia.org/wiki/The_Kingkiller_Chronicle), she points out the importance of naming things. Giving names based on design is a short term solution. Functional names are difficult to come up with and may still fall short. Her solution is to come up with high-level functions that each team member will be able to understand. She went on to say that “modularity needs a strong language foundation, established by the team who uses it”.  

Building a pattern library is an important starting point, which involves naming things. After which the team, with the help of users, will play a key part in assembling these components in meaningful entities. However, it is still very important to look at the big picture before going to the nitty-gritty of each of the component. The individual pieces may be well-designed and named, but they still need to function as a whole when put together.  

## Peter Gasston (rehabstudio)
[Peter Gasston](http://www.broken-links.com/) gave us a glimpse of the next big thing, which is already upon us: Web Components.  

Web Components are reusable, composable, and encapsulated widgets. They work independently from the host site’s CSS or JavaScript rules, but you can control these widgets by tapping in to their inner workings. An example is the ```<picture>``` element.  

Web Components are made up of the following:  

* **Templates:** these are fragments of inert HTML and only becomes active when told to do so  
* **HTML imports:** these are similar to the ```<link>``` element in the site header, but this is bad for performance as the browser will stop rendering as it imports these HTML fragments. The future is bleak for HTML imports, as these will probably be replaced when ES6 comes out.  
* **Shadow DOM:** this is markup hidden within the element and so it is not visible to the browser. An example is the ```<video>``` element with its controls. These are very hard to polyfill, so difficult to maintain.  
* **Custom elements:** these are meaningful markup with bespoke properties. An example code is as follows:  

### JS
{% highlight javascript %}
document.registerElement('fun-times');
{% endhighlight %}  

### HTML
{% highlight html %}
<button is="fun-times"></button>
{% endhighlight %}  

But there is a lot of technical resistance to this.  

There is work to bring standards to Web Components as the engagement level has dipped over the last few months. One way to standardise Web Components is [The Gold Standard](https://github.com/webcomponents/gold-standard/wiki), which is a checklist of everything a Web Component should have.  

When working with Web Components Peter gave the suggestion to follow the [Unix philosophy](https://en.wikipedia.org/wiki/Unix_philosophy) of a modular approach (similar to Alla Kolmatova’s modular design principles).  

## Jason Grigsby (Cloud Four)
[Jason Grigsby](http://blog.cloudfour.com/author/jason-grigsby/) talked about responsive images and and the ```<picture>``` element, which can now be used in Firefox and Chrome / Opera and is in development to be available in IE and Safari.  

He continued with several use cases to use responsive images, such as resolution switching , which includes display density, and art direction. When it comes to where and how to crop images responsively, art direction will play a part. For instance when an image has text over it, where do you have the breakpoints and how do you treat the font?  

One way to make a decision about breakpoints is to maintain a performance budget – it takes more memory to resize a large image than it is to resize a smaller image (same applies to cropping), so when selecting the breakpoints, making sure it remains within the performance budget would be an indicator to determine the breakpoints.  

Upscaling shouldn’t be a scary thing either. If an image is 400×400, upscaling it to a 405×405 slot is not too bad. How far you will go depends on the image and the art direction. But upscaling should be considered an option nonetheless.  

A difficult task is to work with hero images, which are marketing tools. Text resizing may be the only viable option when it comes to working with hero images. It is also important to pick the right attribute: media will tell browser what to do; srcset will give browsers options.  

[JPEG2000](http://www.jpeg.org/jpeg2000/), a newer image file type, is now supported in iOS Safari, so it is a viable option to use because of its relatively smaller file size. It is important to investigate other image file types as well and picking the one that most suits the project.  

## Heydon Pickering (Neon Tribe)
Another highlight of the event, [Heydon Pickering](http://www.heydonworks.com/) talked about quantity queries and why CSS should absolutely not feature in JavaScript if there is a way to do it in CSS.  

Heydon’s main point is that it was pointless to create CSS with JavaScript. Dynamic content needs dynamic layout, but some of the newer CSS modules allow designers and developers to create dynamic layouts using CSS alone. The abundance of grid systems used in websites is exacerbating this problem.  

He gave several demos using quantity queries to create fluid layouts with CSS alone. Some examples of what he used can be seen in his own A List Apart article [Quantity Queries for CSS](http://alistapart.com/article/quantity-queries-for-css).  

He also rebuked the idea that using Flexbox and quantity queries are hacky – they are not. If it works, why not use them? He also mentioned that there are numerous Sass mixins that will help with quantity queries (e.g. [this](http://www.sitepoint.com/using-sass-quantity-queries/)).  

## Jake Archibald (Google)
[Jake Archibald](http://jakearchibald.com/)‘s talk was titled Modern Progressive Enhancement and he talked about a few of the initiatives that they are working on to be used in Chrome.  

Putting a different spin on the previous talk, he argued that JavaScript is not optional – it is a part of the Web. Sometimes relying on JS improves UX, sometimes it doesn’t. But it is highly important to make sure that the experience is not affected massively with or without the JavaScript.  

One of the things that he strongly argued for was the unnecessary confusion between an app and a site – users don’t care! So when saying that an app will have to have JS-driven functionality (because it’s an app) is ludicrous as the user won’t see the difference – and they shouldn’t.  

Another thing he pointed out was the performance issue – the load time of a site (app, whatever) should justify the first experience users will have when the page loads. Splash screen is not an acceptable solution – decrease your load time and don’t make your users wait for your whole JavaScript libraries to load.  

He also talked about [service workers](http://www.html5rocks.com/en/tutorials/service-worker/introduction/) as a way to enable caching websites by having scripts working independently from the web pages. He also argued that sites should be offline first – he showed a demo of a new Chrome feature (behind various flags at the moment) that will allow the browser to work in its own time to load a link when the device is offline and give a notification to the user when the link is ready.  

## Ruth John
[Ruth John](http://rumyrashead.com/) talked about Web APIs.  

She voiced her dislike of the term Web API – she suggested Client Side Web API, which has a HTML5 and native influence. She then gave demos of a few of the following:  

* [Geolocation API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation), which triangulates where you are  
* [Web Animation API](https://developer.mozilla.org/en-US/docs/Web/API/Animation), which gives whole new layer of timing  
* [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/AudioNode), which is built around nodes  
* Ambient Light API, which is a JavaScript event  

## Zoe Mickley Gillenwater (Booking.com)
[Zoe Mickley Gillenwater](http://zomigi.com/) showed some use cases for [Flexbox](http://jonibologna.com/flexbox-cheatsheet/), especially for micro-layouts.  

What Flexbox does really well is taking the mathematics away from the designer and letting the computer do the calculations. So even though relative units are best guesses, they are still guesses at best. Flexbox gets closer to the ideal, because it lets us design without units.  

When working with breakpoints, she suggested using content-driven ones, rather than device-driven ones.  

## Rosie Campbell (BBC R&D)
[Rosie Campbell](https://medium.com/@RosieCampbell) talked about some of the very cool things they are working on at BBC’s Research & Development team, such as the Smart Wallpaper (part of the [Unconventional Screens](http://www.bbc.co.uk/rd/projects/unconventional-screens) project). In essence, BBC is anticipating new ways we will consume its content.  

The project came about from the question “what if you paper the walls of your home with flexible electronic wallpaper”? From this, the BBC R&D team went on to design a few prototypes of what this experience would be like.  

When designing these prototypes they made sure to let UX drive the design and not the technology.  

One of the ways Rosie suggests when coming up with a project like this is to have the following three in mind:  

* Take inspiration from sci-fi – authors and filmmakers will often have great ideas for how the supposed future societies are interacting with their environments  
* Have an ideas amnesty – no idea is too far-out or stupid. Let everyone in the team have their say, no matter how unfeasible the solution may be  
* Choose the most plausible and engaging to move forward  

She also points out that having constraints could breed creativity as it forces the designers and developers to come up with more innovative solutions.  

When it comes to responsive design it is important to stay device agnostic. For example, grids are good but not all screens are going to be rectangular. There will be circular, triangular, or other polygonal shapes. In the case of the Smart Wallpaper, there will be uneven surfaces, angled ceilings, furniture blocking the screen etc.  

## Lyza Danger Gardner (Cloud Four)
[Lyza Danger Gardner](http://www.lyza.com/) (yes, that is her real name) gave, what I reckon was, the best talk of the day. Her talk was around how difficult it is to be a generalist these days and what it takes to be a very good one.  

She began by telling her story of how she got to be a web generalist and how what she and her peers were waiting to happen is happening now. However, now it feels there are too many options. It is now too difficult to get from point A to point B without having to master a whole new technology.  

She likened a generalist to a librarian, curating an insane amount of information and turning it into something meaningful. There is a maelstorm of information and everchange has become the status quo.  

She thinks being a generalist now means having an incomplete mastery of everything, when in fact it should be achieved by reintroducing constraints and having a better understanding of these constraints.  

She finished her talk by saying that web is a set of constraints and we’re building bridges between them.  

## Aaron Gustafson (Microsoft)
The event finished with another inspiring talk, this time from [Aaron Gustafson](http://www.aaron-gustafson.com/), about the future of responsive design.  

He posited an interesting argument for responsive design that we should consider users when it comes to progressive enhancement. All of the design concerns (e.g. colours, language, size …) these are all accessibility concerns. So the future of progressive enhancement (and responsive design) firmly lies with accessibility.  

It is up to designers and developers to design for everyone regardless of disability, gender, race etc. “Our work is meaningless without users”.  

He also touched upon a few new developments in browser technologies and what he sees to be the future of interaction – voice.  

Responsive Day Out was another great event and I’m really happy to have attended this year too. I hope the above gave at least some semblance of what was discussed during the day.  

