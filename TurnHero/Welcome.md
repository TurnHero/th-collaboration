# TurnHero - new UX
## What is TurnHero?
**The pitch:** TurnHero is a new online board game *platform*, that allows its users to play their games online from any platform/device TurnHero stands apart from its compeditors by combing beatiful graphics with rule implementation and a simple user interface. Furthermore, TurnHero was built from the ground up with focus on supporting content creators and gaming enthusiast that want to be able to do spectating, casting, post game analysis etc.

**The vision:** TurnHero will be the premier board gaming site. It will be where official board game tournaments are hosted and the platform of choice for all streamers and content generators with an interest on digital board gaming. However, leveraging it's open-API approach and simple implementation paradigm, TurhHero will also be where new board games are brought to life digital-first, creating a new digital indie-community.

**The app:** TurnHero is a cloud based backend, that can execute board games (rules, state, etc.) and produce all the data needed to vizualize the game and it's interactions in the client. The client is a simple Unity app consisting of two main parts; a menu system for logging in and managing games, and a fully data-driven "game client" that can display draw any board game scene and present user interactions, based only on the data received from the backend.

TurnHero offers support for turn-based timers for tournament style play as well as full replay of all actions taken in a game. TurnHero also has a god-mode option, allowing content creators and commentators to see what is normally hidden to players, but also allowing all players to do post-game analysis.
- A beta version of the app can be accessed at [play.turnhero.com](https://play.turnhero.com/)

**The website:** Once TurnHero is up and running, users will be able to login to [turnhero.com](https://www.turnhero.com). This site will be a portal site, offering the same functionality as the app, but adding more features such as news, forums, etc.

### The user / player concept
Currently we are working with a user (account) and player (profile) approach, where a single account can have multiple profiles (similar to Netflix and others).

This opens up for the possibility of creating games with only your own account's profiles as players - which functions a bit like local "hotseat" games from computer gaming world.

## Target audience
We want to target board games as a whole. The current online community for board games is statistically dominated by male gamers, but we want to be cater to gamers of all genders! We specifically see an steep increase in younger women to the scene, so we definatly need to give them a relevant experience.

### Audience types and motivations
We have defined some user archetypes as well as some key motivational aspects for using TurnHero.

![Target Segments.png](Target%20Segments.png)

| Aspect / Motivation | Example
| -- | --
| Time | The Parent; a gamer but with too little time to meet and play board games with friends.
| Which game? | Couples; one of them feels their 1st choice isn’t being played. What could we try next?
| Young women | Plays board games with her friends before going out on weekends. Can play with friends during week.
| 5 minute gamer | Commuters who have a few minutes now and then to take their turn and follow up on a game’s status.
| Content creators | Stramers and content generators who need a good digital platform in order to create quality content with as little effort as possible.
| Designers | Designers looking to test designs, get feedback and stats. Looking for a publisher, doing a kickstarter or Make-My-Game.
| Curious | Casual gamer who plays board games occasionally but finds it easier to play online.
| Hardcore gamer | Wants to play more! Always looking for games being played.
| Statistics  | Players, designers and publishers can all benefit from in-depth statistics about played games.
| Keeping up | Publishers looking for designs and games. Interested in  statistics.

### Audience age
The age segment for board games is typically a bit higher for than (computer) gamers, so our estimate is in the range 18 ~ 50 years old.

# Visual expression
We are at the stage, where we need a find a good visual expression and to define our UX. Currently we have, what we could call, "Programmer Art".

We can define a few overall guidelines
- Mordern look and feel, but still honoring that we are in a board game world with lots of primary colors and wierd shapes.
- Similarity from phone devices to desktop apps and web pages.
- Simplicity over fanciness.

## Logo
Below are some example of our current logo. The colors of the "color" logo should of course be updated along with the a UI color theme.

The logo is abstract but represents the top left corner of a playing card or a board game board.

| Logo | Name
| -- | --
| ![Logo - white on black.png](Logo%20-%20white%20on%20black.png) | White on black
| ![Logo - black on white.png](Logo%20-%20black%20on%20white.png) | Black on white
| ![Logo - color on white.png](Logo%20-%20color%20on%20white.png) | Color on white

| Logo | Name
| -- | --
| ![Logo - color and text on white.png](Logo%20-%20color%20and%20text%20on%20white.png) | Color logo and text on white
| ![Logo - white and text on black.png](Logo%20-%20white%20and%20text%20on%20black.png) | White logo and text on black
| ![Logo - color and text on black.png](Logo%20-%20color%20and%20text%20on%20black.png) | Color logo and text on black

## Example screens
Below are some example screen shots from the current app with _"Programmer Art"_. For each screen, we have tried to describe it's purpose and what functionality is/should be there, as well as navigational links.

## Login
This is the opening screen of the app, where the user can
- Log in
- Recover a lost password
- Sign up for a new account
  - Current using username and password, but we will also support social media logins.
  - At some point this might be removed from the app and only be available in the portal - depending on payment/fee policies from Google and Apple.

![Screen - login.png](Screen%20-%20login.png)

| ![Screen - reset password.png](Screen%20-%20reset%20password.png) | ![Screen - signup.png](Screen%20-%20signup.png)
| -- | --

## Select profile
The current idea is to support multiple profiles per user account. This is a concept known from most media streaming platform such as Netflix.

Users can 
- Choose an existing profile
- Create / add a new profile
- Delete a profile
  - This should most likely not be available directly on the screen, but instead be in an "edit profile" page.

![Screen - select profile.png](Screen%20-%20select%20profile.png) 

| ![Screen - add profile.png](Screen%20-%20add%20profile.png) | ![Screen - delete profile.png](Screen%20-%20delete%20profile.png)
| -- | --

## Welcome (my overview)
This is the *main menu page* where the user will spend most of his/her time, before entering a game. It needs a <span style="color:red">**complete rework**</span> to be usable.

Below we describe what the main concepts are, and how they are done today,

**Main concepts**
- **Overview of my _ongoing_ games:** i.e. games where I am a participant and that have not yet finised.
  - What am I currently playing?
  - Is it my turn, in any of my ongoing games? I.e. where are people waiting for me?
  - From the overview, I can jump directly into the games.
- **Game management:** I want to interact with my games and create new ones. Most of the per-game features could perhaps be "hidden" away in a submenu to, as they are rarely used by players.
  - Start a new game.
  - Join a game using an game invitation.
    - Currently a very crude funciton, where the user pastes in a game id sent from another player. But this could be expanded into a list of invitations.
  - View (spectate) a game.
    - Similar to "join" this is currently uses a game id pasted into a text box. But we should have some way of finding games to spectate.
  - As a game "owner", I will be able to
    - Rename the game.
    - Delete the game (a development feature, that will later be made unavailable to players).
    - Restart the game (a development feature, that will later be made unavailable to players). Resets the game, keeping only the participating players.
    - Repeat the game. This creates a new game with the same players - sort of like a rematch.
- **A list of my friends:** This is currently not implemented. But players can have added other players as friends. We intend to be able to show their online-status.

![Screen - my overview.png](Screen%20-%20my%20overview.png)

| ![Screen - join game.png](Screen%20-%20join%20game.png) | ![Screen - rename game.png](Screen%20-%20rename%20game.png)
| -- | --

## Starting a new game
This is where players setup new games and add/invite players to them. This also needs a **complete rework**.

**A game has a few properties**
- A name / title.
- A description.
- An number of players range - e.g. 2-5 players.
- A publisher (name of the company "owning" the game)

**Main concepts**
- **Select game (title) to create:** This is currently just a list of icons on a row.
- **Create the game:** This is the actual place, where the game is setup. The player should be able to:
    - Give the game a name by chaning the auto-generated name.
  - Select the number of seats - defaulting to the maximum allowed.
  - My own profile will be added to the game per default. However, I can remove myself and create a game for other players (e.g. when hosting a tournament).
  - Easily add other profiles from my account as players.
  - Add friends directly to the game as players.
  - Add search for other users and invite them to the game.
  - Leave spots open for later players.
  - Confirm the creation of the game.
  - Maybe have a "jump right in" action, if all seats are filled with active players (not invites or open seats). This would start and load the game immediately.

![Screen - create new game.png](Screen%20-%20create%20new%20game.png)

## Navigation
### Going "back"
- As we are currently using a classic tree-structured menu system, there should always be a simple way to get "back".
- Once we enter a game, there should still be a "back" option, which will then mean leave game and go back to the menu.

### Sidebar/drawer shortcuts
- We currently have a "burger menu" that expands a drawer menu, with shortcuts to the different sub-menus, and links for changing profile and logging out.

![Screen - drawer menu.png](Screen%20-%20drawer%20menu.png)

## Ads...
At some point, we will most likely need to feature ads in the app and on the portal website. So at some point, we need to consider, where ads can be placed.
- *This is out-of-scope at the moment.*

## The splash / loading screen
Sometimes we choose to show a loading screen. E.g. when downloading an asset pack from the server, which may take a few moments. We can show this with or withour text.

| ![Screen - splash screen.png](Screen%20-%20splash%20screen.png) |
| -- |

# The game
Finally we get to the actual game itself. This is a different Unity scene, meaning that menus, buttons etc. can/will be made separately from the main menu.

![Screen - the game overview.png](Screen%20-%20the%20game%20overview.png)

The user will have two distinct types of interaction with the app, when in a game.
- Interacting with the board game - moving pieces, selecting actions, etc.
- Interacting with the game menu and the features there.

## Interacting with the game
The user will interact with the board game through a set of simple interactions, data at sent from the server as data, and then "drawn" by the client. Examples of actions are:
- Select an item on the board or table.
- Pickup and move an item to a new location.
- Select an action from a special button menu in the right side of the screen - meant to be easily accessible using your thumb on a tablet.

| Action | Example
| -- | --
| Select item | ![Gif - select piece.gif](Gif%20-%20select%20piece.gif)
| Move item | ![Gif - move piece.gif](Gif%20-%20move%20piece.gif)
| Button menu | ![Git - thumb buttons.gif](Git%20-%20thumb%20buttons.gif)

## The game menu
The in-game menu is a bit of a mess right now, but in general a player will have access to the following features.

| Icon | Action
| -- | --
| ![Icon - reload.png](Icon%20-%20reload.png) | Reload the game from server. Should not be needed in the final product, but should be easily accessible during all development versions.
| ![Icon - camera perspective.png](Icon%20-%20camera%20perspective.png) | Change camera from top-down to perspective.
| ![Icon - investigate.png](Icon%20-%20investigate.png) | Open "investigate" overlay, where the user can pick up and investitage certain items.
| ![Icon - replay.png](Icon%20-%20replay.png) | Enter "replay mode", where the user can replay the game up until the current moment.
| ![Icon - timer.png](Icon%20-%20timer.png) | Configure the "timer" functionality - similar to a chess clock.

**Changing background color**
The user is also able to define a background color and "texture" for the client. This menu is a bit technical at the moment.

| ![Screen - example background 1.png](Screen%20-%20example%20background%201.png) | ![Screen - example background 2.png](Screen%20-%20example%20background%202.png)
| -- | --

### A developer menu
In general, we have had very good experience with embedding some developer functionality into the app, as it makes testing and bug-hunting much, much faster. We will be able to distinguish between normal players and developers, so we can "hide" developer functions when needed.

### Some inspiration for a menu
I personally like the way that Tabletopia has made their menu, using a radial popup, as we know from some computer games. Of course, I don't know how well, that would function on a phone.

![TableTopia - radial menu.png](TableTopia%20-%20radial%20menu.png)

## Other contents on the game screen
There are a few more information areas on the game screen.
- **Who's playing:** In the top-right corner, we have some information about you, the user and the game. Username and profile as well and the name of the game is displayed.
  - The logo is currently also displayed here.
  - But what I believe we really need, is information about the other players in the game.

 ![Screen - top-right.png](Screen%20-%20top-right.png)

- **Messages:** In the bottom-left corner we have a "rolling" message box, that shows information about whose turn it is, and what "phase" the game is in. This could also be the place for a future chat function.

![Screen - bottom-left.png](Screen%20-%20bottom-left.png)

## Compeditors

| Name | Pros | Cons | Pricing<sup>‡</sup>
| -- | -- | -- | -- 
| [Board Game Arena](https://boardgamearena.com/) | • Large user base<br>• Rule forcement<br>• Tournaments<br>• Replay games. |• Web only<br>• Simple<br>• graphics<br>• Old-style UX. | 26 $
| [TableTopia](https://tabletopia.com/) | • Stunning graphics<br>• Nice looking UX | • No rule enforment<br>• No tournaments or events. | 100 $
| [Sovranti](https://www.sovranti.com/) | • Rule enforcement<br>• Similar UX but with 3D avatars<br> | • Noisy UX<br>• Technically not very advanced - e.g. load/save games are still in development. |  108 $

‡ The highest license tier paid for a year at a time in US dollars.

### BoardGameArena
**Web portal**

![Pasted image 20211018153733.png](Pasted%20image%2020211018153733.png)

**In-game (replay)**

![Pasted image 20211018153851.png](Pasted%20image%2020211018153851.png)

### Tabletopia
**In-game**

![Pasted image 20211018153535.png](Pasted%20image%2020211018153535.png)

**Web portal**

![Pasted image 20211018153615.png](Pasted%20image%2020211018153615.png)

**Game archive**

![Pasted image 20211018153639.png](Pasted%20image%2020211018153639.png)

### Sovranti
**Create game**

![Pasted image 20211018153224.png](Pasted%20image%2020211018153224.png)

**Lobbye**

![Pasted image 20211018153321.png](Pasted%20image%2020211018153321.png)

**Select environment**

![Pasted image 20211018153425.png](Pasted%20image%2020211018153425.png)

**News section**

![Pasted image 20211018153459.png](Pasted%20image%2020211018153459.png)

**In-game**

![Pasted image 20211018155051.png](Pasted%20image%2020211018155051.png)