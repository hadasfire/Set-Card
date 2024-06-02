# Set-Card

Implemented a Set card game in Java using concurrent programming techniques, demonstrated a strong understanding of Java Threads and Java Synchronization concepts, Utilized unit testing to ensure the correctness and reliability of the game implementation.

This project was made on my Second year in Ben Gurion University as a student in "Systems Programming" course.

# Instructions
The game contains a deck of 81 cards. Each card contains a drawing with four features (color, number, shape, shading).
The game starts with 12 drawn cards from the deck that are placed on a 3x4 grid on the table.
The goal of each player is to find a combination of three cards from the cards on the table that are said to make up a “legal set”.

A “legal set” is defined as a set of 3 cards, that for each one of the four features — color,
number, shape, and shading — the three cards must display that feature as either: (a) all the
same, or: (b) all different (in other words, for each feature the three cards must avoid having
two cards showing one version of the feature and the remaining card showing a different
version).

The possible values of the features are:

▪ The color: red, green or purple.

▪ The number of shapes: 1, 2 or 3.

▪ The geometry of the shapes: squiggle, diamond or oval.

▪ The shading of the shapes: solid, partial or empty.

The game's active (i.e., initiate events) components contain the dealer and the players.
The players play together simultaneously on the table, trying to find a legal set of 3 cards. They do so by placing tokens on the cards, and once they place the third token, they should ask the dealer to check if the set is legal. If the set is not legal, the player gets a penalty, freezing his ability of removing or placing his tokens for a specified time period. If the set is a legal set, the dealer will discard the cards that form the set from the table, replace them with 3 new cards from the deck and give the successful player one point. In this case the player also gets frozen although for a shorter time period.
To keep the game more interesting and dynamic, and in case no legal sets are currently available on the table, once every minute the dealer collects all the cards from the table, reshuffles the deck and draws them anew.

The game will continue as long as there is a legal set to be found in the remaining cards (that are either on table or in the deck). When there is no legal set left, the game will end and the player with the most points will be declared as the winner!

Each player controls 12 unique keys on the keyboard as follows. The default keys are:
<img width="497" alt="image" src="https://github.com/hadasfire/Set-Card/assets/130358405/5b02c8c4-e56a-4baa-8287-2486dcc97700">

The keys layout is the same as the table's cards slots (3x4), and each key press dispatches the respective player’s action, which is either to place or remove a token from the card in that slot - if a card is not present/present there.

The game supports 2 player types: human and non-human. The input from the human players is taken from the physical keyboard as an input. The non-human players are simulated by threads that continually produce random key presses.

# Getting Started

Clone this repository to your local machine. 

Go to "src/main/java/bguspl/set/Main.java" and start the game.
