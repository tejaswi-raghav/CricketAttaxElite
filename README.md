Cricket Attax Elite – Professional Edition
A Java Swing–based strategy card game inspired by cricket statistics and Top Trumps–style gameplay. Players compete using cricket player cards and select statistical categories to defeat their opponent’s card.
This project demonstrates object-oriented design, AI strategy patterns, observer pattern, and state-driven game logic within a polished desktop GUI.
 
Features
Gameplay
Card-based cricket strategy game
Each card represents a professional cricket player
Players select a statistic category to challenge the opponent
The card with the better value wins the round
Winner collects both cards (and any cards in the prize pile)
Player Statistics
Each card includes:
Batting Average
Strike Rate
Bowling Wickets
Economy Rate
Fielding Catches
Experience (Years)
Some stats reward higher values, others reward lower values (e.g., economy rate).
 
AI Opponent
The game supports AI vs Computer mode with multiple strategies:
Easy Mode
Uses a Random Strategy
Selects any stat randomly
Hard Mode
Uses Max Advantage Strategy
Chooses the stat giving the best competitive advantage
AI decision logic is implemented using the Strategy Design Pattern.
 
 Game Architecture
The project follows strong software engineering principles.
Design Patterns Used
Pattern	Purpose
Singleton	 Ensures a single GameEngine instance
Strategy Pattern	 AI decision-making strategies
Observer Pattern	 UI updates when game state changes
State Pattern	 Manages game turn phases
Factory Pattern	 Creates player cards from data
 
Core Components
Game Engine
GameEngine
Responsible for:
Managing decks
Handling turns
Determining round winners
Updating scores
Saving high scores
Notifying observers (UI)
 
Card System
Interface
Card
Defines methods like:
getPlayerName()
getPlayerType()
getStat()
Implementation
ElitePlayerCard
Stores:
player name
player type
stat values
 
Deck Manager
Handles:
Shuffling cards
Dealing cards to players
Cards are loaded from:
playerstats.csv
(Default player data is embedded in the code.)
 
Game States
The game flow is controlled using state objects:
SelectionState
ComparisonState
ResolutionState
GameOverState
Turn Flow
Select Stat
      ↓
Compare Cards
      ↓
Resolve Winner
      ↓
Next Turn
 
 GUI
The game uses Java Swing with a modern custom interface.
UI Features
Glass-style panels
Custom buttons
Animated turn transitions
Card displays
Match history
Score tracking
Screens
 Start Screen
 Game Screen
 End Screen
 
 Player Types
Cards belong to different cricket roles:
Batsman
Bowler
All-Rounder
Wicketkeeper
These types provide stat modifiers during comparisons.
Example:
Stat Type	Bonus
Batting stats	+25% for batsmen
Bowling stats	+25% for bowlers
 
Data Storage
The game stores data locally:
File	Purpose
highscores.dat	Top 10 scores
matchhistory.dat	Match history
High scores are ranked by lowest number of turns to win.
 
How to Run
Requirements
Java JDK 8 or later
 
Compile
javac CricketAttaxElite.java
 
Run
java CricketAttaxElite
 
Game Rules
1.	Each player starts with 11 cards
2.	Current player selects a stat category
3.	Both cards are compared
4.	Winner takes the cards
5.	If tied: Cards go into the Prize Pile
6.	Winner of next round takes all pile cards
Game ends when one player runs out of cards.
 
Example Players
The game includes real cricket players such as:
Virat Kohli
Rohit Sharma
Babar Azam
Ben Stokes
Kane Williamson
Rashid Khan
Steve Smith
Each card contains realistic statistical attributes.
 
Technologies Used
Java
Java Swing
Object-Oriented Programming
Serialization
Event-driven GUI
 
Educational Value
This project demonstrates:
Advanced OOP architecture
Design patterns in practice
GUI development with Swing
AI behavior implementation
Game state management
 
Author
Tejaswi Raghavendra Banda



