#Journal Entries 

####Jan 13. 2022
##### Portfolio Project Status Update
For the past few days were significant improvement on my personal portfoilo project. I have worked hard to include extra cool features. 

Here are some cool things I've learned in the procress: 

- **Security Concerns and how to deal with them**


 This project has allowed me to realize how important security is when developing full stack applications. 


 I have learned that whenever I use anchor links to external websites, I should always attach a `rel="noreferrer"` or `rel="noopener"`. This prevents the new page from accessing the `window.opener` property.


- **Basic Web Accessibility Resources**


	After experimenting with different colours for my portfolio, it was brought to my attention that using the funkiest colours isn't always the best idea.

	Looking more into it, contrast between foreground text and background text is more important than I thought. Using the [webAIM](https://webaim.org/resources/contrastchecker/) resource, It was possible to check which colours contrasted well. Consquently, I was able to apply this knowledge to my personal project!

- **Scroll Animations**
	Wanting to impress my buddies with my brand new website, I wanted to include some cool animations. One practical way I included animations was the anchor link scroll.
	
	Instead of having the page directly snap to the anchored link, a smooth transition would be preferable. After some reading and researched, I settled for [Chris Coyier's jQuery script](https://css-tricks.com/snippets/jquery/smooth-scrolling/#aa-smooth-scroll-with-jquery). Here is the script after some editing from me: 
	
	```
	// Select all links with hashes
$('a[href*="#"]')

  .click(function(event) {
    // On-page links
    if (
      location.pathname.replace(/^\//, '') == this.pathname.replace(/^\//, '') 
      && 
      location.hostname == this.hostname
    ) {
      // Figure out element to scroll to
      var target = $(this.hash);
      target = target.length ? target : $('[name=' + this.hash.slice(1) + ']');
      // Does a scroll target exist?
      if (target.length) {
        // Only prevent default if animation is actually gonna happen
        event.preventDefault();
        $('html, body').animate({
          scrollTop: target.offset().top
        }, 1000, function() {
          // Callback after animation
          // Must change focus!
          var $target = $(target);
          $target.focus();
          if ($target.is(":focus")) { // Checking if the target was focused
            return false;
          } else {
            $target.focus(); // Set focus again
          };
        });
      }
    }
  });
  ```






####Jan 8. 2022 
##### Learned about Markdown!
- Learned how to use Markdown files (.md)
- Redid journal on MacDown which is a Markdown editor

##### Reviewed JavaScript on freeCodeCamp.org
Today I decided that I wanted to revise my skills in JavaScript, more specifically the latest ES6 version. I have never learned too much of the latest features but I am glad I reviewed. 

I learned how useful arrow functions are and will start implementing them in my code right away. I realized that most functions I used were never used more than once. Arrow functions solves that problem and simplifies my code.

```
var myConcatArray = function(arr1, arr2) {
  return arr1.concat(arr2);
};

```
Turns into 

```
const myConcatArray = (arr1, arr2) => arr1.concat(arr2);

```
Very useful!

####Jan 7. 2022
 - Reviewed Linux System Administration course, learned about system and process monitoring tools such as 'top and 'ps'.

- Brain stormed some ideas on a discord bot. Debated between using Discord.js and  Discord.py. 

- I decided to use Discord.js so I can sharpen my JavaScript skills. Since discord.js uses Node.js, I had to read I read up on Node.js. Was a little confusing but after watching a YouTube video, the pieces start to fall together. 







