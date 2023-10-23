# Q_Training_Algorithm--Pathfinding

## How the Intelligent Agent Works
The intelligent agent works by interacting with its environment (the maze), making decisions (actions) based on either exploration (random directional choice) or exploitation (using predictions from the trained model). It uses the Q-learning algorithm to maximize the expected cumulative reward over time by choosing the most optimal actions that lead to the most rewarding outcomes (Watkins, 1989). 
## Taking a look at the Algorithm
Q-learning is a type of reinforcement learning algorithm that is used to find the most optimum action selection policy for a given finite Markov decision process (Watkins, 1989). It learns an action-value function which leads to the agent taking a given action in a particular state and then following the optimal policy. 
It can handle problems with stochastic transitions and rewards without requiring adaptations. It is off-policy which means that it learns the value of the optimal policy independent of the agent’s actions. 
A basic Q-learning algorithm may be slow to converge. This is the reason that deep Q-learning is used with neural networks as it can generalize across states to speed up the learning process (Mnih et al., 2013). 
## Human vs. Machine Approach to Solving the Problem
Humans would first observe and visually process the maze. They might recognize patterns in the maze based on prior knowledge or experience. They will try out different paths, fail, remember dead-ends, and try to avoid these in their future attempts. Over time, they might develop a strategy to solve the problem (like always turning left or using wall following methods).
A machine learning agent will start at a random free cell and observe the state of the maze. It will then choose an action based on either exploration (random choice) or exploitation (model’s prediction). After taking the action, the agent will receive a reward or penalty and updates its knowledge (Q-values). It trains a neural network to approximate the Q-function. This process will be repeated over numerous episodes to refine the agent’s policy.
Both humans and the agent would use trial and error, and both will refine their strategies over time based on given feedback. However, humans rely on intuition, prior knowledge, and visual interpretation to solve the problem, while the agent uses a learned policy from interacting with the environment. Additionally, the agent’s decisions are automatically optimized to maximize the expected rewards (Mnih et al., 2013). 
## The Purpose of the Intelligent Agent in Pathfinding
Pathfinding is the act of navigating through a space to find the optimal path from a start to an endpoint. The purpose of the agent in pathfinding is to autonomously learn the best strategy to navigate the maze and reach the treasure in the fewest possible steps.
When navigating the maze, the agent uses either exploitation or exploration to choose its next action. Exploitation involves using the agent’s current knowledge to make the best decision, and exploration involves taking random actions to discover new strategies (Watkins, 1989).
The ideal proportion to use between these varies based on the problem to be solved and the stage where the learning is at. Initially, high exploration will be more beneficial since there is almost no prior knowledge. Over time, as the agent learns, exploitation should be increased to make use of the acquired knowledge. In the code, the variable epsilon controls the balance between the two.
Reinforcement learning here involves the agent interacting with the environment to maximize its cumulative rewards (Watkins, 1989). During pathfinding, the agent (pirate) learns by taking actions (steps in certain directions), receiving rewards (or penalties), and updating its policy to optimize the path to the treasure. Over time, the agent learns the best actions to take in different states to reach the treasure efficiently, all to maximize its cumulative rewards.
## Use of Algorithm in Solving Complex Problems
AI and Machine Learning Algorithms can autonomously handle and solve complex problems by analyzing large amounts of data, identifying the patterns, and optimizing their decisions based on perceived feedback. 
In our code, to solve the complex problem of finding the most efficient pathway through the maze, we implemented a deep Q-learning algorithm. The algorithm includes a neural network that approximates the Q-function and an agent that interacts with the maze and stores its experiences (state, action, reward, next state) in a ‘experience’ replay buffer. The experiences are then randomly sampled to train the neural network to update its weights to better predict Q-values. I also implemented the Bellman equation to calculate the target Q-values based on the current rewards and the maximum predicted Q-values of upcoming states (Mnih et al., 2013). The agent then learns an optimal policy to navigate the maze by iteratively updating the neural network via the agent’s experience.
## Working on the Project
I was first provided with a Python function 'qtrain' that implemented a form of the Q-learning algorithm for a maze-solving game. The game represents a maze where an agent (the pirate) needs to find the path to a goal (the treasure). The provided code included the setup of the Q-learning parameters, the training loop, and the logic for the agent's decision-making between exploration and exploitation. The Q-learning algorithm gets implemented using a neural network model to approximate the Q-function.

I completed the missing code for the 'qtrain' function that encapsulated the Q-learning algorithm by setting up the essential parameters and the training loop. This function drives the interaction between the intelligent agent and the environment (the maze) by guiding the agent’s learning process through exploration and exploitation.

## What do Computer Scientists Do and Why Does It Matter? 

Computer Scientists play a critical role in the development of technology, solving complex problems, and optimizing systems and processes. In projects such as this, their cumulative skills lead to improved decision-making, optimized operations, and improved data accessibility, which contributes to better strategic planning, better resource management, and better performance of the company they are working for.

## Approaching Problems as a Computer Scientist

First, there should be a thorough analysis of the client's requirements in order to select the most suitable technology stack. The application should be built iteratively by starting from an MVC (minimal viable product) and gradually adding features based on feedback from users and stakeholders. Every requirement should be broken down into small task problems to be solved. After all of those pieces are solved, comprehensive testing and validation should be done so that all parts of the application function as expected. Documentation should also be added (in the form of comments and docstrings) for the future maintainers of the project.

## Ethical Responsibilities

To the end user, we should ensure the privacy, security, and accuracy of the software, as well as being transparent about its capabilities and limitations.

Computer scientists, towards the organization they are working for, should maintain integrity, provide honest assessments, avoid conflicts of interest, and ensure compliance with legal and ethical standards. 

### References
Mnih, V., Badia, A. P., Mirza, M., Graves, A., Lillicrap, T., Harley, T., ... & Kavukcuoglu, K. (2016). Asynchronous methods for deep reinforcement learning. In International conference on machine learning (pp. 1928-1937). <br/>
Sutton, R. S., & Barto, A. G. (2018). Reinforcement learning: An introduction. MIT Press.<br/>
Watkins, C. J. C. H. (1989). Learning from delayed rewards (Ph.D. thesis). Cambridge University.<br/>
