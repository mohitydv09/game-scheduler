# Sports League Optimization

This repository contains my Python code for optimizing sports league schedules using Local Search algorithms such as Stochastic Hill Descent and Simulated Annealing algorithms. These algorithms aim to minimize the objective function, which considers factors such as the number of matches between teams, repeated matches, and unplayed matches.

## Algorithms Used

-Stochastic Hill Descent: This algorithm iteratively explores neighboring solutions and moves towards solutions with lower objective function values.  
-Simulated Annealing: Inspired by the annealing process in metallurgy, this algorithm probabilistically accepts worse solutions early in the search but gradually decreases the acceptance probability as the search progresses.

## Problem
We need to schedule weekly games for a board game league. This particular board game is a 4-player game, and you have 13 players in your league. Players are named as A, B, C, D, E, F, G, H, I, J, K, L and M. So, for 13 weeks, each week one player will get a "bye" (that is, not play) and the other 12 players will participate in 3 games (each player playing one game.) The goal is to set a league schedule for 13 weeks, 3 games a week.

## Desired Characteristics
- Each player should play each other player at least once
- Each player should play different opponents as much as possible
- No games with the exact same 4 players should occur, if possible

## Objective Function Graph

![Figure_1](https://github.com/mohitydv09/game-scheduler/assets/101336175/ce0b4d52-3ab0-4e6b-9e0b-ea7dd821f0b8)

## Output

At the end both the algorithm outputted a very good schedule which meet all the deseired characteristics.  
As this is a 4-player game, each line represents the three games for that week. The items in each list of four players are the players participating in a given game.

Final match schedule with Stochastic Hill Descent:

```
Final Node obtained with Hill Decent:
Bye for Player A: ['B', 'I', 'D', 'E'] ['F', 'G', 'K', 'C'] ['J', 'L', 'H', 'M'] 
Bye for Player B: ['L', 'C', 'D', 'F'] ['E', 'G', 'M', 'A'] ['J', 'K', 'I', 'H'] 
Bye for Player C: ['A', 'G', 'D', 'L'] ['F', 'J', 'H', 'E'] ['M', 'K', 'I', 'B'] 
Bye for Player D: ['A', 'K', 'C', 'E'] ['F', 'L', 'H', 'I'] ['J', 'G', 'B', 'M'] 
Bye for Player E: ['J', 'B', 'C', 'D'] ['F', 'G', 'K', 'L'] ['A', 'H', 'I', 'M'] 
Bye for Player F: ['A', 'H', 'C', 'D'] ['L', 'G', 'B', 'I'] ['J', 'K', 'E', 'M'] 
Bye for Player G: ['A', 'B', 'H', 'L'] ['E', 'J', 'C', 'I'] ['D', 'K', 'F', 'M'] 
Bye for Player H: ['M', 'B', 'C', 'F'] ['K', 'A', 'G', 'I'] ['J', 'D', 'L', 'E'] 
Bye for Player I: ['H', 'L', 'C', 'M'] ['D', 'K', 'G', 'J'] ['A', 'F', 'B', 'E'] 
Bye for Player J: ['L', 'B', 'E', 'K'] ['C', 'I', 'G', 'H'] ['F', 'D', 'A', 'M'] 
Bye for Player K: ['M', 'I', 'E', 'D'] ['B', 'F', 'G', 'H'] ['J', 'C', 'L', 'A'] 
Bye for Player L: ['M', 'G', 'C', 'E'] ['D', 'K', 'B', 'H'] ['I', 'J', 'F', 'A'] 
Bye for Player M: ['A', 'B', 'J', 'F'] ['E', 'D', 'G', 'H'] ['I', 'C', 'K', 'L'] 
```

Final match schedule with Simulated Annealing:

```
Final Node with SA:
Bye for Player A: ['B', 'J', 'D', 'E'] ['M', 'G', 'H', 'I'] ['C', 'K', 'L', 'F'] 
Bye for Player B: ['G', 'E', 'D', 'L'] ['F', 'A', 'C', 'M'] ['J', 'H', 'K', 'I'] 
Bye for Player C: ['L', 'B', 'M', 'E'] ['F', 'D', 'H', 'I'] ['J', 'K', 'A', 'G'] 
Bye for Player D: ['A', 'B', 'K', 'C'] ['L', 'E', 'H', 'I'] ['J', 'F', 'G', 'M'] 
Bye for Player E: ['A', 'G', 'C', 'D'] ['F', 'K', 'J', 'I'] ['H', 'B', 'L', 'M'] 
Bye for Player F: ['A', 'B', 'K', 'H'] ['G', 'C', 'I', 'L'] ['D', 'E', 'J', 'M'] 
Bye for Player G: ['H', 'E', 'C', 'J'] ['L', 'F', 'A', 'I'] ['K', 'D', 'B', 'M'] 
Bye for Player H: ['I', 'L', 'C', 'D'] ['E', 'B', 'G', 'A'] ['J', 'K', 'F', 'M'] 
Bye for Player I: ['H', 'G', 'M', 'L'] ['D', 'E', 'K', 'A'] ['J', 'C', 'B', 'F'] 
Bye for Player J: ['A', 'L', 'C', 'H'] ['E', 'F', 'K', 'G'] ['I', 'B', 'M', 'D'] 
Bye for Player K: ['F', 'H', 'C', 'D'] ['E', 'A', 'I', 'M'] ['B', 'J', 'G', 'L'] 
Bye for Player L: ['A', 'H', 'D', 'J'] ['I', 'F', 'G', 'B'] ['C', 'K', 'E', 'M'] 
Bye for Player M: ['K', 'B', 'C', 'D'] ['E', 'F', 'G', 'H'] ['I', 'J', 'A', 'L'] 
```
