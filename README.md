# Monopoly Game Implementation

A C++ implementation of the classic Monopoly board game with SFML graphics.

## 🎮 Game Overview

This is a fully functional Monopoly game that includes all the classic gameplay mechanics: property buying, rent collection, chance cards, jail system, and bankruptcy rules. The game features a graphical interface built with SFML and supports multiple players.

## 🏗️ Architecture

### Core Classes

#### **Player**
- Simple constructor that can only be instantiated within a game context
- Tracks player position, money, and owned properties
- Handles player movement and financial transactions

#### **Block System**
The game board consists of different types of blocks, each with specific properties:

**Base Block Class:**
- Contains pixel coordinates for visual rendering
- Has placement number, name, and type identifier

**Property Block:**
- Extends base block with rent and purchase price
- Handles property ownership and rent collection

**Company Block:**
- Contains purchase price only
- Rent varies based on dice roll and ownership

**Chance Block:**
- Represents "Treasure" and "Chance" special squares
- Triggers random card events

**General Block:**
- Handles special squares: "Jail", "Go to Jail", "Free Parking", "Go"
- Implements special game rules for each square type

#### **Board**
- Manages SFML graphics and visual rendering
- Monitors property ownership changes and visual updates
- Handles player movement animations
- Updates display when properties are purchased or developed
- Manages player elimination and property redistribution

#### **Gameplay**
- Central game engine that orchestrates all game mechanics
- Creates and initializes board and players
- Implements main game loop until victory condition is met
- Handles turn-based gameplay mechanics

### Game Features

- **Jail System**: Complete implementation of jail rules and bail mechanics
- **Free Parking**: Special square with parking rules
- **Chance & Treasure Cards**: Random event cards that affect gameplay
- **Property Management**: Buy, sell, and collect rent from properties
- **Company Ownership**: Special utility properties with variable rent
- **Bankruptcy System**: Handles player elimination and asset redistribution
- **Victory Conditions**: Game ends when only one player remains or a player reaches $4000

## 🚀 Getting Started

### Prerequisites
- C++ compiler with C++11 support or later
- SFML library installed
- Make utility

### Building the Game

```bash
# Build the game
make

# Run the main game
make run_main

# Run tests
make run_test

# Clean build files
make clean
```

### Running the Game

After building, simply run:
```bash
make run_main
```

The game will launch with a graphical interface where you can play with multiple players.

## 🧪 Testing

The project includes comprehensive tests covering:
- Core game mechanics
- Edge cases and boundary conditions
- Property transactions
- Player elimination scenarios
- Victory condition validation

Run tests with:
```bash
make run_test
```

## 🎯 Game Rules

### Victory Conditions
- Last player remaining wins
- First player to reach $4000 wins

### Key Mechanics
- Players take turns rolling dice and moving around the board
- Landing on unowned properties allows purchase
- Landing on owned properties requires rent payment
- Special squares trigger various effects
- Players can go bankrupt and be eliminated
- Properties transfer between players or return to the bank upon bankruptcy

## 🔧 Technical Details

- **Graphics**: SFML for 2D rendering and window management
- **Memory Management**: Proper cleanup and memory release on game termination
- **Player Management**: Dynamic player vector with safe removal during gameplay
- **Property Visualization**: Real-time updates showing ownership changes

## 📁 File Structure

- `main.cpp` - Entry point for the game
- `test.cpp` - Comprehensive test suite
- `Gameplay.*` - Core game logic and mechanics
- `Board.*` - Graphics and visual management
- `Player.*` - Player class implementation
- `Block.*` - Various block type implementations

## 🤝 Contributing

Feel free to submit issues and enhancement requests!

## 📧 Contact

**Developer**: kkorenn1@gmail.com
