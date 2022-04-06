# Media Queries

This app demonstrates how to use media queries in CSS files. 

Fork and clone this repo to consult the files as you read the README. I'll be referring to `live-demo.html` and `live-demo.css` throughout the README. Open `live-demo.html` in your browser and consult it and `live-demo.css` while reading through the README. Complete the mini-assignment at the end of the README using the files in the "practice" folder. `index.html` and `index.css` serve as a slightly more advanced example of media queries that you can consult.

## About Media Queries

Media queries are an essential tool for building responsive websites, especially "Mobile First" websites. Including media queries in your CSS allows you to change the layout of your webpage based upon the screen size of the device on which its being viewed. For example, we'll probably want a different layout for mobile phone users than desktop users.

Media queries are included in your CSS file starting with the `@media` tag. You will then specify the type of media you want to query - `screen`, `print`, or `speech`. `screen` refers to devices with screens - mobiles, laptops, desktops, etc. `print` refers to print previews and print devices. `speech` refers to text-to-speech devices. So if you wanted to target screens, you would write `@media screen`. To select all device types, you can write `@media all` or simply `@media`.

After selecting your screen type, you'll specifiy a condition that must be met in order for the styles you've defined within your media query to apply to your webpage. Oftentimes, this condition relates to screen width - we want to rearrange our layout depending on how wide the screen is. A query for a minimum screen-width of `500px` would look something like this `@media (min-width: 500px) {}` (styling attributes would go within the curly braces). Let's imagine that we have an h1 tag with an id of "header" whose font color we want to change to yellow when the screen width exceeds 500px. We would write the following in our CSS file:

`@media (min-width: 500px){
    #header {
        color: hsl(60, 90%, 60%);
    }
}`

## Mini-assignment

In the folder labelled "practice" you'll find two files - practice.html and practice.css. You will be working in practice.css. This will test your knowledge of Media Queries, CSS grid, and general CSS (you might have to do some googling).

#### Deliverables

<ol>
    <li>Set the following default styles:
        <ul>
            <li>Body
                <ul>
                    <li>a margin of 0</li>
                    <li>a grid layout with a row for a header and a row for a main display.</li>
                </ul>
            </li>
            <li>The div with the id 'header'
                <ul>
                    <li>It will occupy the first row of its parent container's grid.</li>
                    <li>You will give a background color of your choise using hsl, rgb, or hex colors.</li>
                    <li>All items in this div should be centered vertically (hint: what else will this div need to make that happen?)</li>
                </ul>
            </li>
            <li>The h1 element that is a child of 'header'
                <ul>
                    <li>Should be centered horizontally in its parent container.</li>
                </ul>
            </li>
            <li>The div with the id 'main'
                <ul>
                    <li>It will occupy the second row of its parent container's grid</li>
                    <li>It will have a grid layout with one column that spans the width of the screen.</li>
                </ul>
            </li>
            <li> The div with id 'sidebar'
                <ul>
                    <li>will not be visible (hint: how do you make sure that an element is not displayed?)</li>
                </ul>
            </li>
            <li>The div with the id 'content'
                <ul>
                    <li>It will occupy the single column of its parent container</li>
                </ul>
            </li>
            <li>The div with the id 'ad-bar'
                <ul>
                    <li>will not be visible</li>
                </ul>
            </li>
        </ul>
    </li>
    <li>When the screen width is greater than 600px, the following styles should be implemented
        <ul>
            <li>'main' div
                <ul>
                       <li>will have two columns - one on the right hand side that is 200px, one on the lefthand side that is 100% of the viewport width minus 200px (hint: you may need <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/calc">this</a>)</li>
                </ul>
            </li>
            <li>'sidebar' div
                <ul>
                    <li>Will be visible</li>
                    <li>Will occupy the right most column of its parent container</li>
                    <li>Will have a distinct background color of your choice using hsl, rgb, or hex</li>
                </ul>
            </li>
            <li>'content' div
                <ul>
                    <li>Should occupy the left most column of its parent container</li>
                </ul>
            </li>
        </ul>
    </li>
    <li>When the screen width is greater than 800px, the following styles should be implemented
        <ul>
            <li>'main' div
                <ul>
                    <li>Should have 3 columns - a 200px column on the left, a 200px column on the right, and a column in the middle that is 100% of the viewport width minus the width of the two other columns</li>
                </ul>
            </li>
            <li>'sidebar' div
                <ul>
                    <li>should occupy the right most column of its parent container</li>
                </ul>
            </li>
            <li> 'ad-bar' div
                <ul>
                    <li>should occupy the left most column of its parent container</li>
                    <li>should have a distinct background color set using hsl, rgb, or hex</li>
                </ul>
            </li>
            <li>'content' div
                <ul>
                    <li>should occupy the center column of its parent container</li>
                </ul>
            </li>
        </ul>
    </li>
</ol>

Your display should look similar to this at screen sizes below 600px;

<img width="495" alt="Screen Shot 2022-04-04 at 4 30 22 PM" src="https://user-images.githubusercontent.com/89106805/161649288-7d848453-2788-45bd-9094-511d2536cc1e.png">

Similar to this between screen sizes 600px and 800px;

<img width="714" alt="Screen Shot 2022-04-04 at 4 32 13 PM" src="https://user-images.githubusercontent.com/89106805/161649339-2da18ba7-8e56-447c-9f81-805fa369830b.png">


And similar to this for screens over 800px;

<img width="820" alt="Screen Shot 2022-04-04 at 4 32 41 PM" src="https://user-images.githubusercontent.com/89106805/161649374-5134fb89-a785-458c-ac1b-2fb52625c8b6.png">

