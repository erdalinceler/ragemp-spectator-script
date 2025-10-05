# Spectator Script

A comprehensive spectator script for RageMP, allowing players to observe other players in real-time.

## Features

- **Seamless Spectating**: Switch between players with smooth camera transitions
- **Vehicle Support**: Automatically follows players whether on foot or in vehicles
- **Distance Management**: Maintains optimal viewing distance with automatic repositioning
- **Player State Management**: Handles spectator visibility and collision states
- **Automatic Cleanup**: Stops spectating when target player disconnects
- **Position Restoration**: Returns players to their original position when spectating ends

## Commands

- `/spectate [player_id]` - Start spectating a specific player
- `/spectate off` - Stop spectating and return to original position

## Architecture

### Client-side (`client/index.js`)

- Handles camera control and visual effects
- Manages spectator state and target tracking
- Implements smooth following with distance checks
- Processes entity streaming for spectator visibility

### Server-side (`server/index.js`)

- Manages spectator commands and validation
- Tracks player positions and states
- Handles spectator session cleanup
- Synchronizes spectator status across clients

## Installation

1. Place `client/index.js` in your client-side scripts directory
2. Place `server/index.js` in your server-side scripts directory
3. Ensure proper event handling is configured in your environment

## Usage

Players can use the `/spectate` command followed by a target player ID to begin spectating. The system automatically handles camera positioning, collision states, and cleanup when spectating ends.

## Requirements

- RageMP server and client environment
- Player entity management system

## Resources

- [RageMP Official Wiki](https://wiki.rage.mp) - Complete documentation for RageMP API and features
- [Client-side Events](https://wiki.rage.mp/wiki/Client-side_events) - Client event reference
- [Client-side Functions](https://wiki.rage.mp/wiki/Client-side_functions) - Client function reference
- [Server-side Events](https://wiki.rage.mp/wiki/Server-side_events) - Server event reference
- [Server-side Functions](https://wiki.rage.mp/wiki/Server-side_functions) - Server function reference
