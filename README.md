# Snake-Game-AI

The given code implements a **Deep Q-Network (DQN)** approach for training an AI agent in a game (such as the Snake game) using reinforcement learning. It consists of two main components: the **Linear_QNet** model and the **QTrainer** class, designed to handle the training process with the **Adam optimizer**.

### 1. **Linear_QNet Class**:
   This class defines a simple neural network architecture with two linear layers. It takes in the state of the game (such as the snake's position and direction), processes it through a hidden layer, and outputs Q-values, which represent the expected future rewards for each possible action (e.g., up, down, left, right).
   
   - **Input Layer**: Takes the game state as input.
   - **Hidden Layer**: Applies a **ReLU (Rectified Linear Unit)** activation function to introduce non-linearity.
   - **Output Layer**: Outputs Q-values for each action.
   - **Save Function**: Saves the trained model to disk for later use.

### 2. **QTrainer Class**:
   This class handles the training of the neural network using reinforcement learning concepts and the Adam optimizer. It performs one step of training, adjusting the model based on the agent's experience during gameplay.
   
   - **Loss Function**: Uses **Mean Squared Error (MSE)** to calculate the difference between predicted Q-values and target Q-values.
   - **Training Step**: 
     - Takes the current state, next state, action, reward, and done flag (indicating if the game is over).
     - Updates Q-values based on the Bellman equation:
       \[
       Q(s, a) = r + \gamma \max Q(s', a')
       \]
       where \(r\) is the reward, \(\gamma\) is the discount factor, and \(s', a'\) are the next state and action.
     - Uses **Adam optimizer** to update the model parameters by minimizing the loss function.

The overall structure is designed to allow the agent to learn from its interactions with the environment, where it gets feedback in the form of rewards and adjusts its strategy accordingly. The Adam optimizer is used to efficiently update the model during training, balancing learning speed and stability.


![Snake](https://github.com/user-attachments/assets/01d00bfc-d19c-4f95-8239-d7140904bc05)
![Figure_1](https://github.com/user-attachments/assets/f8ebe37a-ec8d-496b-998b-fb9c61a52fe2)
