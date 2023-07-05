cmake_minimum_required(VERSION 3.23)
project(Code_4)

set(CMAKE_CXX_STANDARD 14)

include_directories(ann-master/include)
include_directories(ann-master/include/utils)

add_executable(Code_4
        ann-master/include/utils/Math.hpp
        ann-master/include/utils/Misc.hpp
        ann-master/include/json.hpp
        ann-master/include/Layer.hpp
        ann-master/include/Matrix.hpp
        ann-master/include/NeuralNetwork.hpp
        ann-master/include/Neuron.hpp
        ann-master/src/neural_network/backPropagation.cpp
        ann-master/src/neural_network/constructor.cpp
        ann-master/src/neural_network/feedForward.cpp
        ann-master/src/neural_network/loadWeights.cpp
        ann-master/src/neural_network/NeuralNetwork.cpp
        ann-master/src/neural_network/setErrors.cpp
        ann-master/src/neural_network/train.cpp
        ann-master/src/utils/Math.cpp
        ann-master/src/utils/Misc.cpp
        ann-master/src/autoencoder_classify.cpp
        ann-master/src/Layer.cpp
        ann-master/src/Matrix.cpp
        ann-master/src/Neuron.cpp
        ann-master/src/train.cpp)
