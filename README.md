# DOM II - Event Exploration

Fun Bus wants you to make their site more interactive. They are relying on you to provide 10 unique events to enhance their site. Explore the many events available to you by using the [MDN events reference](https://developer.mozilla.org/en-US/docs/Web/Events).

## Instructions

### Task 1: Project Set Up

#### Set Up The Project With Git

**Follow these steps to set up and work on your project:**

* [x] Create a forked copy of this project.
* [x] Clone your OWN version of the repository (Not Lambda's by mistake!).
* [x] Create a new branch: git checkout -b `<firstName-lastName>`.
* [ ] Implement the project on your newly created `<firstName-lastName>` branch, committing changes regularly.
* [ ] Push commits: git push origin `<firstName-lastName>`.

#### Launch the project with npm

* [x] Navigate to the root of the project with your command line.
* [x] Run `npm install` to download any dependencies listed in the `package.json` file.
* [x] Run `npm start` to compile your project and launch a development server.
* [x] Navigate Chrome to the URL indicated in the output of the `npm start` command.

### Task 2: Create listeners for 10 types of events

* [x] Using your [index.js file](js/index.js), create [event listeners](https://developer.mozilla.org/en-US/docs/Web/Events) of at least 10 _different_ types. You must Use your creativity to make the Fun Bus site more interactive. For example you could change colors, animate objects, remove objects, etc. Here are some event types you could try to use:
  * `mouseover`
  * `keydown`
  * `wheel`
  * `load`
  * `focus`
  * `resize`
  * `scroll`
  * `select`
  * `dblclick`
  * `drag / drop`

Note: Drag and drop is a bit more advanced than the others: it's not actually a single type of event but several types that need to work together.

* [ ] Nest two similar events somewhere in the site and prevent the event propagation properly. Remember not all event types bubble.
* [ ] Stop the navigation items from refreshing the page by using `preventDefault()`

### Task 3: Stretch

* [ ] Go look at [GSAP](https://greensock.com/) and implement the animations found in that library with your custom events.

#### Stretch assignment

* [ ] Take a look at the [stretch assignment](stretch-assignment) and follow the instructions in the read me file.

## Submission Format

**Follow these steps for completing your project.**

* [ ] Submit a Pull-Request to merge `<firstName-lastName>` Branch into `main` (student's  Repo). **Please don't merge your own pull request**

const navContainer = document.querySelector(".nav-container");
navContainer.addEventListener("mouseover", (event) =>{
  navContainer.style.backgroundColor = "pink";
});

const nav = document.querySelector(".nav");
nav.addEventListener("mouseup", (event) =>{
  nav.style.backgroundColor = "yellow";
});

const navLink = document.querySelector(".nav-link");
navLink.addEventListener("click", (event) => {
  navLink.style.Color = "blue";
  event.stopPropogation();
  event.preventDefault();
});

const textContent = document.querySelector(".text-content");
textContent.addEventListener("click" (event) =>{
  textContent.style.color = "blue"
});

const button = document.querySelector(".btn");
button.addEventListener("onfocus" (event) =>{
  button.style.backgroundColor = "red"
});

const contentDestination = document.querySelector(".content-destination");
contentDestination.addEventListener("mouseover" (event) =>{
  contentDestination.style.fontSize = "x-large"
});

const contentSection = document.querySelector(".content-section");
contentSection.addEventListener("dblclick",(event) =>{
  contentSection.style.borderStyle = "solid";
  contentSection.style.borderColor = "red blue green"; 
});

const imgContent = document.querySelector(".img-content");
imgContent.addEventListener("mousedown",(event) =>{
  imgContent.alert("Travel Anywhere!");
});

const contentPick = document.querySelector(".content-pick");
contentPick.addEventListener("mouseup",(event) =>{
  contentPick.style.color = "red";
});

const destination = document.querySelector(".destination");
destination.addEventListener("click", (event) =>{
destination.style.color = "blue";
});


