# Rocket League Custom Overlays
Personal project made for enhancing streaming experience during self-organised Rocket League tournaments by showing custom-made overlays on stream instead of the ingame HUD.

This project requires [BakkesMod](https://www.bakkesmod.com/) with the [SOS-Plugin](https://gitlab.com/bakkesplugins/sos/sos-plugin) installed on your computer + [SOS WS Relay](https://gitlab.com/bakkesplugins/sos/sos-ws-relay) & [move.js](https://github.com/visionmedia/move.js/) folders at the root of this project to work properly. Fonts must also be installed from the "fonts" folder of this project.

Even if both old and new overlays were used during self-organised showmatches and tournaments, the project was initialised back in 2020 as an extracurricular project to learn JavaScript, so it is **NOT INTENDED** for professionnal purposes.

## Features :
- **Overlays :** displays ingame informations such as timer, players stats (goals, assists, boost amount, etc.), players events feed (saves, shots, demolitions, etc.), team names (automatically retrieved from the ingame server), endgame recap.
- **2D mini-map :** displays all the players and the ball at anytime of the game
- **Adaptable overlays with series length :** the project contains 3 variants of the overlay depending on the length of the series (best of 3, best of 5 and best of 7). It also keeps tracking of the amount of wins per team during the series, which is displayed under the teams names.

## How to install :
- Once [BakkesMod](https://www.bakkesmod.com/) is installed with the [SOS-Plugin](https://gitlab.com/bakkesplugins/sos/sos-plugin), clone this repo anywhere on your computer.
- Clone [SOS WS Relay](https://gitlab.com/bakkesplugins/sos/sos-ws-relay) & [move.js](https://github.com/visionmedia/move.js/), create folders respectively named "sos-ws-relay-master" and "move.js-master" at the root of this project and drop all their files inside those 2 new folders.
- Your RocketLeagueCustomOverlays folder must now look like this :
├── drops
├── fonts
├── icons
├── move.js-master
│   ├── (all files from [move.js](https://github.com/visionmedia/move.js/) clone)
├── newOverlay
├── oldOverlay
├── sos-ws-relay-master
│   ├── (all files from [SOS WS Relay](https://gitlab.com/bakkesplugins/sos/sos-ws-relay) clone)
└── README.md

## How to use :
- Launch BakkesMod and Rocket League
- Once inside the game, press F2 to open the BakkesMod settings, go to *Plugins > SOS-Overlay System* and make sure the rate is set at the lowest possible (which should be 15)
- Open a command prompt inside the *sos-ws-relay-master* folder, and type in "node ws-relay", press "Enter" 3 times. You should now see "*Connected to Rocket League on localhost:49122*".
- Open your streaming software (like OBS Studio for example), and add either of the new or old and/or the minimap overlays. Resize the overlays to fill all the screen, for the minimap resize and place it as you wish. Make sure they all are above the game source.
- Inside Rocket League, create a new lobby and write the team names on the settings of the lobby, it will automatically write them on the top pannels of the overlay. Once a game starts, press twice "H" to make sure the ingame HUD disappears.
- Enjoy !