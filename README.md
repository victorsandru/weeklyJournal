# Journal Entries

## May 10. 2022

#### End of school year update

Hello again! It's been a while. My second semester was not very kind and it showered me with work. Nothing I couldn't handle though, I accomplished my goal of being on the Dean's Honour List! I worked very hard for this achievement and I am looking forward to more to come.

I have learned a lot this semester, and I am very excited to share these new findings with you!

- **Java**

	At the end of the previous semester, I was introduced to Python Object Oriented Programming (OOP). It was quite difficult to understand until I worked with Java. 
	
	Java is a high-level object-oriented programming language. Unlike Python, you must follow OOP principles to fully utilize Java. I learned about the beauty of OOP and how simple it makes organizing your thoughts and files.
		
	I do have a love/hate relationship with Java. On some days I feel on top of the world with this language, convinced that I could create anything. On other days I am convinced that Java is the worst language created.

- **Python Tutoring**
	
	Sometime in the middle of my semester, one of my buddies approached me to ask for help with his assignment. I happily helped, and realized that it was also very rewarding for me to help others out with something that I am passionate about.
	
	He recommended me to a bunch of his other friends, and now I have a few students that I meet with weekly to just talk about Python, and computer science fundamentals. The best part of all this is that I learn new things from my students! They have a different perspective on coding since they are still new. 

#### Future plans and updates
- Work with colleagues from the Carleton Computer Science Society on a full stack project
- Continue my shadowing of a DevOps Engineer
- Create a curriculum for my Tutoring gig

* * *

## Jan 22. 2022

#### Portfoilo is launched!
You can check out my website at [victorsandru.com](https://victorsandru.com)

Here are some things I learned along the way: 

- **Web Hosting**
	
	After pushing my final commit, I realized I had to start looking into web hosting services. First I tried Google Cloud Platform. I was amazed by the amount of possiblites I can do with GCP. 
	
	I played around and started a cloud VM and connected it with SSH. Afterwards, I installed Docker and launched a container with Alpine in it. To recap, I performing commands in Alpine which is in a Docker container, which is installed on the cloud. All this from my **own** command terminal. That's awesome.
	
	Anyways, the issue with using GCP with web hosting was that I had to use a third-party to obtain a SSL certificate. So I looked to Firebase. Firebase is equally awesome. Probably the coolest thing I've ever done on a project was using Firebase.
	
	Here's what I was trying to solve: the tedious and time sink of updating your local files for your application and then having to upload them to your web hosting. With firebase it was possible to deploy to live via GitHub pull requests. Isn't that awesome?!

#### Future plans and updates
- Update my portfolio from Bootstrap and basic HTML to React
- Discord bot that can access Riot Games' API library and sort through the data
- Create a blog using React


* * *

## Jan 13. 2022

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
	/ Select all links with hashes
	$('a[href*="#"]')

	  .click(function(event) {
	    / On-page links
	    if (
	      location.pathname.replace(/^\//, '') == this.pathname.replace(/^\//, '') 
	      && 
	      location.hostname == this.hostname
	    ) {
	      / Figure out element to scroll to
	      var target = $(this.hash);
	      target = target.length ? target : $('[name=' + this.hash.slice(1) + ']');
	      / Does a scroll target exist?
	      if (target.length) {
		/ Only prevent default if animation is actually gonna happen
		event.preventDefault();
		$('html, body').animate({
		  scrollTop: target.offset().top
		}, 1000, function() {
		  / Callback after animation
		  / Must change focus!
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





* * *

<h4>Jan 8. 2022</h4>

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

* * *

<h4>Jan 7. 2022</h4>
 - Reviewed Linux System Administration course, learned about system and process monitoring tools such as 'top and 'ps'.

- Brain stormed some ideas on a discord bot. Debated between using Discord.js and  Discord.py. 

- I decided to use Discord.js so I can sharpen my JavaScript skills. Since discord.js uses Node.js, I had to read I read up on Node.js. Was a little confusing but after watching a YouTube video, the pieces start to fall together. 







