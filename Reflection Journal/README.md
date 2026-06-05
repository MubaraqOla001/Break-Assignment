# Class One Web Ecosystem
## Theory
1. 

2. firstly, when users use browser they are either in request of an information or making a post, so to solve this browser send an http request to relevant data, however this http cannot move on its own it requires a kind of transit that transport the data or request to server and bring back http response in form of html, css and javascript to the browser, and this transit used to be **TCP, But it has a problem of being slow** considering the fact that the data move using a single path and if one information at the fore front is not ready but the one behind it, is ready it has to wait until the one at the begining ready before it can propel, this cause web page to stall and delay, **QUIC replaced the TCP just to solve that problem of stalling by providing multiple path for data to travel** and if one data is not ready it will not stop the other data from delivering and with that website is now fast.

3. 

## Product Thinking
1. Semantic html elements can help the blog to be more accessible and increase the  SEO(Seach Engine Optimization) which in turn solve the problem of drawing more traffic to the blog because the sematic elements gives meaning to the contents they contain and help the browser understand the structure of the blog, and rate it higher in SEO and moreover, that is the fundamental meaning of the **Markup** in html using tag to mark or provide meaning to the contents they contain.

2. Early before now, cloud computing is used instead of edge computing, it used to work perfectly, as I read but then there is issue of sluggish movement imagine two friends playing a soccer game on the internet and they are located in different part of the world before player ball can reach the other players it has to travel miles before the ball can be pass, so edge computing solve that problem by providing a mini brain(edge) scattered in many location to provide fast internet connection instead of providing the large brain(cloud) located in strategic pattern of the world. **fast game because the data does not have to travel miles before it can be delivered**

## Engineering Best Practice
**My response to the Junior developer:** Yeah, you are correct it works fine visually and you have really done well but then there are several issues with what you have created;
firsty,  HTML is called a markup language for a reason, and that is using tags to give meaning to the contents it contains, it is not just to display content on browser, you giving that kind of divs containing html to browser is just like you giving browser a bunch of unstructured sentences so it will not understand what the page is all about which result in rating the page low on SEO and slow to access ACCESSIBLILY. div is just a generic container and it is normally used when there is no suitable semantic element for a data even at that level you have to use aria-label to tell what the the div is actually about.

secondly, you should not just write code for yourself let other developers even layman see your code and they should be able to understand, let them fall in love with your code in terms of structuring so they can know where to start and what you have done incase you are working on a collaborative project you don't want to make life hard for them right? and even for yourself provide a clear pattern for yourself incase there is a bug in your code if it contains divs it might be hard to trace so solve the problem of **CODE MAINTAINABILITY AND HELP OTHER DEVELOPERS COLLABORATE WITH YOU ON YOUR WORK**.

# Class Two Typography and Information Hierarchy

## Theory
1. `<em>` is a semantic html element that gives the meaning of emphasize the element it contains. And emphsizing means the contents carry more weight compared to other contents on the page. whereas `<i>` is also a semantic html element that italicize the contents it contains so that it can looks different visually from the rest of the document on the page.

I will use `<em>` to lay emphasis on a content and `<i>` to show that the content is different from the rest of the content may be in language.for example `<p>It is fun to learn but <em>consistency matters</em> even though <i>Que sera, sera</i></p>`

2. Screen readers treat `<em>` by changing voice and stressing over contents inside this tag to lay emphasis to the user because a visually impaired person will not see the visual look of the text.
Also, `<a>` anchor tags are treated differently so that the user can know that the content in this tag lead you to another destination and take you out of this document flow.
And lastly, `<h1> to <h6>`  are treated differently so that the user can scan through the page because this represent how the page is structured by giving hierarchy to the contents those heading contains and help the user decide whether they want to read the section under the heading or jump to another heading of the page.

3. I will use aria-label when a button tag contain an image or logo that the user can click in or an anchor tag that has its content as an image where there is no descriptive text to tell what the link is about. example `<a aria-label="A link leading to X page">X icon</a>`


## Accessibility Reflection

1. 
## Product Thinking

1. To help developers scan the technical documentation page quickly, I will use different h tag to structure the page in the following manner:
<h1>Introduction to the page</h1>
<p>This heading used h1 element to introduce the page and it is the main heading of the page and no other h1 will be used through the page as other headings will be sub heading to this</p>
<h2>The universal API link</h2>
<p>This contains the link to the whole contents developer might need through out the page. mind you h2 can be more than one on a page not like h1</p>

<h3>Specific API</h3>
<p>This contain some specific API links under the universal API link</p>

# Class Three Modern Assets & Linking