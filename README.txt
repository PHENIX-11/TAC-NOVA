TAC//NOVA — V3.2 ONLINE SYNC + RECONNECT PATCH

INSTALL / DEPLOY
1. Extract this ZIP into a fresh folder.
2. Upload the contents of the inner tac_nova folder (index.html, style.css, script.js, README.txt) to the ROOT of your GitHub repository, replacing the previous files.
3. Commit the changes to the main branch and wait for GitHub Pages to finish deploying.
4. Both players must open the same HTTPS site URL. Do not use a local file:// URL for online play.

ONLINE ROOM PLAY
1. Both players open ARENA > ONLINE ROOM.
2. Player One selects CREATE ROOM and waits for ROOM READY.
3. Player One copies the temporary Room ID and shares it with Player Two.
4. Player Two pastes the Room ID and selects JOIN ROOM.
5. Player One plays X; Player Two plays O.
6. Keep both tabs open while playing. If a player disconnects, the host should keep the room tab open; the guest can retry joining with the same Room ID if the host room is still active.

V3.2 FIXES
- Host now sends an authoritative full-board state after its move.
- Guest move requests are validated and applied by the host, then the host broadcasts the updated state to both players.
- Winning/draw state is included in synchronization.
- Closed/error connections clear the stored connection reference, so the host can accept a fresh connection instead of rejecting every later join attempt.
- Connection and send errors show clearer status messages.

IMPORTANT LIMITATIONS
- Online mode uses PeerJS for signaling and WebRTC for the direct game connection. PeerJS loads from the unpkg CDN and requires internet access.
- Some routers, school/work networks, VPNs or firewalls block direct WebRTC. Those networks may require a TURN relay server; this build does not include a dedicated TURN service.
- The room ID is temporary and exists only while the host's browser session remains connected. The permanent TN player ID is local profile identity, not the room address.
- This version has not been live-tested between two separate devices in different networks. JavaScript syntax and ZIP integrity are checked; test on two devices after deployment.
