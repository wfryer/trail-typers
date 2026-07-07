# Trail Typers

An Oregon Trail themed typing race in a single HTML file. Players race covered wagons 2,040 miles from Independence, Missouri to Oregon City by typing sentences quickly and accurately. A remix of [typing-bee](https://github.com/wfryer/typing-bee), rebuilt so it needs no Python server, no installation, and no admin rights.

## How to run it

Download `index.html` and double-click it. That is the whole setup. It works on any PC, Mac, or Chromebook with a modern browser (Chrome, Edge, Firefox, or Safari) and a physical keyboard.

## Game modes

**1. Solo practice.** Pick a difficulty and a round length, then type your way west. Best runs are saved on that computer. Solo mode works offline.

**2. Host a wagon train.** The host (a teacher on a projector, or any player) gets a 4 letter room code. The host can play too, or run a projector-only view of the race. The host controls difficulty, round length, and when each round starts.

**3. Join a wagon train.** Everyone else opens the same file on their own computer, chooses Join, and enters the room code. No accounts, no logins, just a first name.

## How the race works

- Every correct character pulls your wagon west. Wrong keys flash red and do not move you, so accuracy matters as much as speed.
- The trail passes real landmarks: Fort Kearny, Chimney Rock, Fort Laramie, Independence Rock, South Pass, Fort Hall, Fort Boise, and the Blue Mountains.
- Reach Oregon City before time runs out to finish the trail. If nobody finishes, the farthest wagon wins the round.
- Live WPM, accuracy, and miles are shown during the race, and full standings appear at the end of each round.
- Everyone types the identical sentence list in the same order, so the race is fair.

## Custom sentences

Choose **Edit custom sentences** and paste your own, one per line (spelling words, vocabulary, content review questions, anything). They are saved in the browser. When the host picks the Custom difficulty, the host's sentences are automatically sent to every player, so only the host needs to set them up.

## How multiplayer works with no server

Multiplayer uses WebRTC through [PeerJS](https://peerjs.com) and its free public broker. The broker only introduces the computers to each other; after that, game data flows directly between the host and each player. Nothing is stored anywhere, and there is no backend to maintain.

## Troubleshooting

- **Multiplayer needs the internet** on every computer, both to load PeerJS and to connect players. Solo practice works offline.
- **School firewalls** sometimes block WebRTC or UDP traffic. If players cannot connect at school, try solo mode, or test on a different network first.
- **"Could not find that wagon train"** usually means a mistyped code (codes never contain 0, O, 1, or I), or the host closed the lobby.
- Scores, names, and custom sentences are saved in the browser's local storage on each computer, not online.
- Sound and the CRT scanline effect can be toggled with the buttons in the top right corner. The CRT effect is automatically disabled for users who prefer reduced motion.

## Roadmap

- Team mode: wagons grouped into teams with combined mileage. The player data model already carries a team field, so this is the natural next remix.
- More sentence packs (states and capitals, science vocabulary, quotes).

## Credits

Built as a remix of [typing-bee](https://github.com/wfryer/typing-bee) by Wes Fryer. Trail landmarks and distances are based on the historic Oregon Trail route. The green phosphor look is a tribute to the classroom computer games of the 1980s.
