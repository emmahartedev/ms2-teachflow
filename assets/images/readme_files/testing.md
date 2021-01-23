## Testing

### User Story Testing
In this section, the user stories which were defined in the [UX](#ux "goto-ux") section of this README document are re-evaluated.

### User Stories

#### Potential ESL Teacher Goals
As a potential ESL teacher:

* I am looking for information on ESL countries so that I can find out what appeals to me.
    * 4 Asian countries (popular ESL destinations) are featured in the maps section on index.html. 
    * Upon clicking on a country, an info section is displayed. 
    * 3 markers are placed on each country. Each marker shows a popular city to teach ESL in. 
     ![Maps example](assets/images/readme_files/maps.png)

* I usually do all my research on my phone so I would like the website to be mobile responsive.
    * A mobile-first design approach has been adopted.
    * The Bootstrap grid system provides an easy solution to creating mobile responsiveness.  
     ![Mobile responsiveness example](assets/images/readme_files/mobilerespons.png)

* I am looking for information about a typical class lesson so I can learn about a typical day on the job.
    * An entire class lesson is provided in game.html which gives the user a clear idea of what a typical class lesson looks like.
    * The class lesson includes flashcards, a song and a memory game.
    * the entire class lesson is approx. 1 hour in length. 
    ![Classtime](assets/images/readme_files/classtime.png) 

* I would like to be able to contact the website owners if I have any questions about the content.
    * A contact form is available on index.html.
    * Once a message has been submitted successfully, the contact form collapses and a admission message is dispalyed.
    ![Contact us](assets/images/readme_files/contact.png)

* I would like to see the requirements for becoming an ESL teacher, the salary and benefits.
    * Requirements, salary and additional information is featured in the country maps information section.
    * This information is displayed when a country is selected.
    ![Maps information](assets/images/readme_files/mapinfo.png)

#### Current ESL Teacher Goals
As a current ESL Teacher:

* I would like to see information on regions in countries as I am familiar the countries do not give me indepth information. 
    * General country information is included in the content map section. 
    * 3 Markers have been placed on each map, showing popular cities to teach in. 
    ![Maps information](assets/images/readme_files/mapinfo.png)


* I would like to see some interactive information about the countries, such as the current weather or statistics so that I am receiving live, updated information. 
    * Due to time limitation & project scope, a weather API was not integrated into this release. 
    * Country info however can be seen in the country maps information section.
        As this is not an API, this information would need to be updated manually. 
    ![Maps information](assets/images/readme_files/mapinfo.png)


* I would like any class material featured to be focused on learning English words and improving students speaking skills. 
    * Multiple content is featured including flashcards, a song lesson and a memory game.
    * A 'Farmyard Animal' theme is used to create a realistic class lesson. 
    * The class lesson is focused on improving vocabulary, pronounciation & grammer. 
    ![Classtime content](assets/images/readme_files/classtimeeng.png)


* I would like to be able to sign up to a newsletter. 
    * A newsletter signup option is offered on the contact us form.
    ![Newsletter signup](assets/images/readme_files/newslettersignup.png)

### Browser Compatibility
[LamdaTest](https://www.lambdatest.com/) was used tp test the website on the following browsers:

* Google Chrome
* Firefox
* Microsoft Edge
* Safari 
* Opera

In addition, internet explorer was tested. As expected issues with Javascript were encountered.
In index.html, the contact form does not submit successfully. In game.html,  all onclick button function are not working. 
As IE is outdated, these bugs were not resolved in this reslease. 


### Responsiveness
The website's responsiveness was tested using [Chrome Dev Tools](https://developers.google.com/web/tools/chrome-devtools).
CSS Media Queries were written as required to improve appearances. 

The devices (and screen widths) tested with include: 
* iPhone 5/SE (320px)
* iPhone 6/7/8 (375px)
* iPhone 6/7/8 Plus (414px)
* iPad (768px)
* iPad Pro (1024px)
* Laptop (1200px)
* Desktop (1920px)
    
In addition to this, [Lighthouse](https://developers.google.com/web/tools/lighthouse) was run in Chrome Dev Tools, to generate reports on the quality of the website.
Primary, actions were taken to improve the 'Performance' rating on mobile devices. 
The following report was generated before changes were made:
![Lighthouse Mobile Report ](aassets/images/readme_files/lhmobb.png)

Actions taken to improve the rating included:
* 


### Code Validation
#### HTML 
* All HTML code was checked using [The W3C Markup Validation Service](https://validator.w3.org/).
* No errors or warnings were produced.

#### CSS
* All CSS code was checked using [The W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/).
* No erros were produced. 
* 26 noncritical warnings associated with imported stylesheets and vendor extensions were produced. 

#### Javascript
* All Javascript code was checked using [JSHint](https://jshint.com/). 
* As a result, all undefined variables were found and removed. 
* Several warnings were received stating that: 'let' is available in ES6 (use 'esversion: 6') or Mozilla JS extensions (use moz). To resolve, a file named ".jshintrc"  was added to this project.

### Javascript Manual Testing 

#### General 
   * All javascript variables were logged to the console in Testinga

* Pre-loader
    * Loaded both index.html & game.html to test. 
    * Adjusted the 'fade-in' & 'fade-out' parmeters were to find a balance between a delay for the user & adequate load-time.

* Navigation
    * Three anchor links (Home, About, Contact Us) are sections on index.html. 'Classtime' is a stand alone page. Each link was clicked to test. 
    * When the jumping anchor links were clicked in the collapsed navbar window, the navbar did not close. This is documented [here](#bugs "goto-bugs").
   
* Smooth scrolling
    * Smooth scrolling is present when jumping anchor links are clicked (Home, About, Contact Us on index.html). Each link was clicked to test. 
    * No issues with smooth scrolling found in index.html.
    * In game.html, all navlinks however did not work due to the smooth scrolling code. 
        This bug is documented [here](#bugs "goto-bugs").

* Fixed navbar dissapear on scroll
    * Scrolled in both directions to test. 
    * Discoved that the navbar was not appearing quick enough at the top of the page, exposing the top margin added to the carousel items. Solution listed [here](#bugs "goto-bugs").

#### index.html

* Carousel
    * Carousel tested by both waiting for automatic cycling of items & by clicking on 'prev'/'next' buttons.
    * A bug was found on mobile devices. On smaller device sizes, half of the carousel items were cut off due to their position behind the fixed navbar.
      This is documented [here](#bugs "goto-bugs")
    
* Maps section (map and info content )
    * Clicked all four 'country' buttons, map and info content appears as expected 
    * Clicked on all markers in country maps, content appears as expected. 

* Contact us section
    * Tested form submission, section collapes as expected on successfully sending a message. 
    * Tested each 'required' field, all confirmed to be needed. 

#### game.html

* Flashcards section
    * Clicked each tile to playSound, sound plays as expected. 

* Memory Game section
    * Intructions
        * clicked the instructions button, the toggleDisplay function runs as expected. 
        * Clicked the button again to close, no issues found. 

    * Tiles pressed (sound and activation colour):
       * Clicked each tile, activation coloured tile appeared as expected. 
       * Sounds were overlapping, documented bug [here](#bugs "goto-bugs").

    * Start game (computer round):
        * clicked the start button. 
        * startRound funtion switches 'memory game' with the round information as expected. 
        * Start button is replaced by 'Listen & watch' as expected. 
    
    * Players turn (play round):
        * 'Listen & watch' is replaced with 'your go' & taps left info, as expected. 
        * tiles are clickable with coloured tiles on hover, as expected.

    * Remaining taps calculation: 
        * Clicked on correct tile, remaining tap descreases by one. 
    
    * Remaining round calculation:
         * Completed a round successfully, remaining rounds descreases by one.
         * Last remaining round is 0, this is replayed by 'Memory Game' once game is complete. 

    * Round successfull:
        * clicked on correct order of tiles
        * Start button section is replaced with a 'keep going message' as expected. 
        * StartRound function runs as expected

    * Round unsucessful: 
        * pressed a wrong tile in a round. The gameOver function ran as expected, displaying an alert box with a 'Whoops' message.

    * Game completed:
        * Played 15 rounds to test gameOver function. As expected an alert box with 'success' message is displayed and game is restarted.

### Bugs

#### Solved
* Navlinks in game.html not working:
The js hash code was interferring with the functionality of the nav link to game.html. While researching, I found a similar issue on [Stack Overflow](https://stackoverflow.com/questions/59706410/link-with-anchor-to-different-page-href). 
After reading this, I created a data attribute for the anchor links on index.html and targeted these only in the js hash code. The navigation then worked without any issues.

* Carousel image cut off in mobile:
On smaller device sizes, the top half of the carousel items were cut off due to their position behind the fixed navbar. To fix this, a top margin was added to the carousel items; which pushed the image down. 
After adding this code, the carousel appeared as expected. 

* Navbar Collapse not closing in index.html:
The collapsed navbar was not closing when one of the anchor links was clicked in index.html.  
To fix this, a javascript function which added & removed a show class to the navbar on click, was added to general.js. This resolved the issue.

* Fixed navbar dissapear on scroll: 
The userScrolled function was causing the nav bar to dissapear for a few seconds once it reached the top of the page. 
Because of this, the carousel's margin was unasthetically exposed. [Codepen](https://codepen.io/fbmiranda/pen/edqgxm) 
provided a solution to this, making sure that the user scrolls past the navbar before it dissapears. After modifying the code, the bug was solved. 

* Memory Game - Tiles pressed (sound and activation colour):
When iterating through each tile in a round, the longer audio files were overlapping. To fix, a timeout was set to the itertateThrough(storedRoundTiles) function. 
When tested again, the issue was fixed. 

#### Unsolved
* Double click on nav item 'Classtime' leads back to index.html.
----------------------------