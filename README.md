# robotWalkNeuralNet
Neural Network to reproduce robot walk path

Used a Neural Network to reproduce robot walk path. And detect it's sensor failures from the reproduced walk path.

Robot moves from any point A to any point B within a predefined area. It will avoid obstacles in it's path. Four sensors provide distance to obstacle on four sides of the robot. Each sensor takes nine samples per second.

Shown plots are for front sensor obstacle distance from different walks of the robot. Past walk sensor data is used to train neural network to reproduce walk behavior of the robot.

Neural Network with Autoencoder kind of model is used. So this network will compress the walk paths and then reproduce expected walk paths from this compressed walk signature. We also used custom activation function to achieve compression in this neural network. Trained network produces three seconds of walk path.

Two checks are used to detect sensor faults. 1) Sample deviation check detects large deviations in each sensor value from the neural network reproduced values to detect faulty sensor output. 2) Path min-max difference check is used to detect stuck sensor kind of faults.

See below link for more info:
https://www.linkedin.com/pulse/robot-sensor-fault-detection-machine-learning-sarabjeet-singh
