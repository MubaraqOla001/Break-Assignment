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
## Theory
1. Firstly, an hero image must be an image of high quality and relatively big in size(visually) to catch the viewer attention as soon as they get in page but then before they get into the page if the image size is much(large mb) it will take a while to load giving the page to even be ranked low in SEO. To solve this problem I will make use of a website called **Squoosh** to reduce the the size from 5mb to a reasonable size like kb and still retail the quality of the image. and the steps I will take include;
paste the image into the squoosh and resize it and convert it from PNG to **AVIF and WEBP** reason for choosing this format is because WEBP have a considerably reduced size and high quality and support by all browsers but then AVIF reduce size of an image even better than WEBP but doesn't get support like webp across browsers but then it supported among major browsers. so I will use the two together serving the format of Avif first then if the browser does not support that then it can make use of the webp, by using the html tag 
``<picture><source srcset="img.avif"></source><source srcset="img.webp"></source></picture>.``

2. Just like I used it in the scenario above, that is just what srcset is meant for it is an attribute used inside img or source to provide different formats and sizes for different screensize and give the device of choosing the format and best size that suits it making the web a resposive layout.

3. when using target="_blank" this allow the link to open the destination of the link in another window, now considering you providing link to another website, that means when the user of your website click the link they move from your website to another website opening in another tab, without rel="noopener" your website is under security risk. In a simple term imagine a door located in a crowd environment but open to a private room, and you come out of the secret room leaving it wide open this gives room for the crowd to enter into the supposed to be secret room without any hindrance, now use this analogy your website is a secret room and the links that link to other websites from website is the door, the the rel="noopener" is the padlock to your secret room, without the padlock everyone has access to your secret room your website so with that potential can hack into your website and get user information that might have been given to your website because of the trust your website has earned from them and the hacker may now have access to their information.

## Engineering Thinking
1. 
Displaying 50 product images on a page is a lot that can slow down the website and allow user to download large size of images my optimization strategy will be:

a. I will set the loading of the images to lazy so that not all images load all at once but load once the user scroll to them but the first grid row containing upto 5 or 6 elements depending on the grid, will have loading of eager and fetchpriority of high so they load on first entering into the page.

b. I will set the format to avif and have webp as the fallback, my choice of avif format is because it reduce the file size better than anyother available format, and my choice of webp is because it is 100% supported by browsers so if a browser does not support avif it will support webp, and this will make the rendering of the web page fast because small size is rendered fast.

c. I will use CDN content delivery network to store my images instead of the user accessing the image from the local storage if it is placed on CDN then it can be easily accessible using the principle of edge computing as explained earlier.

d. I will also make my image to be availabe in different dimension to fit different screen size so that a mobile phone user with only 300px phone width will not download and image of 2000width I can use the website called cloudinary to do this.
considering all these four approaches the website should be accessible and let the user have best experience visiting such web page.

## Class Four Modern Forms and User Experience
# Theory

# Product Thinking

# Engineering Best Practise

## Class Five The CSS Engine - Box Model and Specificity
# Theory

# Engineering Best Practise