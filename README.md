[comment]: <> "LTeX: language=en-US"
## Table of Contents  
1. [Introduction](#introduction)  
2. [Installation](#installation)
3. [Usage](#usage)
4. [Documentation](#documentation)
# Introduction

This is a project by Alexander Reimer and Matteo Friedrich.

We are trying to create an open-source interface for recognizing ERPs of the human brain, for usage in brain–computer interfaces (BCIs). It is being developed with simplicity and ease of use in mind.

We hope to make peoples lives easier and give beginners like ourselves a better chance to develop their own BCIs.

We're just at the beginnings ourselves, however, and also want to learn and grow through this project. Any help and advice is appreciated!

# Installation

1. Clone this GitHub Repository: \
    ``git clone https://github.com/AR102/Interpreting-EEG-with-AI``

2. Create the file __config.jl__ in the folder __src__.

To update, use ``git pull``.

# Usage

1. Start Julia in the directory __the/path/to/Interpreting-EEG-with-AI/src__
2. Use ``]`` to enter the package manager
    - ``activate . ``
    - ``instantiate`` to download necessary packages
3. Exit with Backspace
4. ``include("filename")`` to execute

The way this program is made, it should be able to run by default. So the first thing you should do is execute __train.jl__ and check if any errors occur.

This file is responsible for training the neural network. The files __gather_data.jl__ and __main.jl__ are responsible for collecting your own training/test data and using the BCI live, respectively. However, they aren't finished yet.

If there aren't any errors or problems, you can start customizing the program! 

You can put your own configuration in the __config.jl__ file you created during the installation.

You can look at the default parameters in __default_config.jl__.

Some examples you could put into your config file:

```
# Decrease number of available EEG channels to 8
NUM_CHANNELS = 8
```

```
# Increase learning rate to 0.002
LEARNING_RATE = 0.002
```

You can also create multiple config files and switch between them by replacing ``include("config.jl")`` with ``include("config2.jl")`` or whatever you named the file.

# Documentation

The detailed documentation of all parameters can be found [here](https://github.com/AR102/Interpreting-EEG-with-AI/wiki/Documentation).