# Sprint Challenge: Advanced CSS - Space Walkers Web Page

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in a concrete project. This Sprint explored advanced CSS techniques using Responsive Design and Preprocessing. During this Sprint, you studied how to use the viewport meta tag, media queries, setting up a preprocessor, and advanced use of preprocessing techniques. In your challenge this week, you will demonstrate proficiency by updating a website that is missing content as well as adding mobile styling.

## Instructions

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the Sprint Challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your PM and Instructor in your cohort help channel on Slack. Your work reflects your proficiency in advanced css and your command of the concepts and techniques in responsive web design and preprocessing.

You have three hours to complete this challenge. Plan your time accordingly.

## Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your project manager.

## Description

The client for this challenge is _Spacewalkers Magazine_. Spacewalkers needs your help to build a small proof of concept website for their marketing team. They have provided designs for both desktop and phone views. In addition to designs and content they have most of the home page coded for you. You just need to finish the navigation and header as well as the mobile styles.

In meeting the minimum viable product (MVP) specifications listed below, your web page should look like the solution design files of the desktop and mobile views:

[Click here to review the home design](design-files/home-desktop.png)

[Click here to review the mobile design](design-files/home-mobile.png)

## Self-Study Questions

Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read by your project manager

1. What is the difference between an adaptive website and a fully responsive website?

	Adaptive Design: Adaptive design use's pre-selected HTML for different devices, the web server will decide this based on the device making the HTTP request. Information displayted is pre-selected and only specific device based information is shown to the user. Multiple pages/templates must be made for different types of devices

	Responsive Design: User devices are detected by the use of media queries. Page content is sized and reorganized accordingly for each type of device. All content is loaded to the devices browser wether it is visable to the user or not, and lastly there is only one page / template that gets made that all devices will use.



2. Describe what it means to be mobile first vs desktop first.

	Desktop First Design: Desktop design means you will be writting code for a desktop device first. You will shrink layout and hide content as needed when you begin to LOSE screen realestate moving to tablets and other mobile devices. Your genral styling will be aimed at desktops. Media queries will often use the `max-width` propety to discover the screen size of a device.

	Mobile Design: A mobile design works in the opposite direction. You will write code with a mobile layout first, you will begin to expand your layout and show more content as you gain MORE screen relestate. Your genral styling will be aimed at mobile devices. Media queries will often use the `min-width` property to discover the screen size of a device.

3. What does `font-size: 62.5%` in the `html` tag do for us when using `rem` units?

	When setting the `html` tag to a `font-size: 62.5%` you are setting it to 10px but with using a responsive unit. When you use the `rem` unit you access the `root element` aka the `html` tag which holds a font size of `62.5%` which is `10px` in a % form. So if you say `font-size: 1rem` you are setting the font size to 10px in a % form, if you were to set `font-size: 3rem;` that would be 30px in % form bc our bas is 10px multiplied by 3 which gives us 30px.

4. How would you describe preprocessing to someone new to CSS?

	Preprocessing allows us to write code in a more reusable,scaleable,and readable way. 
	
	If using less you will use NodeJS with a less compiler to compile your code from less down to CSS for the browser to use. You no longer will be writting in a CSS file but in a LESS file. 
	
	Our code becomes more readable bc the nesting follows the same flow as your HTML, Code is more scalable bc we have access to LESS variables which can hold a single value such as a color, font family or even a unit such as %, em, rem, vh, and vw. 
	
	We also have mixins and parametric mixins. These are sets of CSS properties and values, this gives us the power to write many styles in one place and apply them where we see fit. However parametric mixins do not have predetermined values you must provide the value to be assigned to a property. 

	Lastly there is escaping. This can be used to predifne media query break points and applied every where in your code, and if there is a change in device width break points you only have to change the escaped value and it will affect in every spot you are using that specific escaped break point.
	
	All of this makes code more scaleable and manageable bc we now have reuseable pieces of code that we change in one line and affect many lines with. 

5. What is your favorite concept in preprocessing? What is the concept that gives you the most trouble?

	My favortie part of preprocessing is mixins. And the concept that gives me the most trouble is learning when to create and use a parametric mixin.

You are expected to be able to answer all these questions. Your responses contribute to your Sprint Challenge grade. Skipping this section *will* prevent you from passing this challenge.

## Project Set Up

Follow these steps to set up your project:

### Git Set up

- [ ] Create a forked copy of this project.
- [ ] Add your project manager as collaborator on Github.
- [ ] Clone your OWN version of the repository (Not Lambda's by mistake!).
- [ ] Create a new branch: git checkout -b `<firstName-lastName>`.
- [ ] Implement the project on your newly created `<firstName-lastName>` branch, committing changes regularly.
- [ ] Push commits: git push origin `<firstName-lastName>`.
 
Follow these steps for completing your project.

- [ ] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's  Repo). **Please don't merge your own pull request**
- [ ] Add your project manager as a reviewer on the pull-request
- [ ] Your project manager will count the project as complete by merging the branch back into master.
 

### Preprocessor Set up

* [ ] Verify that you have LESS installed correctly by running `lessc -v` in your terminal, if you don't get a version message back, reach out to your project manager for help.
* [ ] Open your terminal and navigate to your preprocessing project by using the `cd` command
* [ ] Once in your project's root folder, run the following command `less-watch-compiler less css index.less`
* [ ] Verify your compiler is working correctly by changing the `background-color` on the `html` selector to `red` in your `index.less` file.
* [ ] Once you see the red screen, you can delete that style and you're ready to start on the next task

## Minimum Viable Product

Your finished project must include all of the following requirements:

### Import LESS Files

* [ ] Navigate to your `index.less` file. Notice the file is blank. You have been asked to use a certain import order. That order is as follows:

```markdown
1.variables.less
2.mixins.less
3.reset.less
4.global.less
5.navigation.less
6.footer.less
7.home-page.less
```

_You will know everything is working properly when you see the styles enabled for the provided content._  

### Home Page - Desktop HTML & LESS

* [ ] Take 10 minutes to review the code that has already been provided for you. Take time to see how the home page was built.

* [ ] Add a viewport meta tag to the head of your index.html page

* [ ] [Review the provided home desktop design file](design-files/home-desktop.png). You are to build the missing navigation system and header image. You have been provided all content necessary in the [index.html file](index.html)

* [ ] Navigation Styles: Use the `navigation.less` file for styling.

* [ ] Main Content Styles: Use the `home-page.less` file for styling

* [ ] LESS Mixins: Create and use 2 different mixins to aid your styling. Use the `mixins.less` file for your mixins

* [ ] LESS Parametric Mixin: create a parametric mixin that is used to create the `sign up` button styles.

* [ ]  Use at least 2 parameters to create your button

* [ ] Create a hover state that swaps the background color and font color of the base button styles.

### Mobile Design

* [ ] Create a `@phone` variable that contains a `max-width: 500px` media query string. Use the `@phone` variable for all your nested mobile styling.

* [ ] [Review the provided home mobile design file](design-files/home-mobile.png). Match your mobile styling the best you can using the design file.

* [ ] Push your changes and create a pull request if you haven't already.

In your solution, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

## Stretch Problems

After finishing your required elements, you can push your work further. These goals may or may not be things you have learned in this module but they build on the material you just studied. Time allowing, stretch your limits and see if you can deliver on the following optional goals:

* [ ] Build a page of your choosing from the navigation items. Come up with content and images that fit the theme.

* [ ] Introduce CSS animations to your site.

* [ ] Create a fixed navigation and add some opacity to the background

* [ ] Create a form that would allow someone to sign up for a Spacewalkers Magazine subscription