# Project3
CMPM121 Third Project Card Game

Final Project Update & Postmortem | 6-12-2025 <br/>
 
CHANGELOG<br/>
------------------------------------------------------------------------------------------------------------------------------------------------------------
- CARD REVEAL DELAYS. Rather than being instant, there is now a 0.5s delay between cards being revealed.
- Cards already revealed on the player's side are now marked with a golden outline.
- The Console is now a feature!
    - You can now see in text what order things are occuring on the field. 
- Swapped points and mana location.
    - After some more playtest, it made more sense to have the mana on the left since it's on the left for the cards as well.
- Cards can no longer be moved after they are placed.
- Tie is broken by player winning, game is hard enough as is.
- Revamp of the end screen!
    - Now shows how many points both sides have at the end of game.
- Added the following cards:
    - Hermes
    - Ship Of Theseus
    - Midas
    - Aphrodite
    - Apollo
    - Hephaestus
    - Persephone
    - Prometheus
    - Pandora
    - Icarus
    - Iris
    - Nyx
    - Atlas
    - Helios
    - Removed Medusa
 
There are now some crash bugs since I've introduced so many new cards, with the size of the game it's become difficult to test and replicate. They're quite rare so hopefully you won't encounter them, but it's something to I have to keep in mind for future projects. Perhaps a way to develop a testing version.

Here is a list of cards added and tested:
https://docs.google.com/spreadsheets/d/1evXyXlMr6XoIrusqhWE59Ww_oS2-gdeqiCtHRJL9HJE/edit?usp=sharing

If you want a list of people who gave me feedback, my brother who helped me playtest and told me to switch the mana and points positions.

<ins>Assets</ins><br/>
Same as before, all default Love2D

Patterns same as the ones listed below.

------------------------------------------------------------------------------------------------------------------------------------------------------------
<ins>Patterns Used</ins><br/>
Inheritance - Cards inherit from a Base Card Class, letting it use methods and access common fields such as position without having to rewrite it.<br/>
Prototype - Also used  by the cards, all cards are a prototype of the base card.<br/>
Singleton - GameManager is a singleton. Technically the player and opponent classes are singletons as well.<br/>
Observer- GameManager also acts as an observer.<br/>

<ins>Postmortem</ins><br/>
I'm actually pretty happy with how the project turned out, both visually and technically. Everything feels well organized and scalable.<br/> 
The Card Class and inhertiance worked really well. The only thing I need to do to create a new card is copy, paste, change the values/numbers, implement the effect function, then add it to the pool and it's done and ready to play.<br/>
Not everything is perfect, the location has a few too many fields that could have been reduced if I made it a single location representing both player and enemy, but it works well enough so I'm not touching it further.<br/>
I still feel like I should have combined the grabber class and player class, but it would be very messy to do in its current state and, again, works well enough right now.<br/>

There's some interesting layouts I've seen in other people's projects such as a console showing what's happening or a side panel showing the card information, but with my current layout I can't make those work. Something to keep in mind for future projects though.

<ins>Assets</ins><br/>
None yet, everything is default Love2D.

