TAC//NOVA — V3.0 PLAYER IDENTITY + ONLINE ROOMS

RUNNING THE GAME
1. Extract the ZIP into a folder.
2. For local play, open index.html in a modern browser.
3. For online multiplayer, run the site from localhost or host it on an HTTPS website. Do not open the file directly for online play.

LOCAL PLAYER PROFILE
- On first launch, TAC//NOVA creates a local player ID (TN-XXXXXX).
- Open the profile icon to edit display name, avatar sigil and profile energy colour.
- The profile ID is stored only in this browser. It is not an account login and does not contain personal information.
- Use the profile ID as your player identity; it is not the online room address.

FIRST-TIME TUTORIAL
- A tutorial opens automatically the first time this browser runs the game.
- Reopen it at any time with HOW TO PLAY on the home screen.

ONLINE ROOM MULTIPLAYER
1. Both players open the same TAC//NOVA website using a modern browser and internet access.
2. Both select ARENA > ONLINE ROOM.
3. Player One selects CREATE ROOM and waits for ROOM READY.
4. Player One copies the temporary Room ID and shares it with Player Two.
5. Player Two pastes the Room ID and selects JOIN ROOM.
6. Player One uses X; Player Two uses O. Moves are synchronized over a WebRTC data connection.
7. Either player can leave the room using LEAVE ONLINE ROOM.

NETWORK REQUIREMENTS / LIMITATIONS
- Online mode uses PeerJS for signaling and WebRTC for the direct game connection. It requires internet access and loads PeerJS from the unpkg CDN.
- The room ID is temporary and changes when a new room is created. The permanent TN profile ID is not used to connect a match.
- For online play, serve the files over HTTPS or localhost. Example on a computer with Python installed: open a terminal in this folder and run `python -m http.server 8000`, then open `http://localhost:8000` on that same computer. For friends on different networks, publish the folder to an HTTPS static host.
- Some restrictive networks/firewalls may block direct WebRTC connections. A TURN relay server may be needed for those networks; this starter build does not include a paid TURN service.
- This build has no central account database, chat, or cloud profile sync. Player profile and records remain in each browser.
- Use a nickname, not a real full name or contact details.

FEATURES RETAINED
- Local two-player and AI play; 3x3, 4x4 and 5x5 grids.
- Custom X/O glyphs and colours, themes, board styles and glow settings.
- Win-line strike, sparkles, celebration splash, synthesized fanfare and screenshot export.
- Local stats, history, undo and rematch.

TESTING NOTE
JavaScript syntax and ZIP integrity are checked. Real multiplayer requires testing from two separate browsers/devices over an HTTPS-hosted build; network behavior can vary by firewall and NAT.
