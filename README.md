# Pixel's Arcade

Pixel's Arcade is a collection of single-player JavaScript games designed to be played in browser on desktop or mobile devices.

Currently available games include:
- Slap-a-Rabbit
- Rock, Paper, Scissors
- Dead Heads Memory Game
- Space Invaders

The concept of the site is one targeted towards users who are searching for quick, accessible games to pass the time on their PC or mobile phone. The games were chosen for their intuitive gameplay so that a user can "pick up and play" quickly. The website is built with future expansion in mind.

![Pixel's Arcade](readme-docs/amiresponsive.webp)

The live site can be found here: [Pixel's Arcade](https://sjecollins.github.ip/ci-pp2-pixels-arcade)

# Table of Contents

- [User Experience](https://github.com/SJECollins/ci-pp2-pixels-arcade#user-experience)
- [Features](https://github.com/SJECollins/ci-pp2-pixels-arcade#features)
  - [Universal](https://github.com/SJECollins/ci-pp2-pixels-arcade#universal)
  - [Index Page](https://github.com/SJECollins/ci-pp2-pixels-arcade#index-page)
  - [Slap-a-Rabbit](https://github.com/SJECollins/ci-pp2-pixels-arcade#slap-a-rabbit)
  - [Rock, Paper, Scissors](https://github.com/SJECollins/ci-pp2-pixels-arcade#rock-paper-scissors)
  - [Dead Heads Memory Game](https://github.com/SJECollins/ci-pp2-pixels-arcade#dead-heads-memory-game)
  - [Space Invaders](https://github.com/SJECollins/ci-pp2-pixels-arcade#space-invaders)
  - [Future Expansion](https://github.com/SJECollins/ci-pp2-pixels-arcade#future-expansion)
- [Design](https://github.com/SJECollins/ci-pp2-pixels-arcade#design)
- [Technologies Used](https://github.com/SJECollins/ci-pp2-pixels-arcade#technologies-used)
- [Testing](https://github.com/SJECollins/ci-pp2-pixels-arcade#testing)
- [Deployment](https://github.com/SJECollins/ci-pp2-pixels-arcade#deployment)
- [Credits](https://github.com/SJECollins/ci-pp2-pixels-arcade#credits)


# User Experience

## User Story
- As a user, I would like to easily browse for a game to play
- As a user, I would like to easily understand the game I am playing
- As a user, I would like to select the level of difficulty 
- As a user, I would like feedback on my progress in the game as I am playing
- As a user, I would like to know how I did when the game is finished
- As a user, I would like to be able to quickly reset the game whenever I choose

# Features

## Universal
### Header
![Header](readme-docs/header.webp)

- The header element features across all pages. It includes the website title flanked by two icons with a navigation bar below.
- The title is a link which directs the user to the index page. When hovered over, the text transitions to a darker green indicating its interactivity.
- The navigation bar includes links to the game pages. Similarly to the header, on hover the text transitions to a darker green to provide feedback to the user when interacted with.

### Footer
![Footer](readme-docs/footer.webp)

- The footer element features social media links and is found on all pages.
- The links have a similar transition to green as found in the header.

### Instructions
<details>
<summary>Instructions Example Image</summary>

![Instructions](readme-docs/instructions-invaders.webp)
</details>

- Each game page features an instructions overlay.
- The instructions overlay can be displayed by clicking on the text "instructions" beneath the game's title. The interactivity is indicated by the cursor changing to a pointer and the text being underlined when hovered over.
- The overlay includes the game title, simple instructions and a link styled as a button to dismiss the overlay.
- The overlay is styled with white text on a black background. A box-shadow gives the illusion of the overlay floating over the game board. The "Got It!" link is styled as a button with black text on a white background that transitions to white text on a green background when hovered over to indicate to the user that they are about to interact with it.

### Game Over
<details>
<summary>Game Over Example Image</summary>

![Game Over](readme-docs/game-over-cards.webp)
</details>

- Each game page features a Game Over overlay when the game ends.
- The overlay includes a heading announcing the end of the game, text informing the user of the result (whether they won or their points), and two links styled as buttons that allow the user to either play again or return to the index page.
- The overlay is styled with green text on a black background. Similarly to the instructions overlay, it features a box-shadow to give an illusion of it floating over the game. The links are styled similarly as well with the same transition from black on white to white on green when hovered over.

## Index Page
<details>
<summary>Index Page Image</summary>

![Index Page](readme-docs/index.webp)
</details>

The index page acts as a simple menu for the games available on the website. A heading invites the user to select the game they would like to play from the selection below which contains a grid of images linking to the game pages, with their respective titles underneath.  

## Slap-a-Rabbit
<details>
<summary>Slap-a-Rabbit Image</summary>

![Slap-a-Rabbit](readme-docs/rabbit.webp)
</details>

Slap-a-Rabbit is a a whack-a-mole style game. The title and presentation of the game are intended to make it as intuitive as possible on first interaction. Immediately on page load, the user is presented with the game title, the option to read instructions, buttons for level selection and game reset, and the empty game board itself with the default time and score displays.
- Instructions:
  - If the user hovers over the instructions text, their cursor changes to a pointer and the text becomes underlined to indicate they can click. This displays the instructions overlay which gives a brief introduction to the game and can be dismissed by clicking "Got It!"
- Buttons:
  - On selecting a level, the game begins, the timer starts and the rabbits pop up from the holes.
  - The level buttons are disabled during gameplay to prevent the user from triggering the startGame function in JS multiple times and breaking the game.
  - The selected level is underlined and font is bolded.
  - The reset button can be selected at any time and will reload the page.
- Gameplay:
  - On game start, the user is given 30 seconds to play the game, as explained in the instructions overlay.
  - The speed of the rabbits is determined by the level selected.
  - When a rabbit appears from a hole, the user can click or tap the rabbit which changes the image briefly and plays a sound to indicate interaction. The user is prevented from selecting the same rabbit multiple times.
  - Points are incremented and displayed each time a rabbit is "slapped."
  - At the end of 30 seconds, the Game Over overlay is displayed with the user's total "slaps" and the user can then decide if they would like to play again or return to the index page.

## Rock, Paper, Scissors
<details>
<summary>Rock, Paper, Scissors Image</summary>

![Rock, Paper, Scissors](readme-docs/rps.webp)
</details>

Rock, Paper, Scissors is a classic two-player game. Here the user can play against the computer in what is a essentially a random chance game. The game features instructions below the title, buttons to choose between best of three or five and to reset the board, displays for the computer's and user's choices, the scores, the round result, and the selectable options for the user at the bottom.
- Instructions:
  - If the user hovers over the instructions text, their cursor changes to a pointer and the text becomes underlined to indicate they can click. This displays the instructions overlay which gives a brief introduction to the game and can be dismissed by clicking "Got It!"
- Buttons:
  - The user has the option of playing best of three or best of five.
  - When selected, the button is underlined and font is bolded.
  - The level buttons are disabled during gameplay.
  - The reset button reloads the page at any stage.
- Gameplay:
  - The user starts each round by selecting from one of the options at the bottom of the screen.
  - With each selection, the displays are updated so that the choices of the user and computer are shown as images, the scores are incremented and displayed, and the round result is updated and displayed.
  - When either the user or computer reaches the required number of wins, the Game Over overlay is displayed and the result of "YOU WIN" or "YOU LOSE" is displayed depending on the outcome. The user can then decide if they would like to play again or return to the index page. 

## Dead Heads Memory Game
<details>
<summary>Dead Heads Memory Game Image</summary>

![Dead Heads Memory Game](readme-docs/cards.webp)
</details>

Dead Heads Memory Game is a classic card game where the user matches pairs while timed. It features instructions, buttons to select diffculty and reset the game, and displays for the time, correctly matched pairs and failed attempts.
- Instructions:
  - If the user hovers over the instructions text, their cursor changes to a pointer and the text becomes underlined to indicate they can click. This displays the instructions overlay which gives a brief introduction to the game and can be dismissed by clicking "Got It!"
- Buttons:
  - On selecting a difficulty, a board of six, eight or ten pairs of cards is generated and displayed. 
  - The difficulty buttons are disabled during gameplay to prevent generating further cards.
  - The selected difficulty is bolded and underlined.
  - The reset button can be used at any time to reload the page.
- Gameplay:
  - On game start, the timer begins.
  - The user can flip two cards at a time only. If the cards match, they remain face up, the pairs tally is incremented, and the user can select a further two cards. If they do not match, the cards flip back over, the attemps tally is incremented, and the user can then select two more cards to flip.
  - Upon successfully matching all pairs on the board, the Game Over overlay appears with the number of pairs the user has matched and the time in which the user has done so. The user then has the option to play again or return to the index page.

## Space Invaders
<details>
<summary>Space Invaders Image</summary>

![Space Invaders](readme-docs/invaders.webp)
</details>

Space Invaders is a classic arcade game in which the user controls a sprite and must shoot enemies before they reach the bottom of the screen. It features instructions, buttons to start the game, change the enemy wrap or reset the page, displays for lives and the score, and on-screen controls.
- Instructions:
  - If the user hovers over the instructions text, their cursor changes to a pointer and the text becomes underlined to indicate they can click. This displays the instructions overlay which gives a brief introduction to the game and can be dismissed by clicking "Got It!"
- Buttons:
  - The user can begin the game by selecting the start button.
  - The user can change how to enemies move across the game board by clicking the wrap button.
  - The user can reset the page at any point with the reset button.
- Gameplay:
  - On game start, the invaders are generated and begin to move across the game board. After a set period of time, an enemy spaceship or "boss" appears which moves back and forth at the top of the screen and drops bombs which can damage the tank below.
  - Using either keyboard or on-screen controls, the user can move the tank left or right at the bottom of the screen and fire a missile at the enemies.
  - In line with the Rule of Three, the tank has three lives, which can be lost when hit with the bomb. And the boss must be hit three times to destory it.
  - When an invader is killed the score is incremented and when the tank is hit the lives display decreases by one.
  - The game can by won by destroying all the invaders and the boss. The game is lost when the invaders reach the bottom of the screen or touch the tank, or the tank loses all of its lives.
  - When the game ends, the Game Over overlay is displayed telling the user if they lived or died and displays the number of invaders killed.

## 404 Page
<details>
<summary>404 Page Image</summary>

![404 Page](readme-docs/error-page.webp)
</details>
The 404 page is very simply styled. It features a link styled as a button that directs the user back to the home page.

## Future Expansion
The website is designed with expansion in mind.
1. _Additional games_. There are four playable games currently available on the site. These games were chosen from ten that I have been working on as they are the most interesting and complete at the time of starting the project. The intention is to expand with further games.
2. _Expanding current games_.
    - Slap-a-Rabbit:
      - Additional difficulty levels with a large board, more holes and more variety in speed.
    - Rock, Paper, Scissors:
      - Different game modes with an expanded range of choices, e.g. Rock, Paper, Scissors, Lizard, Spock.
    - Dead Heads Memory Game:
      - Additional levels with a larger board and more cards.
      - New difficulty challenge including a timer so the user has to race against the clock.
    - Space Invaders:
      - Additional levels including different patterns for the invaders, different or increasing speeds, and new enemies.
      - The option for a progressive game difficulty where new enemies are spawned either after a certain time or upon removal of all current enemies and the score and lives are carried forward.
3. _High scores_. A separate page where scores can be imported, stored and updated upon completion of a game. It could be unique to the individual user to track themselves or available to anyone who uses the site to compare and compete with other users, or both. This may have to include having users create profiles, or perhaps they could be prompted to enter their initials on completion of the game, like in an arcade.
4. _Game sections_. Currently unnecessary, but if the website were to expand there could be the potential to include game categories, e.g.:
    - Having separate single-player or multiplayer sections so that users can browse games they can play against other people.
    - Device specific categories. Not all games are suited to touchscreens. While they can be adapted in some ways, like Space Invaders, it may be necessary in some cases to state clearly to users whether they can play a particular game on their device.
5. _Support or contact page_. If a website such as this were to be available to users in real life, a method for users to report bugs or ask for help would be necessary.
6. _Options menu_. To allow the user to control display and sound settings.

# Design

The overall design is a retro aesthetic inspired by the Apple IIc. The colour design and typography are heavily influenced by the Apple's display. Wherever possible, corners are rounded like the Apple's casing in an attempt to mimic the experience of viewing a game through the Apple's monitor.

The games are generated on a "board" on each individual page and wrapped in this style to meld them together as a collection. Certain design features are present across all pages to attempt to tie the games together - though their individual designs may not match - so that the site has an arcade-like feeling where the user can find different kinds of games all in one place.

The site is designed with future expansion in mind. The index page features links to the games as pictures in a simple grid in the center of the screen with the intention to slot new games neatly into this grid as the site's content grows. 

## Colour

There are three main colours featured across the website - green, black and off-white. These are based on the Apple IIc's green phosphorous display and it's casing. Although, the colours are inverted in a manner, as the "main screen" is white surrounded by black rather than vice versa for readability.

The minimalist colour palette is also intended to be unobtrusive. It should not draw attention from games themselves.

## Typography

Google Fonts was used to import the Press Play 2P font to style.css. This is the only font used on the website as it is the only font available on Google Fonts that is reminiscent of the bitmap font used on on the Apple IIc.

## Buttons and Links

- Links are styled with a dark green transition to provide feedback to the user when hovered over.
- Level and reset buttons are styled with green text on black and transition to white on green when hovered over. When selected, the font-weight increases and a green underline is applied to mark which level is active. 
- Overlay buttons are styled with black text on a white background to stand out on the black overlay. When hovered over, they transition to white text on a dark green background.
- Though not explicitly a link or button, the instructions text on each game is styled so a underline appears when hovered over to indicate to the user that it is interactive. 

## Sound
Currently, sound is limited to simple sound effects in three of the games to demonstrate that sound can be added.

## Game Designs

### Slap-a-Rabbit
Slap-a-Rabbit is a whack-a-mole style game. The images were drawn in Inkscape with a cartoony design to go with the humorous tone intended. Similarly, the sound chosen for "slapping" is intentionally over-the-top.

### Rock, Paper, Scissors
Rock, Paper, Scissors is very minimalistically designed as the choice of using this game on the website was to display handling DOM elements. As such, the focus is on changing the UI when the user interacts with the game.

### Dead Heads Memory Game
Dead Heads Memory Game has a slightly more morbid design purely due to the fact that I have a large collection of images I had previously created for other projects. However, they created an interesting, memorable look on the black cards.

### Space Invaders
Space Invaders is a classic arcade game. The intention was to honour that when creating the sprites and so this game ended up most closely matching the overall style of the website. The explosion sound used is reminiscent of classic arcade sounds. 

The "invaders" are a modified version of the website's logo. The controls are very minimalist and easy to understand. The game board itself features a box-shadow to "lift" the game off the page to attempt to give the feeling of a screen sitting up in front of you like an arcade cabinet.

## Wireframes

Wireframes were created in Balsamiq.

<details>
<summary>Index Page Wireframe</summary>

![Index Wireframe](readme-docs/wireframe-index.png)
</details>

<details>
<summary>Game Screen Wireframe</summary>

![Game Screen Wireframe](readme-docs/wireframe-game-screen.png)
</details>

<details>
<summary>Game Over Wireframe</summary>

![Game Over Wireframe](readme-docs/wireframe-game-over.png)
</details>

# Technologies Used

- [HTML5](https://en.wikipedia.org/wiki/HTML5): mark-up language.
- [CSS3](https://en.wikipedia.org/wiki/CSS): styling.
- [JavaScript](https://en.wikipedia.org/wiki/JavaScript): programming language.
- [GIT](https://git-scm.com): for version control.
- [GitHub](https://github.com): for host repository.
- [Gitpod](https://www.gitpod.io): online IDE.
- [Google Fonts](https://fonts.google.com): to import font.
- [Balsamiq](https://balsamiq.com): to create wireframes.
- [GIMP](https://www.gimp.org): to edit images for Rock, Paper, Scissors.
- [Inkscape](https://inkscape.org): to create images for Slap-a-Rabbit, and arrows for Space Invaders.
- [Aseprite](https://www.aseprite.org): to create the logo, and the sprites for Space Invaders.

# Testing

## [HTML Validator](https://validator.w3.org/)
- Index:
  - ![Index results](readme-docs/index-html.webp)
  - [Link to HTML Validator](https://validator.w3.org/nu/?doc=https%3A%2F%2Fsjecollins.github.io%2Fci-pp2-pixels-arcade%2F)
- Slap-a-Rabbit:
  - ![Slap-a-Rabbit results](readme-docs/rabbit-html.webp)
  - [Link to HTML Validator](https://validator.w3.org/nu/?doc=https%3A%2F%2Fsjecollins.github.io%2Fci-pp2-pixels-arcade%2Frabbit.html)
- Rock, Paper, Scissors:
  - ![Rock, Paper, Scissors results](readme-docs/rps-html.webp)
  - [Link to HTML Validator](https://validator.w3.org/nu/?doc=https%3A%2F%2Fsjecollins.github.io%2Fci-pp2-pixels-arcade%2Frps.html)
- Dead Heads Memory Game:
  - ![Dead Heads Memory Game results](readme-docs/cards-html.webp)
  - [Link to HTML Validator](https://validator.w3.org/nu/?doc=https%3A%2F%2Fsjecollins.github.io%2Fci-pp2-pixels-arcade%2Fcards.html)
- Space Invaders:
  - ![Space Invaders results](readme-docs/invaders-html.webp)
  - [Link to HTML Validator](https://validator.w3.org/nu/?doc=https%3A%2F%2Fsjecollins.github.io%2Fci-pp2-pixels-arcade%2Finvaders.html)

## [CSS Validator](https://jigsaw.w3.org/css-validator/)
<p>
    <a href="https://jigsaw.w3.org/css-validator/check/referer">
        <img style="border:0;width:88px;height:31px"
            src="https://jigsaw.w3.org/css-validator/images/vcss-blue"
            alt="Valid CSS!" />
    </a>
</p>

- [Index results](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fsjecollins.github.io%2Fci-pp2-pixels-arcade%2F&profile=css3svg&usermedium=all&warning=1&vextwarning=&lang=en)
- [Slap-a-Rabbit results](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fsjecollins.github.io%2Fci-pp2-pixels-arcade%2Frabbit.html&profile=css3svg&usermedium=all&warning=1&vextwarning=&lang=en)
- [Rock, Paper, Scissors results](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fsjecollins.github.io%2Fci-pp2-pixels-arcade%2Frps.html&profile=css3svg&usermedium=all&warning=1&vextwarning=&lang=en)
- [Dead Heads Memory Game results](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fsjecollins.github.io%2Fci-pp2-pixels-arcade%2Fcards.html&profile=css3svg&usermedium=all&warning=1&vextwarning=&lang=en)
- [Space Invaders results](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fsjecollins.github.io%2Fci-pp2-pixels-arcade%2Finvaders.html&profile=css3svg&usermedium=all&warning=1&vextwarning=&lang=en)

All pages passed CSS3 validation, however there were 8 warnings for cards.css related to vendor extensions.

## [JSHint](https://jshint.com/)

JSHint was used to detect errors in the JavaScript.
- All JavaScript files were flagged for missing semicolons, as expected.
- One warning was flagged in invaders.js:
  - "129	Expected an assignment or function call and instead saw an expression."
  - This occurred due to the placement of bombInterval within the moveBoss function.

## Lighthouse
The site was tested using Lighthouse in Chrome DevTools throughout the development to check performance, accessibiltiy, best practices and SEO. The final test on Lighthouse was run on incognito mode. The results are below.

<details>
<summary>Lighthouse Results</summary>

![Lighthouse Results](readme-docs/lighthouse.webp)
</details>

## Browser Compatibility
The website was tested on:
- Chrome Version 101.0.4951.67
- Firefox Version 101.0.4951.67
- Edge Version 101.0.1210.53
- Safari iOS Version 15.4.1

## Testing Functionality
The website was tested on the above browsers for these functionality tests.

<details>
<summary>Universal Features Testing</summary>

![Universal Features](readme-docs/pp2-testing-universal.png)
</details>

<details>
<summary>Slap-a-Rabbit Testing</summary>

![Slap-a-Rabbit](readme-docs/pp2-testing-rabbit.png)
</details>

<details>
<summary>Rock, Paper, Scissors Testing</summary>

![Rock, Paper, Scissors](readme-docs/pp2-testing-rps.png)
</details>

<details>
<summary>Dead Heads Memory Game Testing</summary>

![Dead Heads Memory Game](readme-docs/pp2-testing-cards.png)
</details>

<details>
<summary>Space Invaders Testing</summary>

![Space Invaders](readme-docs/pp2-testing-invaders.png)
</details>

## Testing User Story
- "As a user, I would like to easily browse for a game to play"
  - The main page acts as a list or library of the game content of the website. All games available are presented in a grid as the focus of the main page. Users can access any of the games on the site from this page.
  - The navigation bar in the header contains links to the games available on the site. This navigation bar is present across all pages so that users can easily jump between game pages when they choose.

- "As a user, I would like to easily understand the game I am playing"
  - All games present on the website are simple, classic games that are intuitive to play.
  - All game pages feature an instruction overlay that can be displayed when the user clicks on "Instructions" directly below the the game's title. The basics of the game are presented to the user and they can reference this overlay whenever they wish.

- "As a user, I would like to select the level of difficulty"
  - Two of the games available on the website feature difficulty levels.
    - In Slap-a-Rabbit, the user can select between three levels with increasing gameplay speeds.
    - In Dead Heads Memory Game, the user can select between three levels which generate increasing numbers of pairs of cards to match.
  - Rock, Paper, Scissors allows the user to select the length of the game, however this does not really effect the "difficulty" of the game itself.
  - Currently, Space Invaders does not feature difficulty levels.

- "As a user, I would like feedback on my progress in the game as I am playing"
  - In Slap-a-Rabbit, above the board there is a timer counting down for 30 seconds so that the user may monitor the length of time they have remaining. There is also a "slaps" counter that provides the user a running tally of the points as they play.
  - In Rock, Paper, Scissors, with each decision the user's and computer's choice image is updated, their score is incremented and the round result is updated to tell the user the result of each round.
  - In Dead Heads Memory Game, above the board there is a timer counting up from the beginning of the game, a score counter that updates with each successul pair match and an "attempts" counter telling the user how many times they failed to match a pair of cards.
  - In Space Invaders, there is a lives counter for the user that counts down each time a bomb hits the tank and a score counter that counts up each time an invader or the boss is killed.

- "As a user, I would like to know how I did when the game is finished"
  - Each game features a Game Over overlay which displays the user's final score and, in the case of Rock, Paper, Scissors or Space Invaders, whether the user won or lost.

- "As a user, I would like to be able to quickly reset the game whenever I choose"
  - All games feature a reset button in the UI. This simply reloads the the page.

## Bugs

### Fixed Bugs
- Dead Heads Memory Game:
  1. On iPhone, images were not displaying correctly when cards flipped.
      - Safari was not handling transform correctly prior to the addition of "translateZ(1px)" 
      - The solution was found in this [thread on Stack Overflow](https://stackoverflow.com/questions/59716761/flip-card-bug-safari)

- Space Invaders:
  1. On iPhone, the "explosion" sound effect was not playing correctly.
      - This is due to iOS not allowing autoplay of sound. The user has to trigger sound through an interaction. Once it has been played once, it will work as intended.
      - While it is not a perfect solution, the sound is muted and triggered on game start, then unmuted when the shoot or dropBomb functions are called. So, the sound now plays as intended.
      - In future, the intention is to introduce a menu where the user can adjust their audio settings so that they have control volume or mute sounds.
  2. While it did not prevent gameplay, when a missile exited the top of the screen, or a bomb or invader exited the bottom of the screen, the sprites were removed but in console the following error was logged indefinitely: "Uncaught TypeError: Cannot read properties of undefined (reading 'classList')".
      - I believe this was due to JS looking for the next div, but as it had reached the top or bottom of the grid of divs there was nowhere to look.
      - A somewhat hacky way to fix this involved extending the grid and telling JS to remove the "bombs" or "invaders" a row earlier in the grid. And similarly at the top of the game grid, the missile is removed before it actually reaches the top row.
  3. The game would end prematurely if all invaders were removed but the boss was still alive.
      - This was a two part problem. The first simply involved changing the win conditions so that the game didn't count the user as winning unless both invaders and boss were dead.
      - However, there was also an issue where though the invaders were removed, the game was still tracking the progress of their array down the grid. So, a variable of invadersDead was added that is just a simple boolean. It's initially declared as false. When all invaders are removed, now instead of calling checkEnd() the moveInvaders function changes invadersDead to true and we also clear the interval to stop the game moving them even though they're gone. If invadersDead is true and bossDied is true, the user wins and the user can no longer lose from the game moving invisible invaders.
  4. Similarly to the bugs above, there was a bug that involves triggering the game end when the invaders reach the bottom of the screen.
      - There was difficulty getting the game to trigger when the invaders reached the bottom of the screen. One hacky solution involved triggering the end of the game when the invaders array reached a certaion point in the squares array but this didn't account for invaders removed so the top row of invaders never reached the bottom even when no bottom invaders were visible to the player.
      - Fixed as of 30/06. Created divs with an end-tile class that endGame now looks for and if a div contains both invaders and end-tile, the game ends. Still a little hacky as there are two rows of divs not visible below the game-board, but unfortunately without those the bomb and invaders trigger the error mentioned in **2** above.

### Known Bugs
None known currently.

# Deployment
## Steps to deploy site:
- In the GitHub repository, navigate to the "Settings" tab.
- Scroll down to "Pages" in the menu on the left hand side.
- Under the heading "Source", click the drop-down menu and select "main" branch.
- The page will automatically refresh with a link to the deployed website.
- It may not go live for a few minutes, refresh the page to update the link.
- Once deployed, the live website will automatically update when commits are made to the main branch.

The live site can be found here: [Pixel's Arcade](https://sjecollins.github.io/ci-pp2-pixels-arcade)

## Steps to clone site:
- In the GitHub repository, click the "Code" button.
- Select "HTTPS" and copy the URL.
- Open Git Bash and navigate to the repository where you would like to locate the cloned repository.
- Type "git clone" followed by the copied URL.
- Press enter to create the clone.

# Credits

## Code

- The code for Slap-a-Rabbit was adapted from:
  - [Frank's Laboratory](https://www.youtube.com/watch?v=RTb8icFiSfk&ab_channel=Frankslaboratory)
  - [Ania Kubow](https://www.youtube.com/watch?v=rJU3tHLgb_c&ab_channel=CodewithAniaKub%C3%B3w)
- The code for Rock, Paper, Scissors was adapted from:
  - [Web Dev Simplified](https://www.youtube.com/watch?v=1yS-JV4fWqY&ab_channel=WebDevSimplified)
  - [Ania Kubow](https://www.youtube.com/watch?v=RwFeg0cEZvQ&t=1s&ab_channel=CodewithAniaKub%C3%B3w)
- The code for Dead Heads Memory Game was adapted from:
  - [Marina Ferriera](https://marina-ferreira.github.io/tutorials/js/memory-game/)
  - [Tania Rascia](https://www.taniarascia.com/how-to-create-a-memory-game-super-mario-with-plain-javascript/)
- The code for Space Invaders was adapted from:
  - [Ania Kubow](https://www.youtube.com/watch?v=3Nz4Yp7Y_uA&ab_channel=CodewithAniaKub%C3%B3w)
- The fix for the card flip not working correctly on iPhone came from this [Stack Overflow thread](https://stackoverflow.com/questions/59716761/flip-card-bug-safari)
- The code to add sound effects is based on this [this tutorial by Mt. Ford Studios](https://www.youtube.com/watch?v=LfSBbrGqFV0&ab_channel=Mt.FordStudios)
- The code to add the 404 page is based on [this video by Dani Krossing](https://www.youtube.com/watch?v=kPtS4vO42II&ab_channel=DaniKrossing)
- The code to play the sound effects in the games is based on [this thread from Stack Overflow](https://stackoverflow.com/questions/9419263/how-to-play-audio)


## Media
With the exception of the images for Rock, Paper, Scissors, I created the images on the website.

- The images for Rock, Paper, Scissors are from this [free clipart image](https://www.clipartmax.com/middle/m2i8i8G6H7K9Z5H7_rock-paper-scissors-clipart-rock-paper-scissors-clip-art/)
- Sound effects from Pixabay:
  - [Slap-a-Rabbit hit sound](https://pixabay.com/sound-effects/karate-chop-6357/) by ccolbert70Eagles23
  - [Dead Heads Memory Game flip sound](https://pixabay.com/sound-effects/book-page-45210/) by fellur
  - [Space Invaders explosion sound](https://pixabay.com/sound-effects/8-bit-explosion1wav-14656/) by timgormly

## Acknowledgements 
I would like to thank my mentor, Brian Macharia, for all the time he took to help me with this project. He provided excellent feedback and encouragement, and helped to make the project a lot of fun to build!