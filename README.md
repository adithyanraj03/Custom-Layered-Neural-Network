# Custom-Layered-Neural-Network
User-Inputted on command custom neural network creating program.
This repository contains the implementation of a custom layered neural network using HPP (Header++) and CPP (C++). The neural network is designed to be flexible and customizable, allowing users to define the number of layers, the number of neurons in each layer, and the activation function for each neuron.

Features:
- Customizable architecture: Users can define the number of layers and the number of neurons in each layer according to their specific requirements.
- Activation functions: The neural network supports various activation functions, including sigmoid, ReLU, and tanh. Users can choose the activation function for each neuron.
- Backpropagation algorithm: The network uses the backpropagation algorithm for training, allowing it to learn from labeled data and adjust the weights and biases of the neurons to improve accuracy.
- Forward propagation: The network performs forward propagation to make predictions on unseen data based on the learned weights and biases.
- Error calculation: The network calculates the error between the predicted output and the expected output using different error metrics, such as mean squared error (MSE) or cross-entropy loss.

Usage:
1. Define the architecture of the neural network by specifying the number of layers and the number of neurons in each layer in the "main.cpp" file.
2. Set the activation function for each neuron in the "main.cpp" file.
3. Prepare the training data and labels in the desired format.
4. Compile and run the program using the provided makefile or by executing the following commands:
   - g++ main.cpp NeuralNetwork.cpp -o neural_network
   - ./neural_network

Dependencies:
- C++11 or higher

Example:
```cpp
#include <iostream>
#include "NeuralNetwork.hpp"

int main() {
    // Define the architecture of the neural network
    std::vector<int> layers = {2, 3, 1};

    // Create an instance of the neural network
    NeuralNetwork nn(layers);

    // Set the activation function for each neuron
    nn.setActivationFunction(1, ActivationFunction::Sigmoid);
    nn.setActivationFunction(2, ActivationFunction::ReLU);

    // Prepare the training data and labels
    std::vector<std::vector<double>> trainingData = {{0, 0}, {0, 1}, {1, 0}, {1, 1}};
    std::vector<std::vector<double>> labels = {{0}, {1}, {1}, {0}};

    // Train the neural network
    nn.train(trainingData, labels, 1000, 0.01);

    // Make predictions on unseen data
    std::vector<double> input = {0, 1};
    std::vector<double> output = nn.predict(input);

    // Print the predicted output
    std::cout << "Predicted output: " << output[0] << std::endl;

    return 0;
}
```

Contributing:
Contributions to this project are welcome. If you find any issues or have any suggestions for improvement, please feel free to submit a pull request or open an issue.

License:
This project is licensed under the GNU General Public License v3.0. See the LICENSE file for more information.

Acknowledgements:
This implementation is inspired by the concepts of neural networks and backpropagation algorithms. Special thanks to the authors and contributors of relevant research papers and online resources.

Please ensure that you have the necessary dependencies and libraries installed before running the program.
