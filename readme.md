# My over-engineerd personal domain landing page
A wise man once told me to "always register your personal domain name as long as it is available." So, I did.

While I had no clear purpose for the domain, I did not want it to show the default domain registrar landing page. As an international graduate student and cloud freak I:

 - wanted a minimal, good looking and mobile friendly page with my personal details without spending much time on design
 - did not want to pay a premium for the .com domain registration
 - did not want to pay anything on webhosting
 - wanted the website to load fast all over the world (with good GTmetrix and Google PageSpeed Insights scores)
 - wanted to be able to edit the website easily and quickly from any device with automatic versioning

How did succeed?

## Clean, mobile friendly website with minimal design efforts
I found the [bootstrap framework](https://getbootstrap.com/) most suitable for this job, created an index.html file in VScode and linked the bootstrap stylesheet in the header of my page.

## Don't pay a premium for a domain registration
[Cloudflare](https://cloudflare.com) offers domain name registration at great value. They claim "You pay what we pay — you won’t find better value." and I tend to believe them. At the time of writing, registering a .com domain at Cloudflare sets you back $8.57 a year.

## Don't pay anything for webhosting
The awesomeness of Cloudflare doesn't stop at premium-free domain registration. Cloudflare offers a service called [Cloudflare Pages](https://pages.cloudflare.com/), a JAMstack platform for frontend developers to collaborate and deploy websites. And for a simple, single landing page like mine, it's totally [free](https://developers.cloudflare.com/pages/platform/limits/).

## Make the website load fast, all over the world
The fact that you can simply use the bootstrap framework for free by including a single line of code in your HTML file is great. And you can make it load faster by using a [faster CDN](https://www.belugacdn.com/best-cdn-for-bootstrap/). But even by selecting the fastest Bootstrap CDN, a lot of unnecessary CSS code is loaded since I use only a fraction of it for my simple design. 

### Purify (minimize) CSS
I used the [PurifyCSS](https://purifycss.online/) optimization tool to scan my HTML & JS source code and remove the unused CSS selectors. This shrank the size of my CSS with 90%. I downloaded the style.css file and added it to my respository which, in addition, decreased the amount of external requests.

### Minimize Google Analytics

### Global CDN
Another awesome thing about Cloudflare Pages is that it automatically deploys the website over the Cloudflare CDN network, so the page is distributed over hunderds of servers around the world closest to its visitors.

## Edit the website easily, anywhere with automatic versioning
By pushing my files to GitHub, I can access and edit the code directly using the [online file editor](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files).

## What about the e-mailaddress
Per e-mail I received a question about the @pimkamphuis.com e-mailaddress that is shown in the website: "Do you also use an e-mail service for free?" 
