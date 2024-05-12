# wk01-assignment

This website has been made for an education assignment:
Week 01: Build out the website.

# Assignment Reflection
As far as meeting requirements is considered, I feel like I've covered most of the basics:
- I have a navigation in the `<header>` tag, all page contents are in the `<body>`, and a `<footer>` which has the things I think I would expect to see, such as the page's copyright. I feel confident that I know where to place these particular parts of HTML code. Having said that, I have some questions about other elements that I made for this website, but haven't been covered in the course. Where within the document structure is it best practice for a fixed "back to top" button to be placed? I ended up placing it in the header, just below the `<nav>`, since it sort-of-is a navigation button of some kind.
- I feel pretty confident about flexbox. Most of the content in the page I put in a flexbox for one reason or another. I made the `.title` contents of each section set to `flex-direction: column;` to quickly and easily apply consistent spacing between each block - giving the appearance of each block being on a new line. I also had a try with different flexbox styles for the navigation bar. I wanted the navbar to appear as a single row that was aligned to the left of the page on a larger viewport, such as a desktop computer, but change so that the logo & title would appear above the navigation links on a smaller viewport, which required `flex-wrap: wrap`. I used `@media` to give it two different styles that it would dynamically change between, depending on the viewport size.
- I used CSS positioning to add an extra element to the webpage that made sense to be `position:fixed` so that the user can always have access to the function of the button - specifically a back to top button that appears in the bottom-right corner. 

Initially, I ran into an issue when doing part of the assignment "Absolute positioning the titles". Inside the element `<section class="feature">`, the prompt wanted us to make the child element `<div class="title">` with the property `position:absolute`, which the prompt describes as working relative to its parent tag. However, it did not work straightforwardly in this way. The parent requires `position` to be set in the stylesheet, otherwise any child element with `position:absolute` will position relative to the `<body>` tag instead, which is what initially happened while I was following the instructions. When I gave the parent the property `position: relative` in the CSS document, `position:absolute` started working on child elements under it - specifically on `<div class="title">`.

As for general choices I made when designing the website, I've outlined them below:

## Aesthetic choices
- I added a division between each section that's just a solid colour so that the photographic background images appeared to have a divider between them.

I made some aesthetic choices that I think have a functional purpose in improving legibility of text content on the website. I think these worked out quite well:
- Added borders around some text.
- Low opacity (low alpha) gradients in certain places to make text on the webpage more legible against other parts of the webpage.
    - On `index.html` - there is a gradient over the background images of each section to make the text & contents more legible. There are a couple of different gradients in use depending on the section - a couple of the sections have stronger gradients to improve text legibility because the photographs behind them have more details/are more visually chaotic.
    - The navigation bar against the page itself, so that it would appear clearly "above" all other content on the webpage. I had to use `z-index:` to specify the order of the navigation menu against the gradient, with the gradient placed behind.
- Links change colour when highlighted. I think showing the user visual feedback when navigating the website is helpful to demarcate that something is interactive or clickable.

## Problem solving
I used `@media` to change the display style of several elements to better fit smaller viewports:
- I wanted to restrict the display `width` of all items within the `.title` class (the text & links on each feature section on `index.html`) mainly for aesthetic reasons, since keeping everything in a box to one side meant the text didn't overlap as much of its background image. After doing this, viewing the site in my browser, and then testing its display functionality by playing around with the browser window size (I also downloaded an add-on for my browser that simulates mobile phone display), I saw the width of that section would remain fixed and appear partially off-screen on smaller displays that have a smaller relative width than specified in the stylesheet. Due to this, I used `@media` to control it to dynamically change width depending on the viewport size. I did this on other elements with a fixed width as well.

- Longer amounts of content in the `.title` class could push everything outside of the bounds of the section itself - especially likely if the display size was smaller. I also used `@media` so that the position would move upwards in relation to the section so that this would not happen.

- Changing style of the navigation when the display size becomes smaller, so that it would appear with the logo & title above the navigation links. To do this, I had it change the style to `flex-wrap: wrap;`. It fits smaller displays better this way. The different style is mainly an aesthetic choice.

I mostly applied `@media` based upon trial and error. For future projects, I would like to know more about best practices for using `@media` when coding & designing a website. I would very much appreciate feedback on how to use this feature more effectively.

## Some things I added
- Added `scroll-behavior: smooth;` to `html` so that there's a smooth animation when navigating & scrolling between sections.




# Attributions
Fonts (via Google Fonts):
- Poetsen One (Designed by Rodrigo Fuenzalida, Pablo Impallari)
    https://fonts.google.com/specimen/Poetsen+One


Image sources:
- https://unsplash.com/photos/mt-fuji-n--CMLApjfI
- https://unsplash.com/photos/canal-between-cherry-blossom-trees-8sOZJ8JF0S8
- https://unsplash.com/photos/people-gathered-outside-buildings-and-vehicles-alY6_OpdwRQ
- https://unsplash.com/photos/silhouette-of-man-near-outside-qwPSnBvdhtI
- https://unsplash.com/photos/gray-pathway-between-red-and-black-wooden-pillar-NYyCqdBOKwc
- https://unsplash.com/photos/cooked-food-PRM1RuIIQvI
- https://unsplash.com/photos/a-woman-sitting-at-a-table-looking-out-a-window-juL6u-b3naA
- https://unsplash.com/photos/brown-wooden-table-near-window-58ApUELd3Ec
- https://unsplash.com/photos/a-large-building-with-a-fountain-in-front-of-it-T6Hist3MRO4


Self-made graphics:
- ./images/arrow.png
- ./images/japan-logo.png