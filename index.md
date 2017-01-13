<p>This is a prototype I made to practive developing the framework and gameplay of 2D Platform Fighters like Nintendo's Super Smash Bros. series.</p>

<h3><p align="center">Framework Design</p></h3>

<p>The framework was developed using SDL2.1, Boost, and C++, but both demo and framework are in the very early prototype stages (as seen below).</p>

<p>As for the design of the framework, I treated each "state" of the game as its own state and utilized a stack to manage these states (such as MenuState, BattleState, PauseState). This allows for each state to be self contained and can be stacked upon each other without fear of any conflicts happening. (e.g. I can just push PauseState on top of BattleState to pause the game and then pop it off to unpause the game).</p>

<p>The framework also allows for basic graphic options such as different resolutions and fullscreen/windowed modes with borderless variants. The settings are saved in an ini file upon leaving the menu and are loaded at the game's initial startup.</p>

<p>The Controls are contained in a singleton that houses all the necessary data for each player's controls. It is built off of SDL's Keyboard and GameController classes and each state has a reference to the Controls singleton to be able to read user's input. The controls are customizable and are stored in an ini file that is read at the game's initial startup.</p>

<p>As for Gameplay Systems. I decided to use a form of Entity Component Model and create a base form of common entities (Stage,Fighter,Projectile) and attach components (Input, Collision, Graphics, Physics) that would be needed by each. This methodology allows for neater code that is self contained within its own component.</p>

<p>The Stage is a tileset that is loaded through an XML with a graphics layer and a collision layer. I went with this approach as it allows for easy creation and editing of stages. In the final version the stages will be hard coded to prevent any alteration of data, but the XML loading will still remain for User Created Content.</p>

<p>The Characters are all based off of one class, Fighter, and it's necessary components. However, each fighter has their own header file that houses all the data about their attributes and attacks.</p>

<p>Current Framework Features:</p>

<ul>
<li>Customizable resolution settings, fullscreen/windowed (both with borderless options)</li>
<li>Saving and customization of controls and graphics settings in ini files.</li>
<li>Stages are loaded through XMLs to allow for simple and fast stage creation/editing.</li>
<li>Controller and Fight Stick support.</li>
</ul>

<p>Although I call it a 2D Platform Fighter framework, with some minor tweaking the framework could be used to create almost any kind of 2D game.</p>

<h3><p align="center">The Prototype</p></h3>

<p>The prototype game is Super Smash Bros like and features two placeholder characters on a placeholder stage fighting it out. Each character has 4 Light Attacks, 3 Heavy Attacks, 4 jumping attacks, and 4 Special attacks that can be done using a combination of a direction + an attack button. It is in no way indicative of what the end result will look like.</p>

<p>Everything in the prototype is all placeholder and I own none of the placeholders used (Music, Graphics, Fonts). They are all owned by their respective copyright holders.</p>

<h3><p align="center">Video</p></h3>
<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/G5OdLZ-3JeM" frameborder="0" allowfullscreen></iframe></p>

<br>
<p><a href="http://mvpet.github.io/">Back to Main Page</a></p>
