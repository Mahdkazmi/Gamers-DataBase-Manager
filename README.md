# Gamers-DataBase-Manager
Gamers Database Manager
Overview
This project, Gamers Database Manager, was developed as an assignment for the Data Structures course (Fall 2024) at FAST NUCES. It’s designed to manage a dataset of players and the games they play, providing functionality to add, search, delete, and display information about players and their gaming records through a console interface.

# Objective
The objective of this project is to create a console-based database management system (DBMS) that handles specific queries efficiently using data structures like Binary Search Trees (BST). This DBMS stores players and games, enabling quick access and management of records.

# Project Structure
PlayerNode Class - Stores player details such as playerId, name, phoneNumber, email, password, and a linked list of games played.
GamesPlayed Class - Represents each game a player has played, including gameId, hoursPlayed, and achievementsUnlocked.
PlayerTree Class - A BST to store and manage PlayerNode instances.
GameNode and GameTree Classes - Structures to manage game data in a BST, enabling insertion, deletion, and search operations on games.
# Setup
Dataset Files:

Games.txt - Contains the dataset of games (required format: Id, name, developer, publisher, size, downloads).
Players.txt - Contains the dataset of players (required format: playerId, name, phoneNumber, email, password).
Compilation:

# Compile the code using a C++ compiler:
g++ main.cpp -o GamersDB

# Run the program from the console:
./GamersDB


Loads player and game data from the CSV files, storing them in BSTs. The data can be skipped based on a random seed using a unique roll number formula.
Insertion:

New player and game records can be inserted into their respective BSTs, checking for primary key conflicts.
Search and Retrieval:

Supports searching by primary key (playerId or gameId) and displaying the corresponding node information.
Deletion:

Removes any player or game entry from the BST, ensuring memory is freed.
Save Data:

Saves player and game data back to CSV files using a preorder traversal of the BSTs.
Show N Layers:

Displays the first N layers of the BST for both players and games. If N exceeds the total layers, a warning message is shown.
Show Layer Number:

Finds and returns the layer number of a node based on its primary key.
Show Path to Node:

Shows the traversal path to find a specific node, aiding in debugging and understanding the BST structure.
Edit Entry:

Allows editing any entry's data, including primary keys, and repositions the node in the BST if needed.
Top N Players:

Displays the top N players who have played the most games.
Show Player and Game Details:

Allows displaying a player’s details along with all games they have played.
Has Played:

# Thought Process and Logic
The following decisions were made to ensure an efficient, dynamic, and extendable codebase:


Dynamic Allocation: The code uses dynamic memory allocation for nodes to ensure memory efficiency and scalability.
Linked List for Games Played: Each player has a linked list of GamesPlayed nodes, enabling efficient addition and iteration over games without relying on built-in data structures.
Modular Functions: Each functionality, such as adding games to players or checking if a game was played, was designed as a modular function to make the code easy to maintain and extend.
