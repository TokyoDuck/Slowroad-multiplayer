# Slow Roads Multiplayer Extension

## Overview

Slow Roads Multiplayer is a browser extension that adds online multiplayer functionality to Slow Roads.

Players can create rooms, invite friends, and drive together in the same world. The extension injects into the game, synchronizes player positions, and renders other players in real time.

## Core Features

### Room System
- Create private rooms
- Join rooms using room codes
- Copy room invite codes
- Display connected players

### Multiplayer Synchronization
- Sync player position
- Sync vehicle rotation
- Sync vehicle type
- Sync speed
- Sync world seed

### Friend Visibility
- Show nearby players
- Display usernames above vehicles
- Smooth movement interpolation
- Player join/leave notifications

### User Interface
- Multiplayer button inside Slow Roads
- Room browser
- Player list
- Connection status indicator

## Technical Requirements

### Extension
- Chrome Manifest V3
- Content scripts
- Background service worker
- Popup UI

### Networking
- Firebase Realtime Database or WebSocket server
- Real-time position updates
- Automatic reconnect support

### Game Integration

The extension must:

1. Detect when Slow Roads loads
2. Access the game scene
3. Access vehicle position data
4. Inject multiplayer vehicles
5. Render remote players in the world

### Synchronization Data

Each player should broadcast:

json {   "username": "Harry",   "vehicle": "Coupe",   "x": 0,   "y": 0,   "z": 0,   "rotation": 0,   "speed": 0,   "timestamp": 0 } 

## UI Layout

### Popup

text --------------------------------  Slow Roads Multiplayer --------------------------------   Username  [____________]   Room Code  [____________]   [ Create Room ]  [ Join Room ]   Players Online: 0 -------------------------------- 

### In-Game Overlay

text --------------------------------  Room: ABC123   Players:  Harry  Alex  Sam -------------------------------- 

## Development Goal

The finished extension should allow multiple users to join the same room and see each other driving live inside Slow Roads with minimal latency.

The user experience should feel similar to multiplayer driving games while preserving the relaxing nature of Slow Roads.
