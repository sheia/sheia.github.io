---
layout: post
title:  "Welcome to Jekyll!"
date:   2020-07-09 23:26:46 +0530
categories: jekyll update
---


![alt text](https://images.pexels.com/photos/355952/pexels-photo-355952.jpeg?cs=srgb&dl=analysis-blackboard-board-bubble-355952.jpg&fm=jpg)



# Introduction to Artificial Intelligence - Part 1

In this series, I would be exploring, at a high level, some ideas, techniques and algorithms that are at the foundation of AI. AI covers a wide range of techniques and in this series I would be covering the following categories of problems:

1.	**Search** – searching for a problem, for example driving directions from point A to point B
2.	**Knowledge** – making inferences given some information
3.	**Uncertainty** – dealing with uncertain events
4.	**Optimization** – locates the best option among a possible set of solutions 
5.	**Learning** – being able to perform a task by learning from data
6.	**Neural Networks** – drawing inspiration from human intelligence
7.	**Language** – understanding natural language 

In this post, I would be talking about Search and Knowledge.

## 1. Search

![alt text](https://images.pexels.com/photos/814133/pexels-photo-814133.jpeg?cs=srgb&dl=white-chess-piece-on-top-of-chess-board-814133.jpg&fm=jpg)

> Search problems are those where the computer tries to figure out what to do when in a particular situation. 

##### *Examples*
These problems can come in many different types of formats. Some examples are:
- Navigating through a maze to travel from an initial state to a final goal
- Finding driving directions from point A to point B
- Playing games such as Tic-Tac-Toe, Chess, etc.

##### *Approach*

The algorithms that are commonly used for solving classical search problems are [Depth-first search](https://en.wikipedia.org/wiki/Depth-first_search), [Breadth-first search](https://en.wikipedia.org/wiki/Breadth-first_search), [Greedy Best First search](https://www.geeksforgeeks.org/best-first-search-informed-search/) and [A* search](https://en.wikipedia.org/wiki/A*_search_algorithm).

Adversarial search is where the agent is trying to make intelligent decision and there is someone else such as an opponent who has the opposite objective and trying to win the game for itself. A popular example of this would be a game of Tic-Tac-Toe. 

[Minimax](https://www.educative.io/edpresso/the-minimax-algorithm?affiliate_id=5082902844932096&utm_source=google&utm_medium=cpc&utm_campaign=platform2&utm_content=ad-1-dynamic&gclid=EAIaIQobChMI2oeQlc7A6gIVGg4rCh0GWQLxEAAYASAAEgIrfvD_BwE) is an algorithm that can be used to solve adversarial search problems. The algorithm evaluates the various moves the opponent could take in a particular situation and determines the optimal move to make to win the game.

In a simple game such as Tic-Tac-Toe, it is possible to evaluate all the possible moves of the opponent but when it comes to more complex games such as Chess, it is computationally intractable to evaluate all the possible options. This is where optimization methods to estimate the optimal move without having to actually compute all the alternatives become important. [Evaluation function](https://en.wikipedia.org/wiki/Evaluation_function) is one such method. How good the AI is at playing a game would ultimately depend on how good the evaluation function is at estimating how good or bad a particular game state is.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       

## 2. Knowledge 
![alt text](https://images.pexels.com/photos/262488/pexels-photo-262488.jpeg?cs=srgb&dl=black-and-white-blank-challenge-connect-262488.jpg&fm=jpg)

> Knowledge problems are those where the computer makes inferences or deductions based on the facts and logical reasoning. 

##### *Examples*

Consider the following statements. 

- If it didn’t rain, Harry visited Hagrid today.
- Harry visited Hagrid or Dumbledore today, but not both. 
- Harry visited Dumbledore today.

From these statements, AI will derive the following:

- *Harry did not visit Hagrid today.*
- *It rained today.*

Applications include playing games such as Clue, Mastermind, etc. and solving logical puzzles.

##### *Approach*

Knowledge Engineering is the process of encoding these facts and logic in AI, making AI logical so they can do the same kind of reasoning and deductions. 

[Model Checking](https://en.wikipedia.org/wiki/Model_checking) is an algorithm behind the scenes. The idea is to encode all the statements using [Propositional Logic](http://discrete.openmathbooks.org/dmoi2/sec_propositional.html) and apply Model Checking to make deductions.

Another approach is to convert all the statements to [Conjunctive Normal Form](https://en.wikipedia.org/wiki/Conjunctive_normal_form) by using Inference Rules. Then we can apply Inference by Resolution to solve the puzzle. [First-Order Logic](https://en.wikipedia.org/wiki/First-order_logic) is another algorithm ideal for complex logical puzzles.

## 3. Uncertainty
![alt text](https://images.pexels.com/photos/705171/dice-eyes-luck-game-705171.jpeg?cs=srgb&dl=pair-of-white-dice-on-top-of-mirror-705171.jpg&fm=jpg)

In the context of Knowledge problems, the computer made conclusions based on some known facts. We can apply the same idea to probability. 

>Uncertainty problems are those where the AI predicts the probability of variables taking on particular values, by using known information, whether it is some evidence or some probabilities. 

##### *Examples*
Suppose I have an appointment to for which I need to take the train. Whether I make it on time to the appointment or not depends on the train schedule. The train may be on time or delayed depending on whether it is raining and whether there is track maintenance. Track maintenance is also depending on the rain. 

##### *Approach*

By modeling these nodes in a [Bayesian network](https://towardsdatascience.com/introduction-to-bayesian-networks-81031eeed94e), we can program the AI to predict the probability of being able to attend an appointment. 

Another example would be to predict today’s weather, using the previous day’s weather and applying the [Markov assumption theory](https://www.igi-global.com/dictionary/markov-assumption/37576).

## 4. Optimization


![alt text](https://images.pexels.com/photos/408503/pexels-photo-408503.jpeg?cs=srgb&dl=blur-cartography-close-up-concept-408503.jpg&fm=jpg)


> Optimization problems are about choosing the best option from a set of options.

##### *Examples*

- The travelling salesman problem – determining the shortest route a salesman could take
- The ideal location for a hospital – deciding where a hospital should be located so that it is the least distance from a certain number of houses
- Optimizing production and costs – deciding which crops to farm depending on the cost, effort and returns.
- Satisfying certain constraints – solving a Sudoku puzzle or scheduling exams such that certain subjects don’t fall on the same day


##### *Approach*

There are a number of ways we can formulate these problem. Some approaches are given below.

i)	Local search problem -  where we’re looking at a current node and moving to a neighbor based on whether the neighbor is better or worse than the current node we are looking at.
Algorithms - [Hill-climbing](https://en.wikipedia.org/wiki/Hill_climbing) and [Simulated Annealing](https://www.mathworks.com/help/gads/what-is-simulated-annealing.html)

ii)	Linear programs – where we formula the problem in the form of equations and constraints
Algorithms - [Simplex algorithm](https://en.wikipedia.org/wiki/Simplex_algorithm) and [Interior-point algorithm](https://en.wikipedia.org/wiki/Interior-point_method)

iii)	Constraint satisfaction problem – creating a graph of all the constraints that connect to variables that have constraints between them
Algorithms - [Enforcing arc consistency](https://en.wikipedia.org/wiki/Local_consistency) and [Backtracking search](https://www.tutorialspoint.com/introduction-to-backtracking)


---


I would be covered the other AI problems types in subsequent posts in this series. Stay Tuned !

*Reference:* [CS50's Introduction to Artificial Intelligence with Python](https://courses.edx.org/courses/course-v1:HarvardX+CS50AI+1T2020/course/)

